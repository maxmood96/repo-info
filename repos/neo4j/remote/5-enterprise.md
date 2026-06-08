## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:ad508937cb52cbe45a0f853eaccba1b9cff3a26914891ee23873b3e89602d754
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d0bd1c9b11dd472f8e9b58bbb4cee681f4ad371b524c77e3a3210684839ebb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.5 MB (701473433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2aa9ecec3ba53e9d3dddc44ee2d2d51d37fcaca536059b7823be2f21a65bfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 19:31:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jun 2026 19:31:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Jun 2026 19:31:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=757fe6cf1d682b73f41d24a3f3dd1e13c32c8c0bee056708cdc116b89c9ac759 NEO4J_TARBALL=neo4j-enterprise-5.26.27-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Jun 2026 19:31:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.27-unix.tar.gz
# Mon, 08 Jun 2026 19:31:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Jun 2026 19:32:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Jun 2026 19:32:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 19:32:19 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Jun 2026 19:32:19 GMT
VOLUME [/data /logs]
# Mon, 08 Jun 2026 19:32:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Jun 2026 19:32:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 19:32:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239184a9336a4e3cc232e9d345e3c67cc85504bd8014840315695e072bca12c4`  
		Last Modified: Mon, 08 Jun 2026 19:32:56 GMT  
		Size: 158.2 MB (158166925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d232eb23cb1df3c4b0a8e7426ca47131647d2942e2f875f50ebbbee737ae903f`  
		Last Modified: Mon, 08 Jun 2026 19:32:50 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8227b52c6022a616ebf886bddad93bf2a54e4f9b0f4f2b4acf1d8aa7e987dc`  
		Last Modified: Mon, 08 Jun 2026 19:33:04 GMT  
		Size: 513.5 MB (513516490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e5304f8ce319d1effb105c5a5b4cd026d00acc34255bbcf35ca60ab3938ca5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4677079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7cb882dd9cc910afffb643ea35cac51e6e1f5bd77e5b4ef2777835baba220c`

```dockerfile
```

-	Layers:
	-	`sha256:f3abd6dae80d76865fca44c2f2db4571bae07f12ba2193328bea9273ce9d6a11`  
		Last Modified: Mon, 08 Jun 2026 19:32:50 GMT  
		Size: 4.7 MB (4657628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7d3acaaf1b60ae11ea8d140da01592e7b0decfcc78c62562a1b04edec22090`  
		Last Modified: Mon, 08 Jun 2026 19:32:50 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0c22e931ad91b6503e40d01f335a4eee1096e55136bd93e2d3720d73399f565a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.2 MB (699197768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc804718887a21c35189fdb755f9ba3c3f5531c55b44a24f089a38cdb69f3e9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 19:31:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Jun 2026 19:31:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Jun 2026 19:31:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=757fe6cf1d682b73f41d24a3f3dd1e13c32c8c0bee056708cdc116b89c9ac759 NEO4J_TARBALL=neo4j-enterprise-5.26.27-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Jun 2026 19:31:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.27-unix.tar.gz
# Mon, 08 Jun 2026 19:31:39 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Jun 2026 19:32:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Jun 2026 19:32:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 19:32:21 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Jun 2026 19:32:21 GMT
VOLUME [/data /logs]
# Mon, 08 Jun 2026 19:32:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Jun 2026 19:32:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Jun 2026 19:32:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a6871a555ed9a72789578f140d9367df8d5dc42eb72ba221e3fb1ea86e334c`  
		Last Modified: Mon, 08 Jun 2026 19:33:01 GMT  
		Size: 156.5 MB (156461285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea1508aa4edffe1694bf8f2b86409ddef5c45ff1412f3a69839d6fa70f521b9`  
		Last Modified: Mon, 08 Jun 2026 19:32:53 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8549154a807e326db94406617c724875739642ffd29b6da5bea660a7c6be588f`  
		Last Modified: Mon, 08 Jun 2026 19:33:09 GMT  
		Size: 512.6 MB (512584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:144c86fcd70970c9943623601bf06e61e052cd7da1147818aa48fa691d1205ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4671679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fed25ea7e5060ded6cf76dba23839010d6fd85211dffc0c9225a32355b120b`

```dockerfile
```

-	Layers:
	-	`sha256:4a36ac56ac17b77f101ae1623614636d0561cb3c9dec8074e1e2b66ec2aa55b5`  
		Last Modified: Mon, 08 Jun 2026 19:32:54 GMT  
		Size: 4.7 MB (4652074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1834a3edb5e008d6c4fbba6ebdbaed47f1956b510d35f262d58774ffbb007422`  
		Last Modified: Mon, 08 Jun 2026 19:32:53 GMT  
		Size: 19.6 KB (19605 bytes)  
		MIME: application/vnd.in-toto+json
