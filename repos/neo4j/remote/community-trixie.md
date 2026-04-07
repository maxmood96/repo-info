## `neo4j:community-trixie`

```console
$ docker pull neo4j@sha256:a5feb81d916c82d09186807ee8f8a523eb430d578fa6015f37ae72a07f976537
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:f75f94d65018c501678885af5403a6973ed98df4f4604fdcd41d1295d8e6fc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.1 MB (373142359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03ce821f61efd0e3f94586cf98400f2867e359bbea54edb2e148d042f2aff2d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:57:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 02:57:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Tue, 07 Apr 2026 02:57:41 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:58:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 02:58:06 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 02:58:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 02:58:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1081ea499e6a73149885d808c54ba68840285a9b9a3c22c4ce59bf4f3a1f1e`  
		Last Modified: Tue, 07 Apr 2026 02:58:31 GMT  
		Size: 92.3 MB (92256292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41fdec337238ee225998b7f372500c47123df262bc50959ab2bf3b91cb1aca`  
		Last Modified: Tue, 07 Apr 2026 02:58:27 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cb9cfbf07ce8858f6130850b870552653a956207a80708421c1e4fa7a5c949`  
		Last Modified: Tue, 07 Apr 2026 02:58:34 GMT  
		Size: 251.1 MB (251100374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:46a2165e4a9942835e62d0d796b8a072ab18b3582a01b106c203e42ab50de2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4374432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16d0041d321f92914231636f973f9a177f041170682124538d20cb5cc09e134`

```dockerfile
```

-	Layers:
	-	`sha256:d43d83331e3cd836c18392ce164a5bec4dbdc6b979070bc3c0c680cce579bd5d`  
		Last Modified: Tue, 07 Apr 2026 02:58:28 GMT  
		Size: 4.4 MB (4352077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a693f14db1d357aa82b6153f1b5fe668f70182e840fa0caba794e1a5f0a3534`  
		Last Modified: Tue, 07 Apr 2026 02:58:27 GMT  
		Size: 22.4 KB (22355 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5723a86b432dd48a030f6e578739cb1a8514233ef650ce2df2fb83a3aa31f717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371612299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef970831387438a3f7c68c7f5c3b91152cc7703fdafceab8b1f1ada9fbdb123b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:10:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:10:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:10:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 03:10:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Tue, 07 Apr 2026 03:10:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 03:11:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 03:11:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:11:19 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 03:11:19 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 03:11:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 03:11:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:11:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990e0b1af1ca501b4fd53771d4382d38320380eecdaa641e6ad3cf01fcb98f4`  
		Last Modified: Tue, 07 Apr 2026 03:11:44 GMT  
		Size: 91.3 MB (91288266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379d0e843205af072daa67916d001510d04dfb54a167b8344339f828135079b`  
		Last Modified: Tue, 07 Apr 2026 03:11:41 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf8abc071c27c88b3499276648c27111421aef7e6735b0284efbb7b0e22f16f`  
		Last Modified: Tue, 07 Apr 2026 03:11:47 GMT  
		Size: 250.2 MB (250175429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:f32ca2f98872d31869478835e95ad7f2bd2635ea07c6c6f53620ca5210f7d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c555684f2ea94189ac452e9af4012eab8c2f64ac3831197c926cb6c8bf860104`

```dockerfile
```

-	Layers:
	-	`sha256:d4f9ba07b04dab6560ffbebedbce1e5d05f13b64887b99d60d8008be1c1989c0`  
		Last Modified: Tue, 07 Apr 2026 03:11:41 GMT  
		Size: 4.3 MB (4346648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd44c16e3b51b3d9b84914697e22fc564c1750fc6f2c9f0913953a76fd7be81`  
		Last Modified: Tue, 07 Apr 2026 03:11:41 GMT  
		Size: 22.6 KB (22629 bytes)  
		MIME: application/vnd.in-toto+json
