## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:a7237cc068027ca50873d00586b8e77b613ba90a53c925703f73e93d23fe416f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:15dc77301ba3cb39c41f39c5bcd8c8202793afada6f330e0b8a5f5da35eab160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306680945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ce2c87b3693c17d50600e0a730c81150a0202271785685d4406fba9818b4e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:25:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:25:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e7479438004924167ceb707f9620ee39db7d06870e9ce00d52573350f3518dc4 NEO4J_TARBALL=neo4j-community-5.26.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:25:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
# Tue, 24 Feb 2026 19:25:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 24 Feb 2026 19:25:56 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:26:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:26:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:26:16 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:26:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:26:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:26:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6468fb9acbd36198f9ef0c819961d4e5eb208e4fab2676e25243a215d129f2e6`  
		Last Modified: Tue, 24 Feb 2026 19:26:39 GMT  
		Size: 145.6 MB (145628732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e29e5211f7bd020858ce844c8a06892c5e9ed8d2e1e882d85b4b2213c49b3b`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92dd844d2831d58accd337736f1d3910c73bd0d364fcf6323ea967a5a261cf`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da1e928a3da427f0c530cfc07aa0c3fbf49904d8b2b7a014151570067e5297c`  
		Last Modified: Tue, 24 Feb 2026 19:26:38 GMT  
		Size: 130.8 MB (130779718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:090a2fc033ee68e6568c8d9697807109420b2e3484e3f50cde06ca7be6b3ba52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbc6fd945f856c2a414da2bc5e51b4af5ab8a49bc56088a7c49af72eb477995`

```dockerfile
```

-	Layers:
	-	`sha256:ed2361d6bd0a8ac0415c9dad1919f93f6339f8cb226ce55e4b6caf4d6ea001a9`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 4.5 MB (4491217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07ff0c04de1487065dba4a6b4da4c1eb03e9b65be459d99aa66d7cd10b8e9aa`  
		Last Modified: Tue, 24 Feb 2026 19:26:33 GMT  
		Size: 21.0 KB (20954 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eafe38fc2094c9a921539263c8d70a5b6fbf9b0e9d31b9f2a3d2929a9b9e4a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303220518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c0fabf9a364c6927c55862bf5f5d5467bfc9f5cfc44a7411ec4c8928112584`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:30:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:30:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:30:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e7479438004924167ceb707f9620ee39db7d06870e9ce00d52573350f3518dc4 NEO4J_TARBALL=neo4j-community-5.26.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:30:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
# Tue, 24 Feb 2026 19:30:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 24 Feb 2026 19:30:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:30:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:30:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:51 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:30:51 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:30:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:30:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:30:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4323552f0ea743febfd1288965bcdf308ef4f3975eb43d4bcdc4fff21faa60`  
		Last Modified: Tue, 24 Feb 2026 19:31:16 GMT  
		Size: 144.4 MB (144436184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968e10fe7afe76d5473b57fc05b03bcb63807de6ff4844cb50d2f2cd5512e04a`  
		Last Modified: Tue, 24 Feb 2026 19:31:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca174944b1cf7594c4c25a9d9a5be5e5613de266dfa15e5000ee7e502aa991fb`  
		Last Modified: Tue, 24 Feb 2026 19:31:11 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977e7ac0c346578b30553663c4f0f776f31cf950b15e258797af93a5f5fc7979`  
		Last Modified: Tue, 24 Feb 2026 19:31:16 GMT  
		Size: 130.0 MB (130025724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b51118d7a5f635a547bcc93853f2b9ba49492f7772a7380c489c3be7f58768d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4486145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666d56f135a96c0b147187be627ec18157d02b76cb840d1fff1ab16195f44cf7`

```dockerfile
```

-	Layers:
	-	`sha256:656cbb9239f7c8c9e1c00778a5f6fd70b3496bb02370d1e8760301b3f8d6e010`  
		Last Modified: Tue, 24 Feb 2026 19:31:11 GMT  
		Size: 4.5 MB (4465022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb72246cb505d1255716d1b774eb22f2f93ddd74e5250ced19612d0eb36d79b`  
		Last Modified: Tue, 24 Feb 2026 19:31:11 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json
