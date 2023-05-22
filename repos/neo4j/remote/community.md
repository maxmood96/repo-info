## `neo4j:community`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
