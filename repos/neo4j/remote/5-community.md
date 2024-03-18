## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:accc745d81486195b348f01fd833c174bf9a36b922a7e10a7021616133be6eb8
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
