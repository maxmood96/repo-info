<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.30`](#neo4j4430)
-	[`neo4j:4.4.30-community`](#neo4j4430-community)
-	[`neo4j:4.4.30-enterprise`](#neo4j4430-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.16`](#neo4j516)
-	[`neo4j:5.16-bullseye`](#neo4j516-bullseye)
-	[`neo4j:5.16-community`](#neo4j516-community)
-	[`neo4j:5.16-community-bullseye`](#neo4j516-community-bullseye)
-	[`neo4j:5.16-community-ubi8`](#neo4j516-community-ubi8)
-	[`neo4j:5.16-enterprise`](#neo4j516-enterprise)
-	[`neo4j:5.16-enterprise-bullseye`](#neo4j516-enterprise-bullseye)
-	[`neo4j:5.16-enterprise-ubi8`](#neo4j516-enterprise-ubi8)
-	[`neo4j:5.16-ubi8`](#neo4j516-ubi8)
-	[`neo4j:5.16.0`](#neo4j5160)
-	[`neo4j:5.16.0-bullseye`](#neo4j5160-bullseye)
-	[`neo4j:5.16.0-community`](#neo4j5160-community)
-	[`neo4j:5.16.0-community-bullseye`](#neo4j5160-community-bullseye)
-	[`neo4j:5.16.0-community-ubi8`](#neo4j5160-community-ubi8)
-	[`neo4j:5.16.0-enterprise`](#neo4j5160-enterprise)
-	[`neo4j:5.16.0-enterprise-bullseye`](#neo4j5160-enterprise-bullseye)
-	[`neo4j:5.16.0-enterprise-ubi8`](#neo4j5160-enterprise-ubi8)
-	[`neo4j:5.16.0-ubi8`](#neo4j5160-ubi8)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:378f324702724f55658f3efcc2527dd5ff8c8f3d3513c33e5fed5d227ff7396e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:192a103d321e3754d20c5826be77d3901fdc937da5899d852dbc1b21d3a9b9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb449511f25d21e580d2ac3086932d171816aa91126d46f817185fb6566a9cf3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e00db36d12243c3b74e481f64ad66794016f371b1317c164f0cd28258f9bb2`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 142.0 MB (142006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582385003856074444678082daceb0220d1acf1bee746c241767eaf7933c878`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef17d2013da3b27d9cc8e0d90ec4fec0ee4fb11ebe252af03ce1a7f814a73c`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18480adcca5af06da5990f877fa33c882449182bccb79c10ff4ae9aec38443f`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 120.5 MB (120546270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:791df525c83cc3add0a19776b54b39ad7eaea4fed3e254e10cae8008cf09c19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb2ae7913b82c9ee867b95a6b976cfe632661f42afcea6c87cfda7e89c180a4`

```dockerfile
```

-	Layers:
	-	`sha256:b30a6f0661174c9962aafcbb4ae4efbfe0f1196f7fd0ff7e89e7796942534e37`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd5813479bf33136afb1f85ded680cc07f175ba6e2c75089c1c93cb37755fb`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:378f324702724f55658f3efcc2527dd5ff8c8f3d3513c33e5fed5d227ff7396e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:192a103d321e3754d20c5826be77d3901fdc937da5899d852dbc1b21d3a9b9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb449511f25d21e580d2ac3086932d171816aa91126d46f817185fb6566a9cf3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e00db36d12243c3b74e481f64ad66794016f371b1317c164f0cd28258f9bb2`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 142.0 MB (142006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582385003856074444678082daceb0220d1acf1bee746c241767eaf7933c878`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef17d2013da3b27d9cc8e0d90ec4fec0ee4fb11ebe252af03ce1a7f814a73c`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18480adcca5af06da5990f877fa33c882449182bccb79c10ff4ae9aec38443f`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 120.5 MB (120546270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:791df525c83cc3add0a19776b54b39ad7eaea4fed3e254e10cae8008cf09c19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb2ae7913b82c9ee867b95a6b976cfe632661f42afcea6c87cfda7e89c180a4`

```dockerfile
```

-	Layers:
	-	`sha256:b30a6f0661174c9962aafcbb4ae4efbfe0f1196f7fd0ff7e89e7796942534e37`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd5813479bf33136afb1f85ded680cc07f175ba6e2c75089c1c93cb37755fb`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:3ca5bd7fb96247612b86ddc1d225b5b6e05c1c6473185e227f182dcab824f011
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1eb5378fe207f8023517d5d5f2437a9ae578c6179c0d0917cf298f4c0f1df41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402499192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78253fdb59394bcc43890175dd867d337fd94fa54e332e16cb313a329ddbcf14`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e3b493682ef0c012693021016cdb635597ad66078e2459b34c1c802d451e43`  
		Last Modified: Fri, 16 Feb 2024 02:50:16 GMT  
		Size: 145.3 MB (145271122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b1435146d7bcae51d98da09c3a494e57b410965054f4a3e55f1dd7a8136855`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cfccbb1af040ece603b2781a6c70bff35f72d6f65bb2293ccf9213280dfc0`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34c4b777c6507310d60d8beac64a9c7e025aef534d54754ceac3d10fcdc658`  
		Last Modified: Fri, 16 Feb 2024 02:50:17 GMT  
		Size: 225.8 MB (225792389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5a6b17e0e6bac4ddf8a7553329246cba8024a4d49fae0bee461bc0df420f26a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf49abdd843e37603ba4ac8c9f4c85828d203e1c4817d872782e2b4576d59653`

```dockerfile
```

-	Layers:
	-	`sha256:f1745c678b2a247549d0a861bd468cba537f77a4c7b1af9ae6445ac9baf8da81`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 2.7 MB (2698858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa96a8119e23c3e684bc45aff961afdc4842a746210ec7778fe93ee667f3ffe`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9ff9344933c02a49e56a5b54d4c1b43a1b8af1268d9bbbd806d7a7fe05b9511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397846270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c402e0210ec834c0dbb1264432f5846b45d7f1de77e665ff34d6a6fe7cc4ef`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e00db36d12243c3b74e481f64ad66794016f371b1317c164f0cd28258f9bb2`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 142.0 MB (142006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b89648bb1da8004d989fb51ab4c1f3b98238bbdea10883e6a9e6c7eecffd484`  
		Last Modified: Wed, 14 Feb 2024 01:12:49 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bd7b70da80f715c87d8ac6bda1e2b10c479895f45f6335c9674c07aff80878`  
		Last Modified: Wed, 14 Feb 2024 01:12:49 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d15354bca9022c24b14b117bdcd6cb182f3fe3b2934e980bd1c48ccc6c094f`  
		Last Modified: Wed, 14 Feb 2024 01:12:56 GMT  
		Size: 225.8 MB (225755342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:dcfeb8438069c2a0868fef9ecf00021496d57440b3ac65985105d01b2955c5d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78d1fc9900547def192bbc4e6717c20f4fc795546ae304fe0e501519e53ed9a`

```dockerfile
```

-	Layers:
	-	`sha256:e72b0c2283b79723494702a605d077c68a3ec8809254774e05882309ad337e50`  
		Last Modified: Wed, 14 Feb 2024 01:12:50 GMT  
		Size: 2.7 MB (2699180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e3bf0bc753d9e7d0cc4ed8b2d39d03e4d675eff8cf4cf6aaae940ed02d37db`  
		Last Modified: Wed, 14 Feb 2024 01:12:49 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30`

```console
$ docker pull neo4j@sha256:378f324702724f55658f3efcc2527dd5ff8c8f3d3513c33e5fed5d227ff7396e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:192a103d321e3754d20c5826be77d3901fdc937da5899d852dbc1b21d3a9b9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb449511f25d21e580d2ac3086932d171816aa91126d46f817185fb6566a9cf3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e00db36d12243c3b74e481f64ad66794016f371b1317c164f0cd28258f9bb2`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 142.0 MB (142006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582385003856074444678082daceb0220d1acf1bee746c241767eaf7933c878`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef17d2013da3b27d9cc8e0d90ec4fec0ee4fb11ebe252af03ce1a7f814a73c`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18480adcca5af06da5990f877fa33c882449182bccb79c10ff4ae9aec38443f`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 120.5 MB (120546270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30` - unknown; unknown

```console
$ docker pull neo4j@sha256:791df525c83cc3add0a19776b54b39ad7eaea4fed3e254e10cae8008cf09c19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb2ae7913b82c9ee867b95a6b976cfe632661f42afcea6c87cfda7e89c180a4`

```dockerfile
```

-	Layers:
	-	`sha256:b30a6f0661174c9962aafcbb4ae4efbfe0f1196f7fd0ff7e89e7796942534e37`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd5813479bf33136afb1f85ded680cc07f175ba6e2c75089c1c93cb37755fb`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-community`

```console
$ docker pull neo4j@sha256:378f324702724f55658f3efcc2527dd5ff8c8f3d3513c33e5fed5d227ff7396e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-community` - linux; amd64

```console
$ docker pull neo4j@sha256:93fbb9ff278d3b7770b186d77b3aa1d3dd4e1b1e6817c422b07eb8d365d72d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297284887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d87277dbda4a84c2082bc49a240380faaba1e2bf9feef9a68b171890da90bd0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba095a8cc0d4c47de210a416e31cfbffa52fa59c8d656264c2e132f3a815b41d`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 145.3 MB (145271081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fac6bdf3a9a7a930745a4b8168349a0cc05fdec7f1f2abd52747d1b70c8b96b`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7db21cae4b3ff6d0bcacd513b0b182ddd3d265fd1806e4ab200aa6c08960d3f`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7f9d46d6b68f8b2910da80214f71d826369c9ec7fa707568fbfc90a5374f2`  
		Last Modified: Fri, 16 Feb 2024 02:50:05 GMT  
		Size: 120.6 MB (120578124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:85d0647e8edcda71655de869e1ad5201f74e83ab9701c81fe53ffc5eb59de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7a29ac354704e1e586afbc98b35478dc723a5c4b5ff13eea3ae729adfc30df`

```dockerfile
```

-	Layers:
	-	`sha256:36b48bce98a026724b6f4198924fa5e42f8d00fbfd339f8dcae87d5fbc8edda4`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 2.6 MB (2575369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436861a1531ac40aacf9abaabd6217fa07fe2b652c590a79ba7fb0a3178f46cb`  
		Last Modified: Fri, 16 Feb 2024 02:50:02 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:192a103d321e3754d20c5826be77d3901fdc937da5899d852dbc1b21d3a9b9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292637196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb449511f25d21e580d2ac3086932d171816aa91126d46f817185fb6566a9cf3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e00db36d12243c3b74e481f64ad66794016f371b1317c164f0cd28258f9bb2`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 142.0 MB (142006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582385003856074444678082daceb0220d1acf1bee746c241767eaf7933c878`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef17d2013da3b27d9cc8e0d90ec4fec0ee4fb11ebe252af03ce1a7f814a73c`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 9.4 KB (9382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18480adcca5af06da5990f877fa33c882449182bccb79c10ff4ae9aec38443f`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 120.5 MB (120546270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:791df525c83cc3add0a19776b54b39ad7eaea4fed3e254e10cae8008cf09c19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2595040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb2ae7913b82c9ee867b95a6b976cfe632661f42afcea6c87cfda7e89c180a4`

```dockerfile
```

-	Layers:
	-	`sha256:b30a6f0661174c9962aafcbb4ae4efbfe0f1196f7fd0ff7e89e7796942534e37`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 2.6 MB (2575695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd5813479bf33136afb1f85ded680cc07f175ba6e2c75089c1c93cb37755fb`  
		Last Modified: Wed, 14 Feb 2024 01:11:42 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.30-enterprise`

```console
$ docker pull neo4j@sha256:3ca5bd7fb96247612b86ddc1d225b5b6e05c1c6473185e227f182dcab824f011
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.30-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1eb5378fe207f8023517d5d5f2437a9ae578c6179c0d0917cf298f4c0f1df41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402499192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78253fdb59394bcc43890175dd867d337fd94fa54e332e16cb313a329ddbcf14`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e3b493682ef0c012693021016cdb635597ad66078e2459b34c1c802d451e43`  
		Last Modified: Fri, 16 Feb 2024 02:50:16 GMT  
		Size: 145.3 MB (145271122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b1435146d7bcae51d98da09c3a494e57b410965054f4a3e55f1dd7a8136855`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cfccbb1af040ece603b2781a6c70bff35f72d6f65bb2293ccf9213280dfc0`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34c4b777c6507310d60d8beac64a9c7e025aef534d54754ceac3d10fcdc658`  
		Last Modified: Fri, 16 Feb 2024 02:50:17 GMT  
		Size: 225.8 MB (225792389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5a6b17e0e6bac4ddf8a7553329246cba8024a4d49fae0bee461bc0df420f26a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf49abdd843e37603ba4ac8c9f4c85828d203e1c4817d872782e2b4576d59653`

```dockerfile
```

-	Layers:
	-	`sha256:f1745c678b2a247549d0a861bd468cba537f77a4c7b1af9ae6445ac9baf8da81`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 2.7 MB (2698858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa96a8119e23c3e684bc45aff961afdc4842a746210ec7778fe93ee667f3ffe`  
		Last Modified: Fri, 16 Feb 2024 02:50:14 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.30-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9ff9344933c02a49e56a5b54d4c1b43a1b8af1268d9bbbd806d7a7fe05b9511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397846270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c402e0210ec834c0dbb1264432f5846b45d7f1de77e665ff34d6a6fe7cc4ef`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 25 Jan 2024 10:35:36 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["bash"]
# Thu, 25 Jan 2024 10:35:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 10:35:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 25 Jan 2024 10:35:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 10:35:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 10:35:36 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 10:35:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 25 Jan 2024 10:35:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 10:35:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e00db36d12243c3b74e481f64ad66794016f371b1317c164f0cd28258f9bb2`  
		Last Modified: Wed, 14 Feb 2024 01:11:45 GMT  
		Size: 142.0 MB (142006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b89648bb1da8004d989fb51ab4c1f3b98238bbdea10883e6a9e6c7eecffd484`  
		Last Modified: Wed, 14 Feb 2024 01:12:49 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bd7b70da80f715c87d8ac6bda1e2b10c479895f45f6335c9674c07aff80878`  
		Last Modified: Wed, 14 Feb 2024 01:12:49 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d15354bca9022c24b14b117bdcd6cb182f3fe3b2934e980bd1c48ccc6c094f`  
		Last Modified: Wed, 14 Feb 2024 01:12:56 GMT  
		Size: 225.8 MB (225755342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.30-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:dcfeb8438069c2a0868fef9ecf00021496d57440b3ac65985105d01b2955c5d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78d1fc9900547def192bbc4e6717c20f4fc795546ae304fe0e501519e53ed9a`

```dockerfile
```

-	Layers:
	-	`sha256:e72b0c2283b79723494702a605d077c68a3ec8809254774e05882309ad337e50`  
		Last Modified: Wed, 14 Feb 2024 01:12:50 GMT  
		Size: 2.7 MB (2699180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e3bf0bc753d9e7d0cc4ed8b2d39d03e4d675eff8cf4cf6aaae940ed02d37db`  
		Last Modified: Wed, 14 Feb 2024 01:12:49 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community-bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community-bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.16.0-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.16.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.16.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.16.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:9f51a5f6a8bcb6fdd62ab508afdd1d834fc7831485de9df2a79532d9299e1554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7a9eabe22e802af5761350a4762280848cbbb7ca6819392aaec11ac5936ebd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (559974948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b29c77001dafe383df7e5bbc3f0da069b210432c791be470b8b9e7971ec5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428ce3e4156088dba5f9a936aa203bf0209e3dc078d3e7471f2ff554b3f2de1`  
		Last Modified: Mon, 05 Feb 2024 21:52:00 GMT  
		Size: 152.2 MB (152177043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f439e7a8d82c07a57f8f51fc698aa9a3479784e5dd62b6a894d09711d7ea1a6`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced9340d9865370122c1b9953a8d65277c8fba4d6b392be64a702070f8ee33d`  
		Last Modified: Mon, 05 Feb 2024 21:52:04 GMT  
		Size: 368.5 MB (368496317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:21ac93bd2ba8887bea839f0d54d347c0ff4416ef4e44a73577118b2d91e47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9023828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863073c6981bbb2ee3493a34843562517505f54dffc000667bd8c1f031a45722`

```dockerfile
```

-	Layers:
	-	`sha256:31a38617eaeaaa5bed9990e291d8a01fedfc7de8c86e7e39ab2c80005ed68fd3`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 9.0 MB (9003592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d2101f1fa58d0e564da48e808e2f031c6eb05ff8ed8edb6ab34094b7eec170`  
		Last Modified: Mon, 05 Feb 2024 21:51:56 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c6e6e02cab4c8e0e09fb585c5c54f51c20efb38b11d3f5d8bae1f21b6400d35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556874923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836fa77801ce22b7c05b0dfb327d1b3871b80a505cea5af7df8ec233b4dc3769`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318e1f86bc1cc2d1de008ba191458662cad368500da28e4a9d748b8cfe7f6b4`  
		Last Modified: Mon, 05 Feb 2024 22:38:03 GMT  
		Size: 368.5 MB (368496396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:7da9860217f48502beef22b5e0988ee0942b919821e1e952c65f8b11e081d4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9021634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2215b859788af6709b3b5cfd9f6d30ab6c224bd4e36a48399247966af0573578`

```dockerfile
```

-	Layers:
	-	`sha256:6dd1db8dc5a4f2583fea1b98d887de14aca1a58b33ef2c4796c8d8ed45ecb58f`  
		Last Modified: Mon, 05 Feb 2024 22:37:55 GMT  
		Size: 9.0 MB (9001554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162657c00396179f4a94fe58b95c5745224e48b94def3fdae02a12ff28226da2`  
		Last Modified: Mon, 05 Feb 2024 22:37:54 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:15fbad578c41b6cec02166051730b9cf7e64c74148747158a5f87862c4735268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:ea88138f6d5dd19abbc96dae932357e03b12b7b79ac741735d4b74aa68e30c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291732029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a9b39a2ebe2287ff6bec0240991f31b0e0368fe91e3096ec58fc2422405126`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a0ec150a9813f9efa20888461f3aec2d293e98ec3ef98b72e1ce1c4c2831b`  
		Last Modified: Fri, 16 Feb 2024 02:49:59 GMT  
		Size: 144.9 MB (144892407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f808d1839321bf44f95f6068a7b83ce65b727cc1be42983d1259dac94bc7586e`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2066672f161d2b6d0153fd1af8a50ec5faa3e65a46b9edd5c24287fbfefe421d`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6776531ff9d6fbf78e5897af6ba57bd8923a5139a82a71786f93a059263ca`  
		Last Modified: Fri, 16 Feb 2024 02:49:58 GMT  
		Size: 115.4 MB (115403874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:59ccad0d449f0c68f1d2d495c949df2829f11e36dffff38604ef2b879f060338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621047c0a2ce1aba723edcdab83823cdfed7e523f2af98d8bbf3d8dce3296e5c`

```dockerfile
```

-	Layers:
	-	`sha256:90b3d133924e7a60d96e5c62f2fe06546b692217557b6794b020a30f5c39c7ac`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 2.6 MB (2565919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51e22e3ea2e83dc8bdecafaf1f59633a63c89648c50a702058089adb41bbb240`  
		Last Modified: Fri, 16 Feb 2024 02:49:56 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ac0918a0d528d279494acc61e5e254768d616ad043598623bb8a9d645c9d536c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289173265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0be18ea5d1bd41567b7acb7efe6b334fe1f927f9da76356fd82e5356148bcd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1574b03b3ee75f538afdda3e2157972464565301a325e6e3c38856067fe46138`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746affe15d78fb36034d41d455ee8e6615587a111df5c4dd97238ec3de649e0a`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2347d76c6e3f537e83baf3171e8b9ee605379e20e229c165d05dc12b52b35f`  
		Last Modified: Wed, 14 Feb 2024 00:58:00 GMT  
		Size: 115.4 MB (115368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee1807831151e9535b2a9ec9527700b044100325795ba8a84e16a9625a09748f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29029f1a1f1347cf20f5bbb3a5a7be744f9706242e8014c593813c0aad11704d`

```dockerfile
```

-	Layers:
	-	`sha256:30b4d7462e12abbaea28146a41e099ffa5342a341ddb35a2fd50350a52eb8fb5`  
		Last Modified: Wed, 14 Feb 2024 00:57:58 GMT  
		Size: 2.6 MB (2566269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72862e7ef0bf6348618d6ea7b3e699a6bc53582b96be27a1193dc0ba47777f75`  
		Last Modified: Wed, 14 Feb 2024 00:57:57 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:7170e09968a1887b8de65a27c10cc50c1293993164e7101a3277144112cdbf19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:7348d315774c2eb8608194eebd2940b15368e97b0cafbd832583287158630fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303951431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d6a5db762dbcfc882bfb65ad6e6f8eee9145f4f81d2e6de6f4504d53fdf93b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e91fbb26e50b855bd736cda2e05de1bf6db8eea69ff692c8c12949e84ff0054`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 152.2 MB (152177384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d55306869856437612e4dd368c214e41a47a4459ccfb88fc384d65aa80b3b02`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f8b0f48593a36c834227d64f5ca896014a548ce40cad2c1f7de01d7ddb998`  
		Last Modified: Mon, 05 Feb 2024 21:51:21 GMT  
		Size: 112.5 MB (112472464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:5528b76bd1e9535412da4b1fd4af25ca8d321be91f9132bf1148ec0358875419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52d893f3e1f8c9176870abb98f835fc591f5f30b9e6b5ccc53a5a58804b3e4`

```dockerfile
```

-	Layers:
	-	`sha256:ee0484d0dd3634dd6651e35827537bb5c11682a66be431f90faa75adb8e436cf`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 8.8 MB (8810871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035964aff6badbb47cb1426ddb5aa33fe41a70b834a7d2f2fc06808301120a4`  
		Last Modified: Mon, 05 Feb 2024 21:51:19 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:120d05bebff0234e1ea3d977b1b587e9da654a86c73175b11a4c6a4396db5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300851010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d62f45b6d70ea8045bbe82b5bc3c3fc3ffebd18ca9cc1e304371a5d2b67b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL io.openshift.tags="minimal rhel8"
# Mon, 22 Jan 2024 14:26:01 GMT
ENV container oci
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["/bin/bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -rf /var/log/*
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Mon, 22 Jan 2024 14:26:01 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Mon, 22 Jan 2024 14:26:01 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 22 Jan 2024 14:26:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/usr
# Mon, 22 Jan 2024 14:26:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
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
	-	`sha256:3f1c853cd4889d9db94637ef29a8f3c85d486e15b832921c1a7f4a31b911c3a0`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2650c9f2de2c9e46addef2d431b3f3d9722e35a8809f36ed9d0dece4971b16e1`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 112.5 MB (112472483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8446eed76b3b0771b001800d21830ef6c2e2493e4dd945d6280d2a0192bc8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47dc859b37b27c5c04c129a5c81e7031528e4652d78a39b28a58b1e9b8c7b79`

```dockerfile
```

-	Layers:
	-	`sha256:042cfec037864f590974ccd22e3490658c66b18f88ba9ca3013844998d80d635`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 8.8 MB (8808841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accddd2d2d2204f057957ab8ffab6df2d4bac63505fdf62291d3a2ef87f53e84`  
		Last Modified: Mon, 05 Feb 2024 22:36:55 GMT  
		Size: 21.4 KB (21433 bytes)  
		MIME: application/vnd.in-toto+json
