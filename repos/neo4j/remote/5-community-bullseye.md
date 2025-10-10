## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:645e051c5911e0b4a7394d28b537dc72533f40facc8b7f985d1eae2466e06ab0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0eb5aca0fe409819b89b042c70c035b69dc6559350a70f80d7e82d18347fd9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305696357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1944b1e56441667b886a7b61802603bcaa3aa98ebf3b6ef108272d580264edd`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=670888ac88010ddb09df8a82b3f9f3552f03b16e8197e5855110aac86fe36f35 NEO4J_TARBALL=neo4j-community-5.26.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
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
	-	`sha256:455686758de8025e29c2bc644c06328326270fc7d54842ac5a2ffc6212388fcb`  
		Last Modified: Fri, 10 Oct 2025 05:45:00 GMT  
		Size: 130.7 MB (130730776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e3d7b5fb5e6012fd17656ba08ca82593ad7912d81737f14966ca2e3f5e7c3d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4507383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57459168747abcdd4a42f890991046c2d731a20689398f2bed290db818438ad`

```dockerfile
```

-	Layers:
	-	`sha256:4b62cc8c221234ec7924e7f622bd1f6ef0f5f0e713025a5818ed3a73f0f33039`  
		Last Modified: Fri, 10 Oct 2025 05:44:38 GMT  
		Size: 4.5 MB (4484574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2fab099a4a4efb723939b223003bd10e862ef33012684b3b234b366b6ae285f`  
		Last Modified: Fri, 10 Oct 2025 05:44:40 GMT  
		Size: 22.8 KB (22809 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fab7c5a56c74e27fbc320db642bb37707d1314100e5dedd8579babae2f9189d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302279704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986691a30836792620625dd77b02ff0b1c01a6921110364b0bc25d26b97823de`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=670888ac88010ddb09df8a82b3f9f3552f03b16e8197e5855110aac86fe36f35 NEO4J_TARBALL=neo4j-community-5.26.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.13-unix.tar.gz
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
	-	`sha256:b5ff0d57d243d153fbe35dcea3bd8b14cb3a954b142fc01e781869ef2c5d383d`  
		Last Modified: Thu, 09 Oct 2025 22:19:16 GMT  
		Size: 143.5 MB (143542159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ab3b028ccb6fe1a9d4d4c055bf6cd0ea10b00bcdd5714bcec38da42ff5b589`  
		Last Modified: Thu, 09 Oct 2025 23:01:22 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecafb4ae60224f52ded44067a7a6196155b41c74ad8b97260578a6d9f7f6d3fb`  
		Last Modified: Thu, 09 Oct 2025 23:01:22 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e403b17590cc700352fb3c83b6a4da6ed78fa7b3f9c899a493661e23ad1fdf`  
		Last Modified: Thu, 09 Oct 2025 22:19:16 GMT  
		Size: 130.0 MB (129975153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:365bd3158dd3ce5dddf9b4ef4b3f0c039bc45620d799106500aa1bc6f327ea31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938ec542cfa2eb48d8caa45ad62d02c4a341861a8fffee1a687680b6de5e41df`

```dockerfile
```

-	Layers:
	-	`sha256:4df6f6b7e05d834ed81f3a013fa763c1f4921e519389639cc3e920913a854bb8`  
		Last Modified: Fri, 10 Oct 2025 05:44:44 GMT  
		Size: 4.5 MB (4458451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1015270275911023a8ad84b3c30661bccd78c2f9564892ee49c206596f27db71`  
		Last Modified: Fri, 10 Oct 2025 05:44:45 GMT  
		Size: 23.1 KB (23050 bytes)  
		MIME: application/vnd.in-toto+json
