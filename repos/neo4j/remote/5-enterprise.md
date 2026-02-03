## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:b704e3461edd4774182ff2c1085397dc3b867194d9554ee47a632bd0f9dfdc6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0c25fa90e883751869bd5e9e4c723d0c49fcfbd1f6e262016b372d0b56411e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.1 MB (684149342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abd4c8beccfd2a48f38391cead75e64592080649f8eee2503c9db405e66761c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:47:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 02:47:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 02:47:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b23f47fd5d1d1b22a4779fb05c39d7dfe2c1997654be75ecf3faab74fcda5121 NEO4J_TARBALL=neo4j-enterprise-5.26.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Feb 2026 02:47:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
# Tue, 03 Feb 2026 02:47:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Feb 2026 02:48:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       adduser curl ca-certificates gcc libc-dev git jq make procps tini wget     && addgroup --gid 7474 --system neo4j     && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Feb 2026 02:48:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:48:17 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Feb 2026 02:48:17 GMT
VOLUME [/data /logs]
# Tue, 03 Feb 2026 02:48:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Feb 2026 02:48:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:48:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e00f91cba6eb54b531fa1caa636ab9ceb5148dfcacfe78dbeee92b0be85ad11`  
		Last Modified: Tue, 03 Feb 2026 02:48:51 GMT  
		Size: 157.8 MB (157826001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953734f7e4c0158112a49a6a7c5b04175a3f87e7d1c8f1e4d6e52c2abf9da34f`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33bf7718b23f1f2e9020f2c0467630a959e9b690c8834c0457e1ef857cf5d76`  
		Last Modified: Tue, 03 Feb 2026 02:48:58 GMT  
		Size: 496.5 MB (496534649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:89578332a38033e9330aedf718a54375aa8bc7e075722eda703e46908b269c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b71ddd67add2a8e106a8b90d09a6a39d5e886be9666f1cab13b853e8fb49c84`

```dockerfile
```

-	Layers:
	-	`sha256:af1ece25dcda21187c7d284fd8e561f6a75d8c1e28e85a6d3554612b95f3fcf7`  
		Last Modified: Tue, 03 Feb 2026 02:48:46 GMT  
		Size: 4.7 MB (4668892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a50001d15d7ac12d5d50d410f4f7b1f4c47ab7b9be62e48f670ff4efe5dbc4`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 19.3 KB (19325 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7e9fd215d8c51dc77597aa0cb3eaf7bde56fc1438b01f985d80b6b07d9144154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.9 MB (681854664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7ccf4ee2109646b357c88b83b91a1e8058a2511318cf383a0f8f882cb69d71`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 23 Jan 2026 22:00:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 22:00:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Jan 2026 22:00:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b23f47fd5d1d1b22a4779fb05c39d7dfe2c1997654be75ecf3faab74fcda5121 NEO4J_TARBALL=neo4j-enterprise-5.26.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 23 Jan 2026 22:00:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
# Fri, 23 Jan 2026 22:00:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Jan 2026 22:00:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.20-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       adduser curl ca-certificates gcc libc-dev git jq make procps tini wget     && addgroup --gid 7474 --system neo4j     && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Jan 2026 22:00:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 22:00:46 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Jan 2026 22:00:46 GMT
VOLUME [/data /logs]
# Fri, 23 Jan 2026 22:00:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Jan 2026 22:00:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Jan 2026 22:00:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2cc7e8f46fd697b863d92a1faeab5e79a8748a4086efce3f984e33be806045`  
		Last Modified: Fri, 23 Jan 2026 22:01:22 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3149bd08a7db495478f6969897740f46415652118e7e35e9de21a6e4243cbead`  
		Last Modified: Fri, 23 Jan 2026 22:01:17 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3226a66d9c6e24a0574f58a88ddf2c53bdc3ba14c1fb4b90da4fe317f54e946d`  
		Last Modified: Fri, 23 Jan 2026 22:01:29 GMT  
		Size: 495.6 MB (495602951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:d2085d744cb6bd8cd2b5a3c8976b7b94a4108693f99ca37ea6955a5f29636cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4682825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feafbaf274869232f628ee7d04fa728402f84eb4b218320ed831eca5a8df546`

```dockerfile
```

-	Layers:
	-	`sha256:208a8a240e56630c66c8802edd533e1647e1335998ef468e9c94b9e43b27b183`  
		Last Modified: Fri, 23 Jan 2026 22:01:17 GMT  
		Size: 4.7 MB (4663346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6bfe3925c871e2cfbdc4f59880d36a00a9124c7373c26eb6c3337821f3fbf5d`  
		Last Modified: Fri, 23 Jan 2026 22:01:17 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.in-toto+json
