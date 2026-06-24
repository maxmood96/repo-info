## `neo4j:2026-enterprise`

```console
$ docker pull neo4j@sha256:6b5eb6fbcced8aa99af57fc96367a21143cefc92aa8b97e4504480f46c23533b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:749443c5093689552fe3603611f7d8d047c23f57665fb3c0122925aa574cb594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.3 MB (517349508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2041d60626b0c5d04111dc3cd48d32dbff25d224026f3a48f9782d023a6c13a6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:43:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:43:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2507ce15c1410931cf81db4435c1e1e437d5a857f59db3f946697988a5263aeb NEO4J_TARBALL=neo4j-enterprise-2026.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 01:43:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
# Wed, 24 Jun 2026 01:43:26 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 01:43:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Jun 2026 01:43:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:43:52 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 01:43:52 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 01:43:52 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 01:43:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:43:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542e6d11ff1562bdaecf08153eacd5e05cc4683dfdb22cf950d5b45b99af2554`  
		Last Modified: Wed, 24 Jun 2026 01:44:21 GMT  
		Size: 92.6 MB (92574577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fb99d223c0a8bb4eceea2b574a7d23b5b5a87f690218295244c8ddd4d9cadb`  
		Last Modified: Wed, 24 Jun 2026 01:44:18 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f990d1c065c0617a0f717d9e871a24d3b9f14998d5691ce8023e2d7880fe07`  
		Last Modified: Wed, 24 Jun 2026 01:44:27 GMT  
		Size: 395.0 MB (394979461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:bfd0648c756a11ca1c8fbe0aba500571ec6adefb2ba0c58056d0234f17b08094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4682046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058a14b7954e4d07dbf04cdff15742625f680093d6ba641d5230482a577464ba`

```dockerfile
```

-	Layers:
	-	`sha256:99327ec62beb2003621abd728a85ffbb4cfa4021bdbca45fd955947e2e9479e6`  
		Last Modified: Wed, 24 Jun 2026 01:44:18 GMT  
		Size: 4.7 MB (4661929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55032f1897b0f2b33379a51619480f94ced262cc5dd7713c07d1c10ac4b90b9`  
		Last Modified: Wed, 24 Jun 2026 01:44:18 GMT  
		Size: 20.1 KB (20117 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6826dda17966c25f57152357aaf7a3071997afe79bb4fbb0a726825085a065fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515750957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9cd663e9ccfc55b60852a8c1372ac83073b03f4f6ab63f73c4bc8e14d895a9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:46:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:46:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:46:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2507ce15c1410931cf81db4435c1e1e437d5a857f59db3f946697988a5263aeb NEO4J_TARBALL=neo4j-enterprise-2026.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 01:46:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
# Wed, 24 Jun 2026 01:46:52 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 01:47:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Jun 2026 01:47:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:47:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 01:47:18 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 01:47:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 01:47:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:47:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0489e15e1263a6763f362ee037ab1bf2ebf057285e9dff62d08597c6c9cb5b7b`  
		Last Modified: Wed, 24 Jun 2026 01:47:49 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7687caeb32275c4c7168cc8b6307301f8b37af1cbd0a4866bed46b22428b1b42`  
		Last Modified: Wed, 24 Jun 2026 01:47:45 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc93bd443e9e2e3f9b1873c87e5741909d04008050b5aa0a485833b21dfb944`  
		Last Modified: Wed, 24 Jun 2026 01:47:55 GMT  
		Size: 394.1 MB (394050106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:195d31dc2bb77b3e995824f7f29c87499a4673bf849225a21d45d03e07111526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4676691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849b82e64ef0d69a6dceda45840ff2f5d3d6130d3282aa6ffaab3d251d1c464d`

```dockerfile
```

-	Layers:
	-	`sha256:e9373dfb115904a15b6b251fbf91b21078b8e597408d856422ca80257546af7b`  
		Last Modified: Wed, 24 Jun 2026 01:47:45 GMT  
		Size: 4.7 MB (4656396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a966bac1be89810c5ae362ee6ff108d7e1e92e583199421413c68ba0a8db95ef`  
		Last Modified: Wed, 24 Jun 2026 01:47:45 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json
