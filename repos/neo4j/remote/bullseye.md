## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:0c0152e8089c20403ca5c498b6b1b48a614d2ba6543a83575b2e9bec94eca6a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bff039b6746e30ad8099d85bd3a3084bc7ac3f86374c6377ac349b135b01f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.6 MB (431615441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dca195d3962588e2587ca3e0d25b9b9c1ad54b8f9043e001c934b4d0392fb8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Thu, 23 Apr 2026 17:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Apr 2026 17:15:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 Apr 2026 17:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 23 Apr 2026 17:15:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Thu, 23 Apr 2026 17:15:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 Apr 2026 17:15:42 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 Apr 2026 17:16:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 Apr 2026 17:16:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:16:02 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 Apr 2026 17:16:02 GMT
VOLUME [/data /logs]
# Thu, 23 Apr 2026 17:16:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 Apr 2026 17:16:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:16:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e30966e0e99bfd7d7758514a64bc6c81c95f7364a0ba2c8b7cc2b7b01f2d45`  
		Last Modified: Thu, 23 Apr 2026 17:16:29 GMT  
		Size: 157.9 MB (157857073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74bb2ecca27dc7cab42cf351da1d6512911cc73c9eeb90427d3200074e4f74f`  
		Last Modified: Thu, 23 Apr 2026 17:16:21 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c612fa502b9ff65de22ada40be515b2760712cd28775e90b70a7046b24524351`  
		Last Modified: Thu, 23 Apr 2026 17:16:21 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e75f69999c0327d98690fb875af483b0d0456b526e695a8e7749dff2fa36ed`  
		Last Modified: Thu, 23 Apr 2026 17:16:34 GMT  
		Size: 243.5 MB (243486358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5840756579885e859e764134461c1549c5c5df4d0c0098575b050de35d84ee26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4613589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29df4f3681fad7e646e37047b81392545dfa6c7ad35cdee3df8165097cdbee23`

```dockerfile
```

-	Layers:
	-	`sha256:0ce91d96cc04b79d4025b7112fc8be23405fd36a86f5e8fc83b94b8bcabdce4a`  
		Last Modified: Thu, 23 Apr 2026 17:16:22 GMT  
		Size: 4.6 MB (4591965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c996f94ab0ea2ffbabb669c57ea0aa99c4fb291fd6e3e022deec0afe99c463c5`  
		Last Modified: Thu, 23 Apr 2026 17:16:21 GMT  
		Size: 21.6 KB (21624 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:27510330a67747ffedb60c7432d6e17c7db72d5aa59ae5830b600948a6e85d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (427950549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459c12353ac0effaedfe9de8792f8df04cc6e62d3d6a773eb21f06425bf2626f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:18:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:18:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:18:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 00:18:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 00:18:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 08 May 2026 00:18:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 00:18:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 00:18:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:18:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 00:18:46 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 00:18:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 00:18:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:18:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfb3a82b0796308e2c41d1c0d273317b5438ed439a8ce13bf67c8449fd7c99c`  
		Last Modified: Fri, 08 May 2026 00:19:14 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905f212d645d17e0fa7ab2584ba56a70463701a61a4212a82afea0b8065b3537`  
		Last Modified: Fri, 08 May 2026 00:19:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6578876cbfdb60047eaa2b6f8d881b146104bf22bd4ea6d6a30191a9bc0a73`  
		Last Modified: Fri, 08 May 2026 00:19:08 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b9bec9e00067bbaf249699faf02b598c7a26b821da543f9232ffe29efe468e`  
		Last Modified: Fri, 08 May 2026 00:19:15 GMT  
		Size: 242.7 MB (242732691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef144221f106261546c8d99aeb0ab231f220d62f4f1a66bbd36ce0274b95e813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ac6506272e777dc9d4301288ba1cb3ed95f9abd22302edd9afbcab16931300`

```dockerfile
```

-	Layers:
	-	`sha256:d49b73793921ade88480f30e18d1f09d81fa48281fdd808082cbda4c87445c93`  
		Last Modified: Fri, 08 May 2026 00:19:08 GMT  
		Size: 4.6 MB (4566421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f763240bc0abe452528c63ec6dd8480c8ddd6e1c1a282c965ca9a701f9af88a`  
		Last Modified: Fri, 08 May 2026 00:19:08 GMT  
		Size: 22.0 KB (21971 bytes)  
		MIME: application/vnd.in-toto+json
