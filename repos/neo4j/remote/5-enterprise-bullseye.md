## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:6c32a6545e01578f785eaba240b5fff9c0887bfc9442159022b908c99ea12b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:cfa52c9098034d6e7cce6742f8677655c7814fe8da0cf974cd400fd45b1ab849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.2 MB (652238663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3a834ae8e0944c328cd1984a283eeba3be2df975fc74b4875488ff89bce625`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Jun 2025 10:01:35 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 10:01:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jun 2025 10:01:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=906d67491fa2f1352f06fa327d3b850b5f8163ad1fe7bdd8d193326c2855e65b NEO4J_TARBALL=neo4j-enterprise-5.26.8-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Jun 2025 10:01:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 10:01:35 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Jun 2025 10:01:35 GMT
VOLUME [/data /logs]
# Mon, 09 Jun 2025 10:01:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Jun 2025 10:01:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Jun 2025 10:01:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eaab5c118a7b875ad5b00746ee337f869d197771fb3d09d965c78daf4768c5`  
		Last Modified: Wed, 11 Jun 2025 02:44:37 GMT  
		Size: 144.6 MB (144635026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd54d9d2598c3ef23d39ed5752971da512cfeb26e6c77294e18a4c8685bde7e`  
		Last Modified: Wed, 11 Jun 2025 00:07:36 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf50e45370c18028154422bd4a1ff748239d87f96fedb83c8fcd0d7ea83e272`  
		Last Modified: Wed, 11 Jun 2025 00:07:36 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e945e1901c50ef1ba9a4759881977026e8888cba7de31a4d164c007040cd81`  
		Last Modified: Wed, 11 Jun 2025 02:44:47 GMT  
		Size: 477.3 MB (477333674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e57c9c37440e17bc0e02c553fa6c5573128a396f5df0ee51f23d3dd04dffb995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b6fa89b6a4d5c192ad59786d81832ef3bdbb90dfcad4988f61c28d197f72c1`

```dockerfile
```

-	Layers:
	-	`sha256:f715efc6ebbf6fb2a483a68a3f0c3362a5e749880c244a5d4584c886af3a6112`  
		Last Modified: Wed, 11 Jun 2025 02:44:08 GMT  
		Size: 4.9 MB (4859889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c841f05f96ab34d2363c37978595226ebb0008f8454ba725ddb52b6a7fee04a`  
		Last Modified: Wed, 11 Jun 2025 02:44:09 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:100f5a5f7cfd11e06e5b84cb5f8a1ae7f5bf5813125ccf807edc9cad9ecbc91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.8 MB (648848494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470b385ac31f55504e597b9ee27f385dbf77790cb3fded01410a14c7eb54ec1f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Jun 2025 10:01:35 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 10:01:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jun 2025 10:01:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=906d67491fa2f1352f06fa327d3b850b5f8163ad1fe7bdd8d193326c2855e65b NEO4J_TARBALL=neo4j-enterprise-5.26.8-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Jun 2025 10:01:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 10:01:35 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Jun 2025 10:01:35 GMT
VOLUME [/data /logs]
# Mon, 09 Jun 2025 10:01:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Jun 2025 10:01:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Jun 2025 10:01:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4597b8d774c37ff2a36ab9fe4dba1a924caaed8279e24328a0e943dd6d2da`  
		Last Modified: Wed, 11 Jun 2025 05:54:40 GMT  
		Size: 143.5 MB (143512642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530c95564c4d6d1e08f2a20f685cdeb91c0194b56ca4058cfa14b556b3ba58e2`  
		Last Modified: Wed, 11 Jun 2025 03:28:44 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb384045d04ae545d4a08ef287ade625464e4913e16788b3cc5abe2fc499eb3`  
		Last Modified: Wed, 11 Jun 2025 03:28:44 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daff5a71aff21acb82cd2c316a6471d259b134230c10fe80d67fb8688aecfe6d`  
		Last Modified: Wed, 11 Jun 2025 05:54:50 GMT  
		Size: 476.6 MB (476577742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3b4f232e1a5cdf3a8bcf8084ef93907c9fbf9fd8ef0f88d5221cc4fb391fd6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4854876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc9aab0e48f7b3c3ed5c73f4d5af45c682128bdb3c0a621b7f737cb55b19a5`

```dockerfile
```

-	Layers:
	-	`sha256:93edfb2c2cdb17fc012966c58f22958898cddeca7ff450defc8851d12a5fc7f4`  
		Last Modified: Wed, 11 Jun 2025 05:44:09 GMT  
		Size: 4.8 MB (4833694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6171b799262a33a8dfcb9927ec9e28a5410a1365b2bc1a42fee8d4d5e809c704`  
		Last Modified: Wed, 11 Jun 2025 05:44:10 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json
