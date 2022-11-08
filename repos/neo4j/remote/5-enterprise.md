## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:9a4bcf00ee9014a9ff0b708a3c1030ecb09bb23d8d7522b5fe6f2b88a05fb7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:20b7411918a707659786a1a770d5c8c275565d85d0cada635fade57cf575ab83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430159743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75672eebe80dbbdaeaff4717d949e0277218793afaf2d8c655fc59634edb3c70`
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
# Mon, 07 Nov 2022 21:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:21 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:36 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:36 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:36 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:36 GMT
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
	-	`sha256:99e8565cfe49966c982867a5621e5eaf2dacc4051ede76f2d5fa1c05cc4663e8`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a8f35af07dcaed5768cc7f8c4ef833434b4cf18877f9b9b2b829dd76db0a6e`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bef8af0d744b267d17da627ab840c060bc69874505af56002b0e06e1e65abe`  
		Last Modified: Mon, 07 Nov 2022 21:43:55 GMT  
		Size: 206.3 MB (206296947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:63b00a9e963c031cad10716e42ac91ba44aa05241d49480b00ad6a9ee3b9c1c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427444123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58c75c545a73f3f586b558acda7045154e84771fd0182d6754c6440d00d025`
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
# Mon, 07 Nov 2022 21:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:36 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:54 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:54 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:54 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:54 GMT
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
	-	`sha256:9a178c84172e1ce76780f08f6343145c0bcdc38eec775c69b6637fcb0be1d393`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61a5e1cbd196598c089048696990a1e5f2c180f24cb8c95a97eecfbfc538831`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 7.6 KB (7629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084b6431edc5985ae0e1d28b4a14112bd2c2b910312a545f0e41991d94b9ab06`  
		Last Modified: Mon, 07 Nov 2022 21:40:57 GMT  
		Size: 206.2 MB (206153470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
