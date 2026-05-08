## `neo4j:2026-enterprise`

```console
$ docker pull neo4j@sha256:30229d532bfab4940403c0b1ee1849c0aa9722ab713ccf6d2897d8274a3e1b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:66748a87519e0411c18fcde6c00ec784f5cce5ff13b3cbbba0678b7b8ef7616a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.4 MB (514422498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55158f5ecbf259ace73cc15d7749ad8e55ba41f6ecf91a1fd364682665a8f008`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:16:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:16:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:16:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 00:16:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 00:16:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 00:16:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 00:16:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:16:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 00:16:36 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 00:16:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 00:16:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:16:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71846be7cf654615846527bbecfd8a80a137085542e563fbc2c1c21fe509db83`  
		Last Modified: Fri, 08 May 2026 00:17:07 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0e8ec1d8d3ec6e53dc679e08f2fa6f4d03f71de8299ea3ab40e225476edda3`  
		Last Modified: Fri, 08 May 2026 00:17:03 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa424644cfaa6fab4df5a58dfa42062020624a4a2495e8c48426a8cd5e21fbe`  
		Last Modified: Fri, 08 May 2026 00:17:15 GMT  
		Size: 392.1 MB (392057683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:a6aa54cbaa0395c47fd569936b7e703143f38fa776d5d5c937bc1a9002dafed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedd5fa4a6b29d27cfbd18ce221f17f9741ba103469b95e198ef2f5dbf6b2f22`

```dockerfile
```

-	Layers:
	-	`sha256:67288485b66b3a192a2d28661454950a0c77c3e58326c789358b79c37dd924d4`  
		Last Modified: Fri, 08 May 2026 00:17:03 GMT  
		Size: 4.7 MB (4664447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cd7f3cf3b4803056701b7c482df3978a67c12aaadc6fdb77ce540b5140c3e8`  
		Last Modified: Fri, 08 May 2026 00:17:03 GMT  
		Size: 20.1 KB (20116 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e43fdf261b21bddc31a25076f32aa8c63937ee98d7af1a1628b9f3e77becb401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512821188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bd809eae60364e9900afe6385d99e2aa9b79dbd357450ce8c711f7ceeab9b5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:18:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:18:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:18:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 00:18:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 00:18:26 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 00:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 00:18:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:18:53 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 00:18:53 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 00:18:53 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 00:18:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:18:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9b2f92aa76b85ab9e7703f10995bfa7a142a15695798d5a9dc24ae0ce0959e`  
		Last Modified: Fri, 08 May 2026 00:19:26 GMT  
		Size: 91.5 MB (91542292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0180c68d35ccb736fa4837c1a8843c8997aee9ca45715335f2ac51b8ac666d0b`  
		Last Modified: Fri, 08 May 2026 00:19:20 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac2acb76f204db3ece0637701bd2b395335cf456c3de4d86392c3b9146eab43`  
		Last Modified: Fri, 08 May 2026 00:19:59 GMT  
		Size: 391.1 MB (391125237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:1adfccf05c57bccfd956bdcd7ae37e39bf8cdff9da3b5afc4bba205f8957d30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4679217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25932f37e6c408367c67d6da6a72a52efcc8eaf5e645955a852240481077f832`

```dockerfile
```

-	Layers:
	-	`sha256:57bc4ec5bcd12aa2f475d2521784b15d08b02598a63af5e8315beb4ff9a01977`  
		Last Modified: Fri, 08 May 2026 00:19:21 GMT  
		Size: 4.7 MB (4658922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ce9f310928a0db2ebda04a012864803c990b71b5314fdfcca58c87fbcb818d`  
		Last Modified: Fri, 08 May 2026 00:19:21 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json
