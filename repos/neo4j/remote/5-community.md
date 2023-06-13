## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:3bf8dbbda1ef52063693b245c06bf5e9d2768195f082b1b1aed9933475470540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:dc272726680f27f10425e6697cc405103478e358968976515aadfa11b319cbd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338698875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad022bbe615bdf0661ab86f40e73af636e0c6e870e3c60d844b9562397fbefc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jun 2023 03:50:15 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Tue, 13 Jun 2023 07:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Jun 2023 07:09:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 13 Jun 2023 07:09:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Jun 2023 07:09:02 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Tue, 13 Jun 2023 07:09:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 07:09:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 07:09:15 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Jun 2023 07:09:15 GMT
VOLUME [/data /logs]
# Tue, 13 Jun 2023 07:09:15 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Jun 2023 07:09:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 07:09:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bb32e3062db1c890af593910b7980b172f50d98a42b947310bdadd85c41440`  
		Last Modified: Tue, 13 Jun 2023 03:59:06 GMT  
		Size: 192.6 MB (192580388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134a37330edefa0a033fee2d31970e964caeab4aa96bb417e63fb3c0a8e14c`  
		Last Modified: Tue, 13 Jun 2023 07:10:29 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a384b9f2bbf845f7870bc14fa917d7af3ee40d6142a2610c7ed042beb35caaab`  
		Last Modified: Tue, 13 Jun 2023 07:10:29 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cca560702bb0d53e76d67b7c780c1a7a368d00966c9fd3074d917380e1fd11`  
		Last Modified: Tue, 13 Jun 2023 07:10:35 GMT  
		Size: 114.7 MB (114688458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7dd07e2a806fc23110252785bf391d326ae3302b5398dbddace99dd805c6c16b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (336008316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e89cfbba3028caa9c5f7c9e882d0e9b7e5c040d9299cde2c1f91b23816d1191`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jun 2023 04:28:50 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Tue, 13 Jun 2023 04:28:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 13 Jun 2023 04:28:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 13 Jun 2023 04:28:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 13 Jun 2023 04:28:55 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Tue, 13 Jun 2023 04:29:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:29:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:29:07 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Jun 2023 04:29:07 GMT
VOLUME [/data /logs]
# Tue, 13 Jun 2023 04:29:07 GMT
EXPOSE 7473 7474 7687
# Tue, 13 Jun 2023 04:29:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Jun 2023 04:29:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f1d77eefd6a268a661d8baa5ffc1f6d77b6b4e27e034496d0fb5928e86485`  
		Last Modified: Tue, 13 Jun 2023 04:30:57 GMT  
		Size: 191.4 MB (191387706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0a981bd793b3c89ab46f2f6bd1114add130d3116491701e31f0d53f8f12fc7`  
		Last Modified: Tue, 13 Jun 2023 04:30:41 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b539f80e3d71c865200143adaa99ddd5e103f310fe461b2b53d6eaab5e022a22`  
		Last Modified: Tue, 13 Jun 2023 04:30:41 GMT  
		Size: 8.8 KB (8770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ace878b15edfb608ab92fa81107f69cd2c890e1eaec38702cc19dc7a59a74d`  
		Last Modified: Tue, 13 Jun 2023 04:30:46 GMT  
		Size: 114.5 MB (114545124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
