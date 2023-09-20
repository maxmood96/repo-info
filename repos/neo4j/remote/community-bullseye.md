## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:bbd59bda3caa870c94e547f8790410f676ae2b6ea92a0c4002eebc0a8bb33252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:dc497d0de22522c0b1e1e3e874e7df4c876587d5ae13ce2266b1964c0a6d7016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292665190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f63c85a7b03e25228be9f24de1030063761e345233193a453837937a5397aab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 02:03:47 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Thu, 14 Sep 2023 21:20:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=adf9e7915f5c10dfa4daf9eab79852660887eac3c3e165741fce48415c0b6f34 NEO4J_TARBALL=neo4j-community-5.12.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 14 Sep 2023 21:20:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
# Thu, 14 Sep 2023 21:20:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 14 Sep 2023 21:20:10 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Thu, 14 Sep 2023 21:20:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 14 Sep 2023 21:20:23 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Sep 2023 21:20:23 GMT
WORKDIR /var/lib/neo4j
# Thu, 14 Sep 2023 21:20:23 GMT
VOLUME [/data /logs]
# Thu, 14 Sep 2023 21:20:23 GMT
EXPOSE 7473 7474 7687
# Thu, 14 Sep 2023 21:20:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 14 Sep 2023 21:20:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732d09690feda2ec5aced0543a2cf8ee1aadf1e05dd333f551cc4b11eaa287a0`  
		Last Modified: Thu, 07 Sep 2023 02:06:03 GMT  
		Size: 144.8 MB (144775798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d734d2deca94a63896944f62629cffc9c69bac985aedb4b08fb3736c767377ad`  
		Last Modified: Thu, 14 Sep 2023 21:21:55 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595ac29574a2a198c6f5c01263cff98202cb4cd88d163d493b10bd232f4a3e50`  
		Last Modified: Thu, 14 Sep 2023 21:21:55 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c1c9a6bed0e54128889e4f6101b56bad707140ac1e2d0ab666f3bb4f09286e`  
		Last Modified: Thu, 14 Sep 2023 21:22:01 GMT  
		Size: 116.5 MB (116458603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d9265c09666e60cf5f0b9ce0101a365889bc093b12abce1a27b206dcb464f83f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289971148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcea1525f815efaf1979fd3ed385fb066c3bf27b9f589d5f21f9732eaf7461ff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:48:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 09:53:09 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Wed, 20 Sep 2023 12:41:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=adf9e7915f5c10dfa4daf9eab79852660887eac3c3e165741fce48415c0b6f34 NEO4J_TARBALL=neo4j-community-5.12.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 20 Sep 2023 12:41:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
# Wed, 20 Sep 2023 12:41:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 20 Sep 2023 12:41:28 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Wed, 20 Sep 2023 12:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:41:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 12:41:39 GMT
WORKDIR /var/lib/neo4j
# Wed, 20 Sep 2023 12:41:39 GMT
VOLUME [/data /logs]
# Wed, 20 Sep 2023 12:41:39 GMT
EXPOSE 7473 7474 7687
# Wed, 20 Sep 2023 12:41:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 12:41:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603608103e3f4f9bafbfe00174b3aa6d67a38d93136e7e6343f0b5b25ffa8ace`  
		Last Modified: Wed, 20 Sep 2023 10:01:18 GMT  
		Size: 143.5 MB (143543516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff0a5f6e18f53c951201a12c4c0932facf9d9c85d3eda4ce6ef392547570374`  
		Last Modified: Wed, 20 Sep 2023 12:43:08 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889e1ec910ff9a1f31c0ef4b5e54ad0f49079b72f8055d45b7229412e1c30c06`  
		Last Modified: Wed, 20 Sep 2023 12:43:08 GMT  
		Size: 9.4 KB (9430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460216cffb0711592181789f40eaf7ac0f3c9d761590f83a3089e836d876694f`  
		Last Modified: Wed, 20 Sep 2023 12:43:13 GMT  
		Size: 116.4 MB (116351448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
