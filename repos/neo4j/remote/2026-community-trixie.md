## `neo4j:2026-community-trixie`

```console
$ docker pull neo4j@sha256:2b5c5f3f5bf9c948f52756cff2388a7eef21bc0377da378709f2cdf8222ff418
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-community-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:1789cefafe1c6ed14879cd069904cabf8e2470cd823cec3329a24d038b546780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341393005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a72197e1185962b60778668e3b5e784df1c9e3bdbfa591943a91a997de2f7c2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 10 Feb 2026 19:17:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Feb 2026 19:17:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Feb 2026 19:17:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Feb 2026 19:17:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 10 Feb 2026 19:17:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Feb 2026 19:18:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Feb 2026 19:18:26 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:18:26 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Feb 2026 19:18:26 GMT
VOLUME [/data /logs]
# Tue, 10 Feb 2026 19:18:26 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Feb 2026 19:18:26 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:18:26 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b802e268dad8782b8f8c17f3f8f76902a7a22ad19d8e4b7f6692c34556bb40c3`  
		Last Modified: Tue, 10 Feb 2026 19:18:50 GMT  
		Size: 92.3 MB (92256248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2f1c6e7b194e0494274909c2518227c527c5c439546b7fa80735910c6d9d33`  
		Last Modified: Tue, 10 Feb 2026 19:18:47 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd6f84aa8ae63fd30488fbec49b0481dd639b64a4889850a80571b58070d52`  
		Last Modified: Tue, 10 Feb 2026 19:18:53 GMT  
		Size: 219.3 MB (219348108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:b50169e761e2bd1fd70700fcbabe87f63e4da8943a616a4da9f307c3c12edb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54c7164dd7e1360f84c03f06e520457330895814b6ea443db5fd15674a8ffc7`

```dockerfile
```

-	Layers:
	-	`sha256:ece4190c3c4b47470f6390acfa33cdfc8e29475d0062157bb8e6ae5f0fcbb9e3`  
		Last Modified: Tue, 10 Feb 2026 19:18:47 GMT  
		Size: 4.4 MB (4387410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f482563dc3ce5d50f9bd5e6011e20032573015d24d2bf879847c9555350c82`  
		Last Modified: Tue, 10 Feb 2026 19:18:47 GMT  
		Size: 22.4 KB (22355 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-community-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9b827f18eba3515ea9c5aaa4b289a8e3c006d1e5ddcce7ab093864381e06d375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339856469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c3fe10f07746f99b654ce56b23bd5a0458d569647523836d9134b2f6e3b7a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 10 Feb 2026 19:18:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Feb 2026 19:18:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Feb 2026 19:18:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Feb 2026 19:18:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 10 Feb 2026 19:18:54 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Feb 2026 19:19:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Feb 2026 19:19:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:19:17 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Feb 2026 19:19:17 GMT
VOLUME [/data /logs]
# Tue, 10 Feb 2026 19:19:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Feb 2026 19:19:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:19:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bdc76ad995f9fc49bb14c8fd1ad7b0dbe70c88effbc59c863e0edaf330e2a1`  
		Last Modified: Tue, 10 Feb 2026 19:19:41 GMT  
		Size: 91.3 MB (91288264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc387f595deffdd2fd1faebe03cdeb153c03757d69cf2c7ded01920e3b8bb51`  
		Last Modified: Tue, 10 Feb 2026 19:19:38 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10da9f5675f6769887cf74629d06d7a3f4c6eef25967ac4b714808e97f764f48`  
		Last Modified: Tue, 10 Feb 2026 19:19:44 GMT  
		Size: 218.4 MB (218418089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:6fbdd28ae966db499001cae3fc6c0b47f210e280685f826d54b0b6d4c652e21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0366a2666d328a982d409dcbc4b2cdfb8f8c8ac323294ce607f73572118a64cc`

```dockerfile
```

-	Layers:
	-	`sha256:c9067bf19d5a6d4f40390b46a088655473000d2a135e1a271f21cf3c8054e286`  
		Last Modified: Tue, 10 Feb 2026 19:19:38 GMT  
		Size: 4.4 MB (4381981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee02a151bd5e1c44c4a9eafd5d361e0f939abd39b6a984d339da936f7e47a2d`  
		Last Modified: Tue, 10 Feb 2026 19:19:38 GMT  
		Size: 22.6 KB (22629 bytes)  
		MIME: application/vnd.in-toto+json
