## `neo4j:community`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
