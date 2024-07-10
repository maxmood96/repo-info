## `neo4j:community`

```console
$ docker pull neo4j@sha256:fd01c22d482011718d40120796204226ff555bbe14a1060519c862acd94f4670
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:4b3d549fbbd7dc7f89b0af1af92e7465190f3af90e0b341a12666ed49c755152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306433016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb38f907578710825c5fb8ab669e80910b3403a71339ae4d6c070cd05e41b2b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eea688fdf9a0e14a6d4ff4fecf2f721d2a04a59bdc53ca66fa84664d86fd13`  
		Last Modified: Tue, 09 Jul 2024 18:58:59 GMT  
		Size: 145.1 MB (145095096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86506e8982365aafadd6dc12571e80379312e2fb7fa3d3c0aae9df92ed5143e`  
		Last Modified: Tue, 09 Jul 2024 18:58:55 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1f1c57951240050ec69bb62d15f1c33cb2e2388837fc5a7d2b67213f4b0406`  
		Last Modified: Tue, 09 Jul 2024 18:58:55 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8175693595cc97ceab566869e18d6e93eac708b8145e6eff262e9eac6a91deb`  
		Last Modified: Tue, 09 Jul 2024 18:58:59 GMT  
		Size: 129.9 MB (129902140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c027119a2dc90e2bd02334101b23d51a4040a98840cd01769514f524a9ebbd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02c816cf8e859eef5cdba4fe29ee7748d3b9ab095248f06878d92d3eca0a30f`

```dockerfile
```

-	Layers:
	-	`sha256:2298997c9a38a5d626c9e6c1df7915b2313c2bd3d23cf40819ce2cf41e46090f`  
		Last Modified: Tue, 09 Jul 2024 18:58:56 GMT  
		Size: 3.0 MB (2967835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bd69bb17525edc81d4799453f1960c3b93ebe217bbbd245c5453b549f823f5`  
		Last Modified: Tue, 09 Jul 2024 18:58:55 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json
