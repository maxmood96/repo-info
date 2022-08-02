## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:c2b4d83d6e8b95ce74467337cad041e520e25994e3dbefeb46922845c4978877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:f5cf0e31ab8dc79d439793b822b1371441e9b30d8a0888771386d6f6637acc66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.0 MB (452979686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c5920b07b6853c937adf4512cc447b9d2b18d62dbc1c2f514ca45279651ea2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 05:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Aug 2022 05:03:09 GMT
COPY dir:8e4cdecb3cdc4d9fbf51ae71d2e79970572b7cb5b1e1415971a1386a1e1490dd in /opt/java/openjdk 
# Tue, 02 Aug 2022 05:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=747b2e71b273d8f0dd82cdb594aca02b87f03f445d2ee5eaba561c8ebd474bb0 NEO4J_TARBALL=neo4j-enterprise-4.4.9-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 02 Aug 2022 05:03:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
# Tue, 02 Aug 2022 05:03:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 02 Aug 2022 05:03:30 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 02 Aug 2022 05:03:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 05:03:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 05:03:45 GMT
WORKDIR /var/lib/neo4j
# Tue, 02 Aug 2022 05:03:45 GMT
VOLUME [/data /logs]
# Tue, 02 Aug 2022 05:03:45 GMT
EXPOSE 7473 7474 7687
# Tue, 02 Aug 2022 05:03:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 05:03:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f69b2146feda330dc1ff54a2a42008d3b55ba602058dd074608359fa171808`  
		Last Modified: Tue, 02 Aug 2022 05:07:47 GMT  
		Size: 194.6 MB (194596362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b97f0739fe84a79452b3e725edb8f28e0e5111188c7917230a04f98bab0bf6e`  
		Last Modified: Tue, 02 Aug 2022 05:08:06 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abb9019354dea47cc75f0a566e14fd11fa8fd35348a49ef7b994250dbeced00`  
		Last Modified: Tue, 02 Aug 2022 05:08:05 GMT  
		Size: 7.6 KB (7611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d2ff1d4d354a7e75238ac6cff079bc2f0b8d80b7c335c8373bb78c098625f3`  
		Last Modified: Tue, 02 Aug 2022 05:08:17 GMT  
		Size: 227.0 MB (227005099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5e0898da0f9bfd329b35878258b4c7d1edd2860a5132dbc7c57b257b6e631c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.3 MB (448276372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f933749c9e3ee0545c5b221e27a316e90bb8862544f16afa3ca59971fbfa33e4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Aug 2022 04:00:50 GMT
COPY dir:b0f8583e007c797668d2e0da85819a94225394d53d1cae6c9b8c1a07b83c1575 in /opt/java/openjdk 
# Tue, 02 Aug 2022 04:01:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=747b2e71b273d8f0dd82cdb594aca02b87f03f445d2ee5eaba561c8ebd474bb0 NEO4J_TARBALL=neo4j-enterprise-4.4.9-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 02 Aug 2022 04:01:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
# Tue, 02 Aug 2022 04:01:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 02 Aug 2022 04:01:22 GMT
COPY multi:3374c8dc0747f37551a88a28b1d77a933ccfa81a6b8258bf2e495e2876116c57 in /startup/ 
# Tue, 02 Aug 2022 04:01:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.9-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:01:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:01:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 02 Aug 2022 04:01:38 GMT
VOLUME [/data /logs]
# Tue, 02 Aug 2022 04:01:39 GMT
EXPOSE 7473 7474 7687
# Tue, 02 Aug 2022 04:01:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:01:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd713a67f483328f18d8b3046ef66e19393a23d1e10c0348bea711ac5a51874`  
		Last Modified: Tue, 02 Aug 2022 04:04:19 GMT  
		Size: 191.3 MB (191349043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00490db0a901a5acc34a375ff96a73b6a6e46feb96ae2df226b4c3613581dce`  
		Last Modified: Tue, 02 Aug 2022 04:04:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e154a4a99c1a25a424c59c85319056708c29a4b300192c86701cd94e039252`  
		Last Modified: Tue, 02 Aug 2022 04:04:42 GMT  
		Size: 7.6 KB (7586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088290c2a217c43d5409c613eeba4304410404ddd38a4fa95f221817efa34e90`  
		Last Modified: Tue, 02 Aug 2022 04:04:56 GMT  
		Size: 226.9 MB (226861603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
