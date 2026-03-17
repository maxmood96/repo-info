## `neo4j:trixie`

```console
$ docker pull neo4j@sha256:1b900c4b7fd292126117f9c4ad2b66932a6630f5fdaa8a7d218d3a2d8a425c4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:58ff34dbdf0e2bd110d15b51e952c869909d46426859c70355cceb1de3e7d2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 MB (384586916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb8ef161863a5e3386d3372493a6fb7af09ee5680d42c741a034a400ab59d2f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Mar 2026 22:42:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 16 Mar 2026 22:42:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Mon, 16 Mar 2026 22:42:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 16 Mar 2026 22:43:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 16 Mar 2026 22:43:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:43:11 GMT
WORKDIR /var/lib/neo4j
# Mon, 16 Mar 2026 22:43:11 GMT
VOLUME [/data /logs]
# Mon, 16 Mar 2026 22:43:11 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 16 Mar 2026 22:43:11 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b037991ce7e80619de683a4f5eb88ccf74143802f9c7b1a87bbea9dcf554b2`  
		Last Modified: Mon, 16 Mar 2026 22:43:34 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e678c3f4c7f7061f33975cc33c1fd769a50e68bbeb64f55da51c577a99c1aa`  
		Last Modified: Mon, 16 Mar 2026 22:43:30 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e7731538bb3dc5783f7033eaad6b345ef9bedbabaa41892b532c42952e1cc`  
		Last Modified: Mon, 16 Mar 2026 22:43:37 GMT  
		Size: 262.5 MB (262545050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:694ce3c5ca3fe677fecbc4f6390f2b82eba2a9b2e1cb741dd89ca4d179f0bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4400798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462e5afb28b7458db85d35a67151e7de59533c9fb617479938a78f2fab70d297`

```dockerfile
```

-	Layers:
	-	`sha256:8b97acac2adaf0bad5cff47b8eefdcc2cb388024649e4a11719a684ae1d88a21`  
		Last Modified: Mon, 16 Mar 2026 22:43:31 GMT  
		Size: 4.4 MB (4378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c360d700c3bdea8c5903927468c6cd2fbfaab85de35a33708e45a7003133a2`  
		Last Modified: Mon, 16 Mar 2026 22:43:30 GMT  
		Size: 22.4 KB (22355 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a0d00e6d5adda35707aff9f7087ab8d948fb536463e96323f91d3ca1fa8a44a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383050639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d03ceac786acc34e1d7edf6e7694bca1709396220587983801c419d80cc9f39`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Mar 2026 22:44:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 16 Mar 2026 22:44:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 16 Mar 2026 22:44:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Mon, 16 Mar 2026 22:44:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 16 Mar 2026 22:44:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 16 Mar 2026 22:44:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:44:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 16 Mar 2026 22:44:56 GMT
VOLUME [/data /logs]
# Mon, 16 Mar 2026 22:44:56 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 16 Mar 2026 22:44:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:44:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ceba906f16a7274403c6b3b61ae8c11ae4430459f37b0f072e7cfe166580d5`  
		Last Modified: Mon, 16 Mar 2026 22:45:22 GMT  
		Size: 91.3 MB (91288290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93646d02aef5f83476eb52d8fe345ba603e339486fa054dda0c98ae4072436b8`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c1d5d2d45a7420aebcc3b430633ae283973b1588a39148b6232f9b05e57113`  
		Last Modified: Mon, 16 Mar 2026 22:45:24 GMT  
		Size: 261.6 MB (261613880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:aa29824f11da9bd6b3a44471067a49dec56b62e47769a7fb09d2f81921442e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4395643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988b2185ec8dee40b33063acc312cd7d25ebdd182f0a71b39a3515a21c5dba8a`

```dockerfile
```

-	Layers:
	-	`sha256:f56042652585c7ff7c050e73346d37e31ccccf79421e6f13f46288264b9fa991`  
		Last Modified: Mon, 16 Mar 2026 22:45:18 GMT  
		Size: 4.4 MB (4373014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db63fcd1a2e57d6450724d3f455c9061f17bd7fcff609d8e3888264801bd2b1`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 22.6 KB (22629 bytes)  
		MIME: application/vnd.in-toto+json
