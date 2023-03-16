## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:22eaf8585a13f194a98fb0c3c2f72c768ecfa407f64b66eecffdd13d6f8f29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b750d556c7fe46bf7dfe565932b45cedaca08d5dda3b3a3e595b4f8bfd487fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b70e78aaa852faa9322df16912659d74ca3250c737ebde9ecab3b47a4a19386`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:09:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:04 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:09:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:20 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:21 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7faf1cbaba3044a9068d65a3c0498e7c0d66c9bc7e077f1fcbec60e1e7c503c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6cbd2a8118028bb60557929266606feb4ec4e9f26a1fb4ac99cce58c4a366c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e24e0d4bf82b601ff7f0b08e4b72740d466a4d5708817c835aa05195c099e`  
		Last Modified: Thu, 16 Mar 2023 07:11:11 GMT  
		Size: 320.1 MB (320124347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5b9642a46beda383b5c4b2e0cd2e1287ea9d382a1a66348cdc348669d8071bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87106aebfd70f8607a883d41014e4acf1a38e41e880c7950669d12c4f06dc044`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:42 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:12:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:05 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:05 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debdc6e583e4d9de905be35df35f7f4e359b68b391bcb09f5996693245fe1276`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884476f2fa28819c14f1cbcecb95388dc5302248c67f2c2b56bb5bc50586bfed`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 8.4 KB (8420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2503db9ba63adcd504c01a50e7dfbe87d3e1822cbbd258e8a631d43ed2c6d908`  
		Last Modified: Thu, 16 Mar 2023 06:13:40 GMT  
		Size: 320.0 MB (319982031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
