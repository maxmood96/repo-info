## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:3c124b7aa87fceab197855f6322cd90cf46ccd963643c0bf7060c8d110f6b0b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:83f60aaf60698a9a79ddeb436ff0e2b1488ac3de2e92576da3600d9da4375b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304209755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfde9e154a491e51cc8961406e91756544fe1e035af8d18e8e15763f48ac0f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 13:55:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 13:55:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=80ae623641a3b353e3b2bca5e49cb6f0dbb79d89d512850c751c356a1378c444 NEO4J_TARBALL=neo4j-community-5.22.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 23 Jul 2024 13:55:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 13:55:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Jul 2024 13:55:16 GMT
VOLUME [/data /logs]
# Tue, 23 Jul 2024 13:55:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 23 Jul 2024 13:55:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93434bba57c4205f8008506bc59dff4f894a61f081a138f9fa8fe4540c3ff07c`  
		Last Modified: Tue, 23 Jul 2024 18:14:11 GMT  
		Size: 145.2 MB (145166533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a7b513e7443aa7b2fd1c8634ff4e2518bf57e76a61f9e3726fd617791de33`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bab337b0425aacf8de629d1f4b3360333778d6140b39012c458160ad00aab92`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fc1b4f9dd9ac8d83be8eb39b9d91e393e420d3dd0d78189f9de5279236dbc4`  
		Last Modified: Tue, 23 Jul 2024 18:14:11 GMT  
		Size: 127.6 MB (127601396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9cb74f837092c86ea4b29b7d3d8bd5c58501c0ceb231b4f3c843dc7aa9bd5536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3051076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5956a48deb42e2c602300606738f55f2a23ce7d9374e0868d12748039cbf9f2`

```dockerfile
```

-	Layers:
	-	`sha256:113f48a05fedc4931b81a98954546d75171d43adca9932d14833aa331ca25dd8`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 3.0 MB (3027693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14258504adddaa8864a03edfef82cfac390b4581f6be8777aaa86cd84c573ad2`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 23.4 KB (23383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

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

### `neo4j:bullseye` - unknown; unknown

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
