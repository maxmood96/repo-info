## `neo4j:latest`

```console
$ docker pull neo4j@sha256:05ecd534432a68288643929ea0ecd77f6558725dbe74d4f18060de34c5b556f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:eb31e3006c2ca014a46d0272807995d9012899591c63120ba0a838cfe45ea664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336743054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268cb77482f3f7ee70b81e62e8c397e931fc6b847868f3a4a39d7c4fd5b3c5bd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8cae10d52593f1764754b8c5cda548e87facec1009bff6cc5290b949fe872d`  
		Last Modified: Fri, 31 Jan 2025 02:16:08 GMT  
		Size: 144.6 MB (144566514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fd0ffd7fd6422276a86acc3f69d477c22405cb5edf8210f61ca97212774ba1`  
		Last Modified: Fri, 31 Jan 2025 02:16:04 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e08e81ad4a8018b4713341d71bf3443f34f791fa6784ed9806f9c9c05dde936`  
		Last Modified: Fri, 31 Jan 2025 02:16:04 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecf242c02bb435bfb24c0f3e74816f6e279d00c0ced5ad7f338a0fbfdfa87b0`  
		Last Modified: Fri, 31 Jan 2025 02:16:08 GMT  
		Size: 161.9 MB (161909971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:558460218b36fb010a2d872365f257da02ee21290ca97965e0b9b5fbbc327b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b13751931c9c41cc952b50063544dde9efc3bd6b9988f0e7fc59d68c2a03215`

```dockerfile
```

-	Layers:
	-	`sha256:f8bda9f75e0e79e57e5aba556fef91ab7c3a651e7888aa8794d2b087b804dcb5`  
		Last Modified: Fri, 31 Jan 2025 02:16:04 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e06fd336fde61f9082d2591e45a2205d22baf6d205957c11106b4f9125e6bf0`  
		Last Modified: Fri, 31 Jan 2025 02:16:04 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json
