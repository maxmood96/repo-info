## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:c69db090912f09a8d8fdb26235691719242a1b15d860ad77411c8d609f5e979b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c373e151e5a56106c292febb694d04e863c99ed9764e862d46d7393169654d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.2 MB (490244843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1937cbb0df01ad17a9ea9c1a99e6aa1b237ab8789c22a916b1150b8c0ac8cc3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 10 Feb 2026 19:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Feb 2026 19:17:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Feb 2026 19:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Feb 2026 19:17:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 10 Feb 2026 19:18:00 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Feb 2026 19:18:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Feb 2026 19:18:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:18:36 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Feb 2026 19:18:36 GMT
VOLUME [/data /logs]
# Tue, 10 Feb 2026 19:18:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Feb 2026 19:18:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:18:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11ba3fb971da1b09eb297b07369f4c2b55379f5506aef563ad339686e0f3e7f`  
		Last Modified: Tue, 10 Feb 2026 19:19:05 GMT  
		Size: 92.3 MB (92256279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ab686fc289e882e69ecb9859a0455d6d5fb722823da3902349225a8ab61cea`  
		Last Modified: Tue, 10 Feb 2026 19:19:01 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b9b622c2be077899e5170218ec195d75d3071860b7568aee6427e9450771bd`  
		Last Modified: Tue, 10 Feb 2026 19:19:11 GMT  
		Size: 368.2 MB (368199916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4c066a6b3d949f78bb3c0b3dd1cb88c53fdb8d41fa4beefefebb76fde9646db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4650079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5027a6edaf1a70253922feac64c4fcd31e509385b831ce94da9a380a2c132e`

```dockerfile
```

-	Layers:
	-	`sha256:e5149d5cef4a5c60a733f781e3d88e313114fe469c6b79b7381ca1a7f9bac723`  
		Last Modified: Tue, 10 Feb 2026 19:19:02 GMT  
		Size: 4.6 MB (4630116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a7973fab3d6afd0e5badbd9503471f824ee108bfdf4fd25f5ba56f2c8c6a35f`  
		Last Modified: Tue, 10 Feb 2026 19:19:01 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3aa99381b3af91f7df8f6a55b6e3e9ed88c5a7aba69e92b8f96e19f9568141b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488713523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09a3bd8feb540c375c7c38b5352d7f99427a729c2764d3466f44b983cb3960f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 10 Feb 2026 19:18:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Feb 2026 19:18:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Feb 2026 19:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Feb 2026 19:18:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 10 Feb 2026 19:18:59 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Feb 2026 19:19:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Feb 2026 19:19:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:19:25 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Feb 2026 19:19:25 GMT
VOLUME [/data /logs]
# Tue, 10 Feb 2026 19:19:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Feb 2026 19:19:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:19:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad6acff8b11a78b630a5189422c238eebf4ec64615b7155ea7591283e0eec67`  
		Last Modified: Tue, 10 Feb 2026 19:19:55 GMT  
		Size: 91.3 MB (91288264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3b9ce4b06b23822df18cb54fb0b47a4ed2c860321211ed3b3762abe8e666b`  
		Last Modified: Tue, 10 Feb 2026 19:19:51 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d47d368fff6a96e5dfd8c3a0da26bd039dbb8d4d9ec8840f26f66dc6739c18`  
		Last Modified: Tue, 10 Feb 2026 19:20:00 GMT  
		Size: 367.3 MB (367275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0309b13a44d854ef729dcd798acc37ab202066ac7b97a3135ce6026ec1e11cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2cc4d5ed27d76dba8542c0be614a588c81c8eba3e48b6ccc28fe33337d7851`

```dockerfile
```

-	Layers:
	-	`sha256:5d39694ae1674c1d26d3924cb2a49636dfa7985b4de3f429d29aef0dc2a1febe`  
		Last Modified: Tue, 10 Feb 2026 19:19:52 GMT  
		Size: 4.6 MB (4624591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c553183e367dc424b032f21ccb1c6fed94c0eea7fa78448df1b452648b19a0df`  
		Last Modified: Tue, 10 Feb 2026 19:19:51 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
