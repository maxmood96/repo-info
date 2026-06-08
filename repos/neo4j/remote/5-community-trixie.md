## `neo4j:5-community-trixie`

```console
$ docker pull neo4j@sha256:a08208139e1a4f9a5673bbd4cbf8d6e8bfaf94884a92ef11c4b6cb84ff8c3374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:af74df64c72de87ee9b09f08aa32eda9bdd65655b22c9e880d20a56f68006ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355571323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54d6de860a6ded2c3ed53a3eea82ab6ef23cdaf8e4db580f9b8a308e2d8c7a6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 19:30:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jun 2026 19:30:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Jun 2026 19:30:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Jun 2026 19:30:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Mon, 08 Jun 2026 19:30:47 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Jun 2026 19:31:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Jun 2026 19:31:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 19:31:09 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Jun 2026 19:31:09 GMT
VOLUME [/data /logs]
# Mon, 08 Jun 2026 19:31:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Jun 2026 19:31:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 19:31:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91546e87de093cb1bf883e80b98dfbfb53c766ef11aae65618f56c74adee7dd`  
		Last Modified: Mon, 08 Jun 2026 19:31:35 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2329a3303a59d90e8bbd2b5fe2402d56e3366fb2007c49f2a43cc1e9464fb6ed`  
		Last Modified: Mon, 08 Jun 2026 19:31:29 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d9be793c3f0ccc9d38adae1404fb965e877181dcdbc4e2b2f7b3b7e323754d`  
		Last Modified: Mon, 08 Jun 2026 19:31:35 GMT  
		Size: 167.6 MB (167614366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:96c8ff29b399da7d104b84288f87e3d2edd82de78ca23112f695ce9f2e2e5f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f639121c83452c55fea07c62e1d163aff7fad86c8b32e9ebd0cd6b2a1c81ab`

```dockerfile
```

-	Layers:
	-	`sha256:8d33eafa304cbd1a155007533d2262df2d6cc6c626023259bb86f1fcc78d4135`  
		Last Modified: Mon, 08 Jun 2026 19:31:29 GMT  
		Size: 4.3 MB (4291176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f47ea5502edd81b93b313ae8175afbf9fa5a804e653082416297b6514aa7419d`  
		Last Modified: Mon, 08 Jun 2026 19:31:28 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:89c41c7dd44cba8c96f0735e8fcc22c6ec95a529a0bcd439ffdab29381fdc25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353300602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda0210987114531c51b6cbe3804ef96f598b20dabea1092ea3c6b18eb1c53e7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 19:30:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jun 2026 19:30:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Jun 2026 19:30:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Jun 2026 19:30:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Mon, 08 Jun 2026 19:30:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Jun 2026 19:31:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Jun 2026 19:31:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 19:31:04 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Jun 2026 19:31:04 GMT
VOLUME [/data /logs]
# Mon, 08 Jun 2026 19:31:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Jun 2026 19:31:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 19:31:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14cee931c5446fd5afa5cbca9e6689de0d93c92135ff5882a159615af3d49f3`  
		Last Modified: Mon, 08 Jun 2026 19:31:29 GMT  
		Size: 156.5 MB (156461249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4accb58223332ee7a5f9d4650e1676cf125273718dbc6547ea7b5f7e0ebe0e26`  
		Last Modified: Mon, 08 Jun 2026 19:31:23 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa5b436975885246a421ad2053810849a8886bd94493a69f490e5a229fbffb`  
		Last Modified: Mon, 08 Jun 2026 19:31:30 GMT  
		Size: 166.7 MB (166687343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:3df7d122806076f49930b03222b969a1165c86aafef8cdc61947924982d88c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4307143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe67b02f5196cc112f75db5a9399100462e5b3730106794dcedfb6f8ecc323cd`

```dockerfile
```

-	Layers:
	-	`sha256:98ead36a1547927f319270a566814dd745c2cadebc8b0401eb038b4d75664e7a`  
		Last Modified: Mon, 08 Jun 2026 19:31:23 GMT  
		Size: 4.3 MB (4285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96a63eb407f9274d2ea48e1418643f4f762064e4d000ab8d31cd786700043400`  
		Last Modified: Mon, 08 Jun 2026 19:31:23 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json
