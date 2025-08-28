## `neo4j:community`

```console
$ docker pull neo4j@sha256:cab98be4bb9ab340885a97f10bab54cf01f931acc63be5bac890304dd13ddec9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:38f7f4c74549b300e5bd40df425003a0fa38fec762f176e025f39ee5e75398aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391693028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa240094c218272d6ea0e436ac75a03bb6375ef409228ff2abb4bd0afbcf90f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cce5d0d88c05635692a8db86cde299861ff8fd71271e034fc633080bb09d9c59 NEO4J_TARBALL=neo4j-community-2025.08.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfac9c1cbfb0198f5c13fd51c7d26bb0f578c40884ade1a124ae2dd0fe42c37`  
		Last Modified: Thu, 28 Aug 2025 17:44:46 GMT  
		Size: 157.8 MB (157804778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a454f42f361cc83de86e4ce3b2aec9c3d5f4e1d32805a5a4098e84c13eb64696`  
		Last Modified: Thu, 28 Aug 2025 17:13:22 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae940aa536c3a16d6478c60b5fdcce515c4f59931d0e2f108b80b79fa4b0419`  
		Last Modified: Thu, 28 Aug 2025 17:13:25 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b303e8020a69d698df2207053242aaa8a13042c6c6a83d3677f2801017a8ec0a`  
		Last Modified: Thu, 28 Aug 2025 17:44:45 GMT  
		Size: 203.6 MB (203618239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:fd78a57183dd9f6c52d8a4d2910aa1be6d5e66d53fa84e96a05196d3a857a73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4624931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edac1ea014724ff2342314158d7454236e517b108626d9defc8a114f490e3970`

```dockerfile
```

-	Layers:
	-	`sha256:996f24a901351cbb8774dd23181e269cfeefd2788f3f420d040bcbe5934f27ca`  
		Last Modified: Thu, 28 Aug 2025 17:43:21 GMT  
		Size: 4.6 MB (4600822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:240bb0dd56574609730db90ce2b7fd8ba18201d87f994d11a2b442ee4602c785`  
		Last Modified: Thu, 28 Aug 2025 17:43:22 GMT  
		Size: 24.1 KB (24109 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2c918dd73a42f72f4cca787fb449b4fcd117cb1b00ab9ccfcf862045984897f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387708121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4cc1151e10cc82e18ef82bc5df747c805c888fd26603519af52c0dbd0e3f81`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cce5d0d88c05635692a8db86cde299861ff8fd71271e034fc633080bb09d9c59 NEO4J_TARBALL=neo4j-community-2025.08.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2018a747c37989de117c5255ed9b90797d04cc50b7b51efd380710484b6be5df`  
		Last Modified: Tue, 19 Aug 2025 02:32:37 GMT  
		Size: 156.1 MB (156081251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f56535870b273a74d9d898d997f71030909d63c13595b8461e881e0a9853628`  
		Last Modified: Thu, 28 Aug 2025 17:13:23 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0508e5c18f847c7ed70ef6b902f07baec5462de4eb5d34b9b39e68ce99e744f2`  
		Last Modified: Thu, 28 Aug 2025 17:13:27 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5ca2fa910e5f949a91737596ded94895ea31f7897aa1cebdc6f3682842341c`  
		Last Modified: Thu, 28 Aug 2025 17:46:22 GMT  
		Size: 202.9 MB (202862463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:623890de80bbe51f61d3d70e0fe63781777b1e4b843322fee4d4fa1cc6f1ad48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4599145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ac8a5dd0776da91a7087d27170f58023b320928d80d9237285e9432dec6b47`

```dockerfile
```

-	Layers:
	-	`sha256:d7c34195f3e74245feed86f34f900e1f20d8aef216bd586b95bed8f9a4eb15ea`  
		Last Modified: Thu, 28 Aug 2025 17:43:26 GMT  
		Size: 4.6 MB (4574747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d544d9751411ce421b6e8a978ccbbb34ac27f52cee16f0f9be56cb9321949d94`  
		Last Modified: Thu, 28 Aug 2025 17:43:27 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json
