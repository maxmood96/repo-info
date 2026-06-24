## `neo4j:5-trixie`

```console
$ docker pull neo4j@sha256:937fbd163e302a5751dd329b719c1b05e2a4293af223d61b1aa17e3dea087709
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:41f6fec4080d2f5b10b47d3392a19ffaf8f71d2e89100757559e2a43b6a8f7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355577091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b4c30662aa794360bae816e76ecc6d4206bcbaefadd56d344526d3feaba962`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:43:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 01:43:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Wed, 24 Jun 2026 01:43:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 01:43:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Jun 2026 01:43:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:43:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 01:43:57 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 01:43:57 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 01:43:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:43:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd9c01fcd53c66a79850bb146e9cb313e088b65a3481a04ca2984714b2c4fa5`  
		Last Modified: Wed, 24 Jun 2026 01:44:21 GMT  
		Size: 158.2 MB (158166944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3dd63890f5f6518340e958cf8f308b0d4a8a9b6be6c0e0ffb98151f7bfc3b9`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e968292c86b05db92b835fccabc753b614a3da96163c6f60a89463efc482b6`  
		Last Modified: Wed, 24 Jun 2026 01:44:21 GMT  
		Size: 167.6 MB (167614633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:04b743611846c64a5ec391e080fcc60b2970556ca0696da48b165f803e34e878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8041303a6071bc24104d851d292b5b0d1076404bf2e1408f0043c7f96826f6`

```dockerfile
```

-	Layers:
	-	`sha256:3aab61bf0de391a8af83d66a7cff78aea07519854b3700bfb61b6e792d2dcf95`  
		Last Modified: Wed, 24 Jun 2026 01:44:16 GMT  
		Size: 4.3 MB (4291176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4de8bfc1c0877e428ab080d26bc1ab017fc5f5effc5444ffb6e21ea60f7b9d`  
		Last Modified: Wed, 24 Jun 2026 01:44:16 GMT  
		Size: 21.2 KB (21222 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:17825c4300c0c377ee968bee22f9ceb061e1ff89567ed6fef72e41fef9aec0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353307222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e3f50559cfbae99667de730e21f2c559159365285cfc7c2607f72f13d4deb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:47:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:47:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:47:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Jun 2026 01:47:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Wed, 24 Jun 2026 01:47:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Jun 2026 01:47:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Jun 2026 01:47:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:47:38 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Jun 2026 01:47:38 GMT
VOLUME [/data /logs]
# Wed, 24 Jun 2026 01:47:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Jun 2026 01:47:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:47:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c6a8b0cab814bf632626c7842b0970ff4773e13c74000e7962e57e8b70453c`  
		Last Modified: Wed, 24 Jun 2026 01:48:02 GMT  
		Size: 156.5 MB (156461287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2291513ed765eac5e7c71a5272bebcc3d5b1ba2f9a81531adc062d699791bc97`  
		Last Modified: Wed, 24 Jun 2026 01:47:57 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62c0393606a08108e49fafb1dd6fad63a86ffd6897dd308d117d11a61f1fbbc`  
		Last Modified: Wed, 24 Jun 2026 01:48:03 GMT  
		Size: 166.7 MB (166687289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:9ca5a58397345cbcbe1c24bd003e55fcb6e8d5b789d46f2f88a700fee634e176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4307143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad4cb890633c138c920a2619c291a844357131dd5ef4040716a9ee10afd0d1b`

```dockerfile
```

-	Layers:
	-	`sha256:49018b342cadbfd53a79901de579f9fabc218b078bd5142e6400461bf6429130`  
		Last Modified: Wed, 24 Jun 2026 01:47:57 GMT  
		Size: 4.3 MB (4285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5b639d529c3b4a69b7f975704d1a95573cf10a3d3b1a4f0a85ce056b9c754d1`  
		Last Modified: Wed, 24 Jun 2026 01:47:57 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json
