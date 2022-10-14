## `neo4j:latest`

```console
$ docker pull neo4j@sha256:b8bd93e9a9256c24e89d57299cf37a2f890b463a981eec8d4e8b5e621a874e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:17334cbc668d852ca8a3d8590f66c4fda64d9c7de7d93cc62803f534ae7dbce6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364700569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ae5bfb75495d129630107d1dc2ff2fac5a5988315c7c0383ba4a448632e78b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:19:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:19:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:19:59 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:20:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:20:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:20:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:20:12 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:20:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:20:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:20:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaaaf8954c2ff61e744735d2032871d4080c8bed1b8c878313d64c2dac07254`  
		Last Modified: Fri, 14 Oct 2022 21:22:29 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7c1680a7fe090ca41b7fffbd63d3a951f0e80c76f43334f336ba552d885eb0`  
		Last Modified: Fri, 14 Oct 2022 21:22:28 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a0126ab25e546fa6b2fb0f68c2737627f4dee15f96c92b4bea749a07d0f91e`  
		Last Modified: Fri, 14 Oct 2022 21:22:35 GMT  
		Size: 135.1 MB (135144015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15aabe0a070a165e52ae3bf8781bcbdc6588ee4935f0a5c0c544f3da3301d743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359736471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530ec3c2144ed1ade06f96a81979f7ecbb3c8383fcce46c162cd38e94284faa5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:40:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:40:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:40:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:40:46 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:40:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:40:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:40:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:40:59 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:41:00 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:41:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:41:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9484df044d656b445873a7daa65c765f30d6896c583418086772c0d902a5b94`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885002c3309b298661a5b4a76d61e67ff3c385070fedb22692774343f3c93e2c`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eca9d5d225cef9f0d9f1bec2a18e72eebd5e333f79e022b3f31a4f6bf8e2f50`  
		Last Modified: Fri, 14 Oct 2022 21:42:52 GMT  
		Size: 134.8 MB (134794066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
