## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:ed63f3acf32a36c60ad15e8f204617e0f8dfea5c73cc044f770d47bed6ad8def
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9962a91875fbdbf90ba8da095cd6dcc87366e9e915cc764717e986086215c8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589376168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963578a13e8844bcac6aa5a6dcb28a792a35cbbe849d3861559ebeb94545f7b9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80c317f17a024125041a7a8905c75e457fc35d9e36e1d2f450c2ff29213f02`  
		Last Modified: Thu, 27 Jun 2024 18:56:10 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4799fe4f2ec9c0e676a03d5ac852260becd9bdba3fa811c0c0b5456624c7667c`  
		Last Modified: Thu, 27 Jun 2024 18:56:07 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8820b732880945ebe8499c44a1f319b88cdf32e021a25a69ebea31a3ff49a4`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65574dcdba419ae254626f3430430a02421cf74bbb22554a37af0c8e1ca389ac`  
		Last Modified: Thu, 27 Jun 2024 18:56:13 GMT  
		Size: 412.8 MB (412833563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4694056ac18a4fb26d3f803f67b7ccb8d9517d7b77c2b03571a296fe0adc755c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b86ca6797db0cf81a5ead95793f9968c8e5c3d773ea71df2301a25d658cb754`

```dockerfile
```

-	Layers:
	-	`sha256:b0aeed5d6f4b44a6534d6bc656b0f79b8cd79a945b67b1e9a4b08fc4a350c3be`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 3.2 MB (3188135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:753b02a8234492a858c70bfd27164c65b3b9d577a95333fd8dddb1cdf88b1752`  
		Last Modified: Thu, 27 Jun 2024 18:56:07 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json
