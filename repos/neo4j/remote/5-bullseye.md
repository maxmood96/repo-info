## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:111f8d029027013104b6ac23a5e650aeaefea611fafb8e9edc55e1728c8d13d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b8fcb236459e30025f81bd2ddd2eb13b8d76a1f4719d17de8b2e414123c6d90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305700959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff1b0df27c37b77e20b188d9ae069dde21b8337d3477ea390ebf69f01acecb5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:57:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Dec 2025 23:57:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 29 Dec 2025 23:57:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da87ec6d1d5f348815589fe1becce86f1c097ed72d30487669c4bba01ed622a7 NEO4J_TARBALL=neo4j-community-5.26.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 29 Dec 2025 23:57:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
# Mon, 29 Dec 2025 23:57:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 29 Dec 2025 23:57:52 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 29 Dec 2025 23:58:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 29 Dec 2025 23:58:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:12 GMT
WORKDIR /var/lib/neo4j
# Mon, 29 Dec 2025 23:58:12 GMT
VOLUME [/data /logs]
# Mon, 29 Dec 2025 23:58:12 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 29 Dec 2025 23:58:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:58:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26724fb5ef68658026fd131936ac622b8c5e573971e660624d5f1ad0045adf39`  
		Last Modified: Mon, 29 Dec 2025 23:58:55 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4260118b69faa9c45ebd3f91ea8260d87d0b4a2e5c3dd66f44e491dcb30ef479`  
		Last Modified: Mon, 29 Dec 2025 23:58:43 GMT  
		Size: 3.8 KB (3829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b2912b79ee49875a0ad176fcd261cf09ae57ecd9091c0db94b92941ff677f4`  
		Last Modified: Mon, 29 Dec 2025 23:58:43 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c9f204efa52145ff7b897d7acefe09ac387e4bc4edcc9553e26987d2af65f`  
		Last Modified: Mon, 29 Dec 2025 23:58:59 GMT  
		Size: 130.6 MB (130580652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0fe0565de606618b6e9bfc6601c849e093f8f7be809b80c7807d35c61abfec6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde02cc672cbd29881eb66ff1884d6944a99d6a3b82b90475fe23295915db554`

```dockerfile
```

-	Layers:
	-	`sha256:7076f7f38f2cc8a9f585f2470c0160acfe6801b68fbc5d8e5e312cc775fe4181`  
		Last Modified: Tue, 30 Dec 2025 03:45:09 GMT  
		Size: 4.5 MB (4481733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31236fe2169247df725444bfb12db4e5311ef44a2daf134f119b741b35ff7e0a`  
		Last Modified: Tue, 30 Dec 2025 03:45:10 GMT  
		Size: 22.8 KB (22766 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2706328053a597150f2f2bd6a7becc08afed197142c5ab2f5470bccfded8d956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302266694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22302bb5e1bdedb4e0880dea928448c7c90e7c409f1853f66548e2d32f78287a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:57:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Dec 2025 23:57:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 29 Dec 2025 23:57:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da87ec6d1d5f348815589fe1becce86f1c097ed72d30487669c4bba01ed622a7 NEO4J_TARBALL=neo4j-community-5.26.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 29 Dec 2025 23:57:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
# Mon, 29 Dec 2025 23:57:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 29 Dec 2025 23:57:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 29 Dec 2025 23:58:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 29 Dec 2025 23:58:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:12 GMT
WORKDIR /var/lib/neo4j
# Mon, 29 Dec 2025 23:58:12 GMT
VOLUME [/data /logs]
# Mon, 29 Dec 2025 23:58:12 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 29 Dec 2025 23:58:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:58:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff17433fd932beecf4e830c2a6049049e273974253fee3dddab17e88c05262ba`  
		Last Modified: Mon, 29 Dec 2025 23:58:53 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40745bfacd19071b68fb9f472f0f9f0b9aaac34344ba7abf4d84d4f71f4e383c`  
		Last Modified: Mon, 29 Dec 2025 23:58:41 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c192da3a442cce3f699bea1101efc910a589a0dfa158ee54d23a91c48eaee2ff`  
		Last Modified: Mon, 29 Dec 2025 23:58:41 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb50a53c4c3a50991e78deabd6b7afa40048becfc1a36650c27a5b7e4bda8a2`  
		Last Modified: Mon, 29 Dec 2025 23:58:54 GMT  
		Size: 129.8 MB (129824357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8f435e5c4d2a44ffeeb10f6d4ee0852b8a0d9a3f91544c26ea7625ebbf8050a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8732ea501e6c8ad1708fc383715a1e8d80f1cad2a119ec15ebb0c671223fd8`

```dockerfile
```

-	Layers:
	-	`sha256:5a70d00e19a9780f5979c6f1014258dfbc97fa6c1d66802759635670d1338228`  
		Last Modified: Tue, 30 Dec 2025 03:45:14 GMT  
		Size: 4.5 MB (4455610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f8b1ffa89bfd2ac479970031dbdeb73e049b06ccddf909876b263f2519e276`  
		Last Modified: Tue, 30 Dec 2025 03:45:15 GMT  
		Size: 23.0 KB (23007 bytes)  
		MIME: application/vnd.in-toto+json
