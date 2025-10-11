## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:16959c76edc23174482d7a1ad05ffac5eafc754c3ad1e7a3a4aa52e5d0612d3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b78dd50ace018d91902d9f80d56a96375c83e11e2db9674659b9f66da167f3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.9 MB (666935666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344cf73988be25c32dd80ee22d85d0735a7f7e70fb3a44397422adeabe7a803e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Mon, 06 Oct 2025 07:06:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Oct 2025 07:06:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=379c3771ab55d7c9c62cfb52c5ca47d19452e042951560a73e3bc3ba2b13e5e4 NEO4J_TARBALL=neo4j-enterprise-5.26.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 07:06:58 GMT
WORKDIR /var/lib/neo4j
# Mon, 06 Oct 2025 07:06:58 GMT
VOLUME [/data /logs]
# Mon, 06 Oct 2025 07:06:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 06 Oct 2025 07:06:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9b8aecb23d1b0fb331b3ba495a9c3efdacb5835dee9d88989c6b576ec789e5`  
		Last Modified: Fri, 10 Oct 2025 05:45:01 GMT  
		Size: 144.7 MB (144693292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac75c6628e0412761c73cb69817172636582d7e1ee121cba7daa5adaaaf64d6`  
		Last Modified: Thu, 09 Oct 2025 23:02:20 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879cbc326e890aecb4ec76e087a7cae3bd623f5f828bf739927adbcb9ce0a57`  
		Last Modified: Thu, 09 Oct 2025 23:02:22 GMT  
		Size: 10.1 KB (10056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4888942fb21d438f27a33958955ed7202bd1d9f81fdf2f68050db6f8c4ea51`  
		Last Modified: Fri, 10 Oct 2025 05:52:06 GMT  
		Size: 492.0 MB (491970085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2659f1ed97353f52204806d0aa2424ae27b5f062690f93f51a33d4ba0cfb05f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4876518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d755dd62b3e3ae052131c273716737dbb8c9719c63aa65972ac3e64c17bb9e9f`

```dockerfile
```

-	Layers:
	-	`sha256:a66fea1f3a5b55448beb0a76c2ad3732cc118144c8994a66ea686d4a07dbb256`  
		Last Modified: Fri, 10 Oct 2025 05:44:51 GMT  
		Size: 4.9 MB (4855490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb071749a21bee10241551512fc316c23011d3295f7b517e5fca26d8cb221bb`  
		Last Modified: Fri, 10 Oct 2025 05:44:53 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45dc1cd3cd8c95ce46be187c50c8dc7fbd0fbfc858dba114af03188a5333c4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663519457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febe9c8db2a7faa33ba9910587878d2cfa10d40b310ac1ae5670ee2c002718aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Mon, 06 Oct 2025 07:06:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Oct 2025 07:06:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=379c3771ab55d7c9c62cfb52c5ca47d19452e042951560a73e3bc3ba2b13e5e4 NEO4J_TARBALL=neo4j-enterprise-5.26.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 07:06:58 GMT
WORKDIR /var/lib/neo4j
# Mon, 06 Oct 2025 07:06:58 GMT
VOLUME [/data /logs]
# Mon, 06 Oct 2025 07:06:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 06 Oct 2025 07:06:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b2beb0cf597f27a9b89b7eb3f7f614e4167f2e6b5ac4b102d1b2a0844561f6`  
		Last Modified: Fri, 10 Oct 2025 03:32:30 GMT  
		Size: 143.5 MB (143542163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc1e4c5bd40d3f3c09665bc11d0a20804da5d40c98254bcfe2ef45786491596`  
		Last Modified: Thu, 09 Oct 2025 22:20:01 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46939cc2eb3037b0d8ae57f9890a845a6af0ab1ee827c7bce316072faffbdd63`  
		Last Modified: Thu, 09 Oct 2025 22:20:02 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b85283e823831e62f9c7203830348480ad5576bc3a9dba0bd1ff9222bcc1408`  
		Last Modified: Fri, 10 Oct 2025 03:32:59 GMT  
		Size: 491.2 MB (491214904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a944d89debe3f1f66b18b95c440587c55b8958c9467bcd1d342b3faebeb22b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e808a9c0bc5acc50dc7c36421d809c21d4730d146728f757b89e35036227ea99`

```dockerfile
```

-	Layers:
	-	`sha256:f148c9f7b64d414ff51fd8b4fcd9d35bc7f9f0a97fe56af1eb6a37e0fd6eb0d7`  
		Last Modified: Fri, 10 Oct 2025 05:44:58 GMT  
		Size: 4.8 MB (4829295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2c5564d4a104ea05b8a8be65b5ad06b1402da54e02fbbd5d21d18606f2ef34`  
		Last Modified: Fri, 10 Oct 2025 05:44:59 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json
