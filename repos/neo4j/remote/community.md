## `neo4j:community`

```console
$ docker pull neo4j@sha256:f88f9176940a6db1ea298102a0991359e529089b565e59afda910d2e6e842116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:79ea371edf6e9673c5508eff4a3f1bd82bd24a9b245972de73a2fe7ab025a3e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341583649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec142860f24c22c0e0d2729a0d227aaf92830bd888f31bfd3e961f60e716368`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:58 GMT
ADD file:bd80a4461150784e5f2f5a1faa720cc347ad3e30ee0969adbfad574c316f5aef in / 
# Tue, 04 Jul 2023 01:19:58 GMT
CMD ["bash"]
# Wed, 19 Jul 2023 20:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Jul 2023 20:42:13 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 19 Jul 2023 20:42:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2bbf7257481874b0f4b025d0344f81fe972bba1f20fd18e3eb8840ff04ad1b33 NEO4J_TARBALL=neo4j-community-5.10.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 19 Jul 2023 20:42:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
# Wed, 19 Jul 2023 20:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 19 Jul 2023 20:42:15 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 19 Jul 2023 20:42:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Jul 2023 20:42:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jul 2023 20:42:35 GMT
WORKDIR /var/lib/neo4j
# Wed, 19 Jul 2023 20:42:35 GMT
VOLUME [/data /logs]
# Wed, 19 Jul 2023 20:42:35 GMT
EXPOSE 7473 7474 7687
# Wed, 19 Jul 2023 20:42:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 19 Jul 2023 20:42:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:faef57eae888cbe4a5613eca6741b5e48d768b83f6088858aee9a5a2834f8151`  
		Last Modified: Tue, 04 Jul 2023 01:25:03 GMT  
		Size: 29.1 MB (29124829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef95bdc735d909eaee3e2c5c5072bf884101807a69a15402bee83aab9a13f4`  
		Last Modified: Wed, 19 Jul 2023 20:43:50 GMT  
		Size: 192.6 MB (192580400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a2003ccc9bff898d52197b197450e5f9d299a5ac61a1f2b0c8617031eb2ea9`  
		Last Modified: Wed, 19 Jul 2023 20:43:36 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b030f8fa6fcb4d46cee2540085eea25d237d613ebfb3d601299360b0e906f40a`  
		Last Modified: Wed, 19 Jul 2023 20:43:36 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb71c33bfc11d85c4a4e2a6f0999cf8af96169719c624f9c5a21d16c7f2860b`  
		Last Modified: Wed, 19 Jul 2023 20:43:43 GMT  
		Size: 119.9 MB (119867913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d3f2aa0ec36aafe9ce19fe7dbeb55cd93e3296718ff9cb9a9402fdb7510a79fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d96d1eec2fae614a8255e75368bd66bc617967f6ec6ea022634ce4e9e1a197b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:39:58 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Wed, 05 Jul 2023 04:25:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 05 Jul 2023 04:25:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Wed, 05 Jul 2023 04:25:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 05 Jul 2023 04:25:09 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Wed, 05 Jul 2023 04:25:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 04:25:23 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 04:25:23 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Jul 2023 04:25:23 GMT
VOLUME [/data /logs]
# Wed, 05 Jul 2023 04:25:23 GMT
EXPOSE 7473 7474 7687
# Wed, 05 Jul 2023 04:25:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Jul 2023 04:25:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a44711a84ae8605b1c1f0f04cf29732536ca2ecfae7b5a7b10134f3584ec4`  
		Last Modified: Wed, 05 Jul 2023 03:49:53 GMT  
		Size: 191.4 MB (191387679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab1c2b58763ccbe51ba678e3d904b0365c7b6d7fa043c0aaebb98f1b365d08c`  
		Last Modified: Wed, 05 Jul 2023 04:26:35 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32971c8b8616ea434510c51dd1881c3b5549cb2af293a2b6015c7bae5a66a9ab`  
		Last Modified: Wed, 05 Jul 2023 04:26:35 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcbaf761ab2b873809a90f00820b0e855c2672f4bf6740f4a25db4277d0fa11`  
		Last Modified: Wed, 05 Jul 2023 04:26:40 GMT  
		Size: 115.6 MB (115646257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
