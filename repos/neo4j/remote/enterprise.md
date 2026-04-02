## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:7175c2d3e7b7efa3f67ee942c0511cf7eccf88cc632d148fb593978846e70c4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:169c6a0d0d724fc6d87b8652817a14432aa39cffaf02548a132d7ef09ca69a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515194945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f66f1bf59affd4bce2e7c32cba50bda602315f7cdb8a784404daa6f88e40e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Wed, 01 Apr 2026 21:09:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 21:09:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 01 Apr 2026 21:09:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 01 Apr 2026 21:09:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Wed, 01 Apr 2026 21:09:47 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 01 Apr 2026 21:10:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 01 Apr 2026 21:10:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:10:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 01 Apr 2026 21:10:19 GMT
VOLUME [/data /logs]
# Wed, 01 Apr 2026 21:10:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 01 Apr 2026 21:10:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:10:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18457cbc2a024090101ea50d8e030f80fae44246cabbdfa59375a315b8b2f99`  
		Last Modified: Wed, 01 Apr 2026 21:10:50 GMT  
		Size: 92.3 MB (92256328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cd7303681ae29c65daf5ebfa029dd8df62cd7ab95f95d367abd1663ebebcb8`  
		Last Modified: Wed, 01 Apr 2026 21:10:32 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209bc44d7f4eae35ab1b7da047450cad9485fc578b39fb04c349d32466d15dc1`  
		Last Modified: Wed, 01 Apr 2026 21:10:56 GMT  
		Size: 393.2 MB (393153067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2b007bc4afb6a47ac335f6a92b322fb36c8940152de2dac9b5be2829fc4affb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4673084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc322015c2c5cbb7b3f1f4df6cf2a96be1fd1b96e5529d92eee52ec5319d7536`

```dockerfile
```

-	Layers:
	-	`sha256:680c2378c3f669c13f8a3e1af8ef6210b39e00db45da49734c9b04b65fa1f907`  
		Last Modified: Wed, 01 Apr 2026 21:10:46 GMT  
		Size: 4.7 MB (4653121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33c09cb7d3e7b135dddba4ae3254d1b74201ff498fc7ef84be1716f13459f390`  
		Last Modified: Wed, 01 Apr 2026 21:10:46 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a019228c8bd3152d368305787cdf82b8d791a30f98c9320f2c92432efd7b4718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.7 MB (513663904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0a22e3352ec90dccd3460a516d4e6d34a4b0deb12b7918a8b03e658c37fe3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Wed, 01 Apr 2026 21:09:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 21:09:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 01 Apr 2026 21:09:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 01 Apr 2026 21:09:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Wed, 01 Apr 2026 21:09:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 01 Apr 2026 21:10:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 01 Apr 2026 21:10:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:10:19 GMT
WORKDIR /var/lib/neo4j
# Wed, 01 Apr 2026 21:10:19 GMT
VOLUME [/data /logs]
# Wed, 01 Apr 2026 21:10:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 01 Apr 2026 21:10:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:10:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561bf837ad2917a034a321f77832691a9b617e17d36b9a06c3e70bc5b420319f`  
		Last Modified: Wed, 01 Apr 2026 21:10:52 GMT  
		Size: 91.3 MB (91288291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e987e551425f350b0fb55316d8a1aae5705a9ffe8a69d6963f3d3fe571ca2`  
		Last Modified: Wed, 01 Apr 2026 21:10:47 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f28764cbe572225908fc324b7d878a57d954343ea91d1d0dde3c388f98dc5c`  
		Last Modified: Wed, 01 Apr 2026 21:10:59 GMT  
		Size: 392.2 MB (392227150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ae093fc8c9576e213b792b7c871d0bbb8a88b49844e71e603963d94129a445f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9e991d2cd834af4db1d253300a26bbcde4fb524721f2e6224e91f75ab4047d`

```dockerfile
```

-	Layers:
	-	`sha256:84bf64911d0f3c3970cc746bbc77cb32f849335aab248f42370ecea20074b555`  
		Last Modified: Wed, 01 Apr 2026 21:10:47 GMT  
		Size: 4.6 MB (4647596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5454c9e8baa0f03b16a31cfa7149ad8e101513c1cce38f0a422c75e63073a0e7`  
		Last Modified: Wed, 01 Apr 2026 21:10:47 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
