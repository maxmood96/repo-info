## `neo4j:community`

```console
$ docker pull neo4j@sha256:9654996cdc20865fe2f84b75730e66ad7ae6310290ad64dcdf9fe1a47a0e8ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:09650480dab502b2d889eb5461f55ed87317a36b639afc6fea27ea3cce1fedd6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364519074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fa14550df0336a082905b36ec3edae1c65d2685f98c262b80ca15af120ad7d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Aug 2022 19:47:31 GMT
COPY dir:075eb263f56e9eb4c32e827fd6ba780cefec0c30fd1905af231fac1048d9f24f in /opt/java/openjdk 
# Fri, 12 Aug 2022 19:47:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Aug 2022 19:47:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Fri, 12 Aug 2022 19:47:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 12 Aug 2022 19:47:34 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Fri, 12 Aug 2022 19:47:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 19:47:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Aug 2022 19:47:47 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Aug 2022 19:47:47 GMT
VOLUME [/data /logs]
# Fri, 12 Aug 2022 19:47:47 GMT
EXPOSE 7473 7474 7687
# Fri, 12 Aug 2022 19:47:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Aug 2022 19:47:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795d0152849607b73ed557da98f01f970a3654e4ef60a2d6d466beda4c93827d`  
		Last Modified: Fri, 12 Aug 2022 19:53:34 GMT  
		Size: 198.1 MB (198120799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55572ab03567f3f5021178e04c0f7e5c092fd8a6b867bcadea3d0c2348d0be2`  
		Last Modified: Fri, 12 Aug 2022 19:53:19 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e78b4184addec19f24de507d3706738fd66947777732bb8660bbdeaaaf98502`  
		Last Modified: Fri, 12 Aug 2022 19:53:18 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040827f03f1cbd0ef8ae24475bae00e881dc45f1577f8ba0c7adf871e3af068f`  
		Last Modified: Fri, 12 Aug 2022 19:53:26 GMT  
		Size: 135.0 MB (135020046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:846eb8f28f7d5c7ec3265ce027667782088226acc5cb9e66aa2cd5025e4ac1fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359811851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91348f64919a11c444d77517cde31af7baf44fe3b804a72fcb3b6e82cd3ad86`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Aug 2022 21:03:18 GMT
COPY dir:e5bd61f4facd9326f475d46e6508e132d506189701c632d2ef4b1f956f5e2ab5 in /opt/java/openjdk 
# Fri, 12 Aug 2022 21:03:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=869ecb89ce36fe457b4d4c4fcaa48fdf2f2d739c45323bd2c8ccdf09aa11abbf NEO4J_TARBALL=neo4j-community-4.4.10-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Aug 2022 21:03:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
# Fri, 12 Aug 2022 21:03:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 12 Aug 2022 21:03:22 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Fri, 12 Aug 2022 21:03:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.10-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Aug 2022 21:03:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Aug 2022 21:03:35 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Aug 2022 21:03:36 GMT
VOLUME [/data /logs]
# Fri, 12 Aug 2022 21:03:37 GMT
EXPOSE 7473 7474 7687
# Fri, 12 Aug 2022 21:03:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Aug 2022 21:03:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d549dc286e2ba114371af131cfc5d35e8d8ced543a24f43b254e61ecbb0862f`  
		Last Modified: Fri, 12 Aug 2022 21:08:01 GMT  
		Size: 194.9 MB (194869154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ac6cc891550167f52e8ecb281fb2513d4c389213e03ca92d924705d028fa2e`  
		Last Modified: Fri, 12 Aug 2022 21:07:44 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1ad341728aead5e5947e5aabb80f66a5c7a564592a584613027eac38b1f5d5`  
		Last Modified: Fri, 12 Aug 2022 21:07:43 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8012d7aed4c5b3ea015c7f3658d9fae1b92d648e563d871212fed2597fc605ba`  
		Last Modified: Fri, 12 Aug 2022 21:07:52 GMT  
		Size: 134.9 MB (134876975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
