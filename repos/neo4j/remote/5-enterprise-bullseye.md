## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:260a57988fcd808fadad0c9f565cc2c9e2a4313c6dad42b910101e559e650040
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d07c091e66652a26f3fe3039bb14a78ed5da23511841929bb2bc05ffa7a5c92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.1 MB (657088487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7b57999dd9cf72389ad23f404233173b58f0364e638b4de788f3a3e5ef41e3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 27 May 2025 16:09:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 16:09:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d9da8eaa1c3ee171c5d5cc91db0073bda883bc4412e44ccfe9afbd1aa0784329 NEO4J_TARBALL=neo4j-enterprise-5.26.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 27 May 2025 16:09:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.7-unix.tar.gz
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.7-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 27 May 2025 16:09:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.7-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 16:09:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 May 2025 16:09:55 GMT
VOLUME [/data /logs]
# Tue, 27 May 2025 16:09:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 27 May 2025 16:09:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 May 2025 16:09:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f9c226738c857bf709e0dd1cd2286e343ee4faa3183fcab1e92570ba89de5f`  
		Last Modified: Tue, 27 May 2025 20:45:59 GMT  
		Size: 144.6 MB (144634971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63802118e57fe37a22f9ad258a70d32e1884a4585ced927ee8fbd6224407833`  
		Last Modified: Tue, 27 May 2025 20:45:57 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5e2ef0f6b400b574842e92dd17e1696f4493ccff706f8c028bcc51e2aaa47`  
		Last Modified: Tue, 27 May 2025 20:45:57 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cebde7d931d24c60c77be02eba6707adbcb613d5ed5d65c12d914835509ccd`  
		Last Modified: Tue, 27 May 2025 20:46:04 GMT  
		Size: 482.2 MB (482183678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a7dc1c6cc937f718967736a4164b8edea313c9e88c3312a2a9ec15dcd34d183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4788239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9107d4df1727060c3c96d6a8da3b91e481456baa6b78fbf0f052f4cba080677c`

```dockerfile
```

-	Layers:
	-	`sha256:01382470456d533b4418bf59d3e515aa47a2134562981a9bf5093c9fc72f6b7e`  
		Last Modified: Tue, 27 May 2025 20:45:57 GMT  
		Size: 4.8 MB (4767226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f9bf2f1781dbb7d000efe71814b275588f028d6d92f32afd57f61f825fa9138`  
		Last Modified: Tue, 27 May 2025 20:45:57 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fd126d5a4089e76f54d94f011f9ec37b5a1fdff0b53a19587e5722cdcb2c405c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.9 MB (652917376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e64f071687a214ef024e71a9070747eacf4b64f0ecf838007c559fb2a4321c7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 27 May 2025 16:09:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 16:09:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d9da8eaa1c3ee171c5d5cc91db0073bda883bc4412e44ccfe9afbd1aa0784329 NEO4J_TARBALL=neo4j-enterprise-5.26.7-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 27 May 2025 16:09:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.7-unix.tar.gz
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.7-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 27 May 2025 16:09:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.7-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 16:09:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 May 2025 16:09:55 GMT
VOLUME [/data /logs]
# Tue, 27 May 2025 16:09:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 27 May 2025 16:09:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 May 2025 16:09:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d42e8bebe42abc72f8a99347a686e6bcc371f4b39b9d2f706177fdfa30ce72`  
		Last Modified: Tue, 27 May 2025 21:52:52 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231128c61c27f83a1657e4e95bbfefae51b9011ff06001db8db9950b350cf96f`  
		Last Modified: Tue, 27 May 2025 21:54:17 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010e631898c6cd68835bfde9f272053e31c31b0af0a1f292c580d5613d9c1c49`  
		Last Modified: Tue, 27 May 2025 21:54:18 GMT  
		Size: 10.0 KB (10025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457a6cb471fc242f3206ffb82423dbc629c47823de0f667c23707de9ed6e07b8`  
		Last Modified: Tue, 27 May 2025 21:54:28 GMT  
		Size: 480.6 MB (480644560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f8055d71ca66ea48653a5e88f95ddb13c88b48d13e4a176fb62fe8763a7ae2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4762213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef06c144c4476c1afc0e0b93b79dda2e60c0201a2f5d67c2f8ee0571a262eac`

```dockerfile
```

-	Layers:
	-	`sha256:cfe574a1707f7f42998746bb0b271f12acb1f23ddfbc3ee954065032d9a19864`  
		Last Modified: Tue, 27 May 2025 21:54:18 GMT  
		Size: 4.7 MB (4741031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b11066e7c10fe4bf5ae2707d165c5690c4ffb5ec94fcd951ff976c96896b17`  
		Last Modified: Tue, 27 May 2025 21:54:18 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json
