## `neo4j:5-enterprise-trixie`

```console
$ docker pull neo4j@sha256:1eca3bdeb70de307408bedba5d431a03bca7025c39b2667f276507c911ba026e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:c14ee99c402a77e6ffc44c1356c64acdbf9316dd5839abbafed1ae5f98704e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.1 MB (684144669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace61411756a188b1e819b82f6eb57ec60d018359fe27c19ec0661dd0a2fc62d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 23 Jan 2026 22:00:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 22:00:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Jan 2026 22:00:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b23f47fd5d1d1b22a4779fb05c39d7dfe2c1997654be75ecf3faab74fcda5121 NEO4J_TARBALL=neo4j-enterprise-5.26.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 23 Jan 2026 22:00:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
# Fri, 23 Jan 2026 22:00:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Jan 2026 22:00:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       adduser curl ca-certificates gcc libc-dev git jq make procps tini wget     && addgroup --gid 7474 --system neo4j     && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Jan 2026 22:00:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 22:00:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Jan 2026 22:00:46 GMT
VOLUME [/data /logs]
# Fri, 23 Jan 2026 22:00:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Jan 2026 22:00:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Jan 2026 22:00:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445c29526c92dc2bfeae831a13493455b84154782132daf67035415593aa71bc`  
		Last Modified: Fri, 23 Jan 2026 22:01:26 GMT  
		Size: 157.8 MB (157826034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df981e448e365194cade2a8f1c694d530b81ffc12ab5a4a3dbc605adc5dd188`  
		Last Modified: Fri, 23 Jan 2026 22:01:16 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c551467539df43ec080ba5f2005a695faaf8bc0810409a9326d27661b44293d`  
		Last Modified: Fri, 23 Jan 2026 22:01:30 GMT  
		Size: 496.5 MB (496534855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:907483ef856ea84bf42b36d86ab21370075150f22b6da7e753f1e7840c3c4aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a8e315420c7b7e49a1ab2cc2422c793abf048963e5f86f4d89981365ffcc40`

```dockerfile
```

-	Layers:
	-	`sha256:e522a3768798adc28d99427a5e859219dd8c66742a4aec80349e2f4313b76105`  
		Last Modified: Fri, 23 Jan 2026 22:01:16 GMT  
		Size: 4.7 MB (4668892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e85d28d1ee454974140c3fcf9cfc968e57c07bec49139a7e9217e3e5b70c69`  
		Last Modified: Fri, 23 Jan 2026 22:01:16 GMT  
		Size: 19.3 KB (19325 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7e9fd215d8c51dc77597aa0cb3eaf7bde56fc1438b01f985d80b6b07d9144154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.9 MB (681854664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7ccf4ee2109646b357c88b83b91a1e8058a2511318cf383a0f8f882cb69d71`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 23 Jan 2026 22:00:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 22:00:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Jan 2026 22:00:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b23f47fd5d1d1b22a4779fb05c39d7dfe2c1997654be75ecf3faab74fcda5121 NEO4J_TARBALL=neo4j-enterprise-5.26.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 23 Jan 2026 22:00:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
# Fri, 23 Jan 2026 22:00:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Jan 2026 22:00:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       adduser curl ca-certificates gcc libc-dev git jq make procps tini wget     && addgroup --gid 7474 --system neo4j     && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Jan 2026 22:00:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 22:00:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Jan 2026 22:00:46 GMT
VOLUME [/data /logs]
# Fri, 23 Jan 2026 22:00:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Jan 2026 22:00:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Jan 2026 22:00:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2cc7e8f46fd697b863d92a1faeab5e79a8748a4086efce3f984e33be806045`  
		Last Modified: Fri, 23 Jan 2026 22:01:22 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3149bd08a7db495478f6969897740f46415652118e7e35e9de21a6e4243cbead`  
		Last Modified: Fri, 23 Jan 2026 22:01:17 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3226a66d9c6e24a0574f58a88ddf2c53bdc3ba14c1fb4b90da4fe317f54e946d`  
		Last Modified: Fri, 23 Jan 2026 22:01:29 GMT  
		Size: 495.6 MB (495602951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:d2085d744cb6bd8cd2b5a3c8976b7b94a4108693f99ca37ea6955a5f29636cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4682825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feafbaf274869232f628ee7d04fa728402f84eb4b218320ed831eca5a8df546`

```dockerfile
```

-	Layers:
	-	`sha256:208a8a240e56630c66c8802edd533e1647e1335998ef468e9c94b9e43b27b183`  
		Last Modified: Fri, 23 Jan 2026 22:01:17 GMT  
		Size: 4.7 MB (4663346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6bfe3925c871e2cfbdc4f59880d36a00a9124c7373c26eb6c3337821f3fbf5d`  
		Last Modified: Fri, 23 Jan 2026 22:01:17 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json
