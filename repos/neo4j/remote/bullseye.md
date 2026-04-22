## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:992187110a42b0f5351d4e613fbecf9585bdd9712a7665368b203f87fd4f8376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d4a0e51773ee1f01a01da5593a5449892353cd59cd3cfad710dbd90b3f8d8c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436471257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6186f21a2945e23401a95d352432d8b5fa2ff94fb5308de6207568ec0b7c3d4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:42:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:42:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 22 Apr 2026 01:42:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Wed, 22 Apr 2026 01:42:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 22 Apr 2026 01:42:53 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 22 Apr 2026 01:43:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 22 Apr 2026 01:43:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:43:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 22 Apr 2026 01:43:13 GMT
VOLUME [/data /logs]
# Wed, 22 Apr 2026 01:43:13 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 22 Apr 2026 01:43:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4c9ce8e1a0656f1c8356f6b5c9026c9818e85aa6a571d2df177fd2d08b2ad`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 157.9 MB (157857083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d32488e9111fa409b5a66aef8e3b1e72806291f5cd7fe0a713397cef298181`  
		Last Modified: Wed, 22 Apr 2026 01:43:36 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e161cc63b46d45e7fc32b4f424302786f9ddbca80363718afe2a9c674b50b3`  
		Last Modified: Wed, 22 Apr 2026 01:43:36 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ee554ee293978fc21cdec673ff3e5473c6ccb9c6183993958da883176ed34e`  
		Last Modified: Wed, 22 Apr 2026 01:43:48 GMT  
		Size: 248.3 MB (248342181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:31c3582ab24a06e11c15cd7717ac145d3369ad43b1c5e84f4e17ca30fcefe58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ff95603de11094d14203a57cc07735e8c49f5cab70382dfa0bef488d90712f`

```dockerfile
```

-	Layers:
	-	`sha256:3d8505372faf1c26d4acab057753eda3ccd86bd791e9753a737d2f74f7fcaf49`  
		Last Modified: Wed, 22 Apr 2026 01:43:36 GMT  
		Size: 4.6 MB (4584706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da5d3e620c60220a989d83d571fb58c15f26548ccd9da68d81bbf93e57a11f6e`  
		Last Modified: Wed, 22 Apr 2026 01:43:36 GMT  
		Size: 21.6 KB (21623 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ec22d662cdeb47e9c4dd193bb691c0ed8485fff2e632e99146b58dc50f0d5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432477349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56756a4619a587bd8ab0af9bdb83eaa2ae0424f4981ed7c432ffffa016779d7a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:45:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 22 Apr 2026 01:45:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Wed, 22 Apr 2026 01:45:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 22 Apr 2026 01:45:24 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 22 Apr 2026 01:45:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 22 Apr 2026 01:45:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:45:43 GMT
WORKDIR /var/lib/neo4j
# Wed, 22 Apr 2026 01:45:43 GMT
VOLUME [/data /logs]
# Wed, 22 Apr 2026 01:45:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 22 Apr 2026 01:45:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:45:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35289c7ac42c3715065ef6cfc99ccae4b7d42df3ff7a8c888684183ef024eaf2`  
		Last Modified: Wed, 22 Apr 2026 01:46:11 GMT  
		Size: 156.1 MB (156133028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fccf1555f4ed3d9a2da10347a0ad935fa30e97830f2c2ed134b86864a306bb3`  
		Last Modified: Wed, 22 Apr 2026 01:46:06 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ad2cf74126391fc201d4360ce6f4a9f4be48cc3461201b33bd192f8f81b260`  
		Last Modified: Wed, 22 Apr 2026 01:46:06 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442ea8f63c1d7e539c436ca0a3eade3e9f838c36ab6ce382b59c3284e84ddfe`  
		Last Modified: Wed, 22 Apr 2026 01:46:13 GMT  
		Size: 247.6 MB (247587722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:95f1b687ace0015556ca3be9269a7282d995eb69cd3042caca2a7d94e1832bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a29ac1651f1d110bb7abfb226dbc5bb9855a1b58af7f352407b3b61b26151d`

```dockerfile
```

-	Layers:
	-	`sha256:6d43fd65f23ee9b10b103d8607cc1c82b4b65688f9e66a7d4414419718308676`  
		Last Modified: Wed, 22 Apr 2026 01:46:06 GMT  
		Size: 4.6 MB (4558535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b370162b439f40f8d8d6bf2aadfa48b608cb9f10704cc7fec933ffccd06377`  
		Last Modified: Wed, 22 Apr 2026 01:46:06 GMT  
		Size: 21.8 KB (21817 bytes)  
		MIME: application/vnd.in-toto+json
