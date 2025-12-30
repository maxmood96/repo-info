## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:b95f895092a48e7d6852b6b592c30f426adb5ba406124d8e8e1b5ba4bedd72cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:83cda0a6824512d671442ec8fb0786ea89670b902063636ee6bc09cd49871394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668498939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31d9724aa5a5b803c1e56c0631bfc9b91a8bfc316bbdf72eb710bf6720b1fea`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:57:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Dec 2025 23:57:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 29 Dec 2025 23:57:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4090c59d7959304579e5725902d3c1cf0c5ffc5852da6e68d2f0cdd4e84bc3f2 NEO4J_TARBALL=neo4j-enterprise-5.26.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 29 Dec 2025 23:57:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
# Mon, 29 Dec 2025 23:57:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 29 Dec 2025 23:57:44 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 29 Dec 2025 23:58:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 29 Dec 2025 23:58:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:25 GMT
WORKDIR /var/lib/neo4j
# Mon, 29 Dec 2025 23:58:25 GMT
VOLUME [/data /logs]
# Mon, 29 Dec 2025 23:58:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 29 Dec 2025 23:58:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:58:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae79abbfb79209d03f424c822367b91c88630d2c27ef83305b6396d10b9783e`  
		Last Modified: Mon, 29 Dec 2025 23:59:24 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d06dd9b52f25f58b29a1ae81cb65add56c1d38b80cb7e38398380aa1b52da7`  
		Last Modified: Mon, 29 Dec 2025 23:59:11 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b14b67835018c744f7d5cd505558e5b563abb146adda36d14f9b0063351e8a`  
		Last Modified: Mon, 29 Dec 2025 23:59:11 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59493e2e94c7f641341353f4608e593c03a9715735c7bd5d99e923f7e033d56`  
		Last Modified: Mon, 29 Dec 2025 23:59:44 GMT  
		Size: 493.4 MB (493378622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e82d94e3afe16caec4fb066d36a5d8c8285e06153823323651f59664f0a41c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4868197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf86c54877e82eb6fc2b70d8271133e53eac9ce5703062728d8ae6e17b5e817`

```dockerfile
```

-	Layers:
	-	`sha256:c2d97684cc68bc833200d6c2e22d7c8b32ec256474bb2f3a8c032ab8ecb861aa`  
		Last Modified: Tue, 30 Dec 2025 03:45:23 GMT  
		Size: 4.8 MB (4847212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf2010665ff28dc38f85c737ab6a6abdfd0c6415edabcbcd1ddee932d81f9b4`  
		Last Modified: Tue, 30 Dec 2025 03:45:24 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85cefbdf858c27030cd1c0838e6b60453ceed5b400255df3dcec08e12e9c1f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.1 MB (665064891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacebad3f05f11b473393c1dfaa95633831d570c0274e018f52d6d2362ee1b52`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Dec 2025 23:58:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 29 Dec 2025 23:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4090c59d7959304579e5725902d3c1cf0c5ffc5852da6e68d2f0cdd4e84bc3f2 NEO4J_TARBALL=neo4j-enterprise-5.26.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 29 Dec 2025 23:58:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
# Mon, 29 Dec 2025 23:58:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 29 Dec 2025 23:58:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 29 Dec 2025 23:58:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 29 Dec 2025 23:58:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:58:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 29 Dec 2025 23:58:59 GMT
VOLUME [/data /logs]
# Mon, 29 Dec 2025 23:58:59 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 29 Dec 2025 23:58:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:58:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec70c5cbb8fdd2babc304de364b7024115658c332ff63e975307ff9ba747ebb`  
		Last Modified: Tue, 30 Dec 2025 00:02:20 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90dfbd1eec88cf45c763625a5530c97abc55afb94ab24c1b86a17c4d7355250`  
		Last Modified: Mon, 29 Dec 2025 23:59:48 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0e3c62b21701081cbf720131f84ea52510cec83d65338db8e8409097cb6179`  
		Last Modified: Mon, 29 Dec 2025 23:59:48 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfd7c28f7ae39159679bc8a7546bcf70157b5e16f1ed2b97be775ca495a4d40`  
		Last Modified: Tue, 30 Dec 2025 00:00:19 GMT  
		Size: 492.6 MB (492622563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e021a4a8bc92fb69e35add9185243eb1af7ba03f74646f37d198a903d9858c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4842171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17f0b67489525a19cdfb942a425a73ae8c400080ef37d108121692cd266d17d`

```dockerfile
```

-	Layers:
	-	`sha256:9d6fd9b0160562f4192931b19fa87788713671fd7373ee73670d8f0adcf5367c`  
		Last Modified: Tue, 30 Dec 2025 03:45:28 GMT  
		Size: 4.8 MB (4821017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07fa3973d0dc99ab7efe4f26dcc528d9f7a91acbc9bada1d6a48c4c31761089a`  
		Last Modified: Tue, 30 Dec 2025 03:45:29 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
