## `neo4j:latest`

```console
$ docker pull neo4j@sha256:940f32f66324801848793fe3ec4e6163861f522cc7aa05cbebbc5324f6eb3268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:a7a2b1a6e992771b405cf3b53b634a2b8c547756279799ba13baeacb328e33df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304207821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468584de930e2da70f06a23c9faa19fe85c14b18cca4ac6b2c888fe9d7d7578e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jul 2024 13:55:16 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 23 Jul 2024 13:55:16 GMT
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd9d4bab84b0b1cd5dc103a0740ac97bd4fbe0c9de868a1dbe7976db9e13f7`  
		Last Modified: Sat, 17 Aug 2024 02:05:37 GMT  
		Size: 145.2 MB (145164838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bb0b3060bc9a6a8654da55c4cf08a082cb440fba001c46cc4dd2f146d6f3ea`  
		Last Modified: Sat, 17 Aug 2024 02:05:35 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0da549cf5517894fc68dbd0642841211c14d147aa75a75ef50303d5982a8be`  
		Last Modified: Sat, 17 Aug 2024 02:05:35 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2876123263e268f56a748d291fdab7bed0a693a77882ab0471d9b6a11950df`  
		Last Modified: Sat, 17 Aug 2024 02:05:37 GMT  
		Size: 127.6 MB (127601205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:27d7299c327aebf3b777d0381458376d7c0349f0d3a12e354b84a21a13bfec83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3051076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0113a7e4bff4958dcb979f878e53dfac7f2f1d97a66d7fa0cf4d21b037cf0d33`

```dockerfile
```

-	Layers:
	-	`sha256:e9308f8eedcf45e1c236486dd7222c2a2ffaab1c35593a518ac7856ec5c90d99`  
		Last Modified: Sat, 17 Aug 2024 02:05:35 GMT  
		Size: 3.0 MB (3027693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e230dc0cc05c04afffe3bb1f009c2ac2db606c979548a6df1674a8ed97c6ca`  
		Last Modified: Sat, 17 Aug 2024 02:05:35 GMT  
		Size: 23.4 KB (23383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46f7a177ef84a6ac347c5b2941a1890aaaece610670d1535330bb29cc23d1f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301614142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7eb257d9905db3850a6754bd3ad2abc556df2347002526b98ef2a541be6da12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jul 2024 13:55:16 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 23 Jul 2024 13:55:16 GMT
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e77718461fce3137ffc528beac77db0246cb0b5c93b3e3b0fe3e760c7ec7414`  
		Last Modified: Tue, 13 Aug 2024 06:33:53 GMT  
		Size: 144.0 MB (143959484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611900f477b0467c34c47b676a9f28b41742b424b5f5a5a837b6983455777e23`  
		Last Modified: Tue, 13 Aug 2024 07:35:18 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7759ecbf36a3d965a47b051a7d95fac275c4b528f371680f8ea7daa299e8c6af`  
		Last Modified: Tue, 13 Aug 2024 07:35:18 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661bd42eb01d39bac67fcaf268d1aeb3802646a29b8329c9736ba57538f1dc2`  
		Last Modified: Tue, 13 Aug 2024 07:35:21 GMT  
		Size: 127.6 MB (127565048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:47e23eaa340ba53155e6eb4637c98a35751f83b83acc31384acb8656f69af2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbc64bb3485bdf561cdc70c121adef38e385e4bf53b2a21e890c70bedef5d69`

```dockerfile
```

-	Layers:
	-	`sha256:8a832733b5608ffe33aa502acd84a690a0daaa0126b2f88b392293413501deca`  
		Last Modified: Tue, 13 Aug 2024 07:35:18 GMT  
		Size: 3.0 MB (3028100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86104115a370856a1693ba6bfc614db829b02969f34f2795c101f53abc9687b3`  
		Last Modified: Tue, 13 Aug 2024 07:35:18 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json
