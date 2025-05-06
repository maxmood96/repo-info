## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:5878e533971f2fee1ce27cf51eb173cfd7d833c4038089f128a315bcc4b3414e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:48ed4fc4e9c388b38fad34b00bb58d3f08363614900a7768f4e0c699b8291526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340419711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b787c69b8b24a9699bae6851c854ce0ebd652c8ca5a5f5b463dd5e83b79b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 02 Apr 2025 06:15:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Wed, 02 Apr 2025 06:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Apr 2025 06:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6e53caa88fa871c9c2b5c887a54f86cf38f2e7cb8da718cd411a402cf5f59784 NEO4J_TARBALL=neo4j-community-5.26.5-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 02 Apr 2025 06:15:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.5-unix.tar.gz
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.5-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.5-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Apr 2025 06:15:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Apr 2025 06:15:25 GMT
VOLUME [/data /logs]
# Wed, 02 Apr 2025 06:15:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 02 Apr 2025 06:15:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Apr 2025 06:15:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32393d4d9d1a410e0b3b19379bc5323f4d177b2bfaacac53630b6364256d9561`  
		Last Modified: Mon, 05 May 2025 17:04:30 GMT  
		Size: 144.6 MB (144634985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dce10b374f10b8d4e1a844da16c9618ce2335153100eb8bc862874c275ef0a`  
		Last Modified: Mon, 05 May 2025 17:04:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29344c22f1ea39c4742910841edbfc425738feecd966fa3cdd5a8a16d21fcb72`  
		Last Modified: Mon, 05 May 2025 17:04:23 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7ce074632c0371758f17ad51c24e44f16e1b7b7cc514bc24b05b4b6c2b1762`  
		Last Modified: Mon, 05 May 2025 17:04:29 GMT  
		Size: 165.5 MB (165516220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d3567d89fd05bfe3c64594b31c701ad480ccaf0e12c823f79b62d546cd6e0b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054a6b09ab3ca355c1568f21329855420fcf8a8397334b2001432b712e8f755`

```dockerfile
```

-	Layers:
	-	`sha256:65ad4bf928f63ba5579f7a2d01c30d3bcc448bbba7cba039eab07ab971fad6c8`  
		Last Modified: Mon, 05 May 2025 17:04:24 GMT  
		Size: 3.2 MB (3241721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90710cfa47147a07115698db30e683bfa9c1d13fcc1b1d5c263a1571a26ddc7f`  
		Last Modified: Mon, 05 May 2025 17:04:23 GMT  
		Size: 22.5 KB (22535 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6d822176b69fdea4f8b0271df4c380b4d8a102f133a96b83f5d91673d0e94996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336965431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b7469648aeab6ba8b49a43a3fdb51c708521d52a8d46ff8cd758b31350e43b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 02 Apr 2025 06:15:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Wed, 02 Apr 2025 06:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Apr 2025 06:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6e53caa88fa871c9c2b5c887a54f86cf38f2e7cb8da718cd411a402cf5f59784 NEO4J_TARBALL=neo4j-community-5.26.5-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 02 Apr 2025 06:15:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.5-unix.tar.gz
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.5-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.5-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Apr 2025 06:15:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Apr 2025 06:15:25 GMT
VOLUME [/data /logs]
# Wed, 02 Apr 2025 06:15:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 02 Apr 2025 06:15:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Apr 2025 06:15:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ae675387ee815f1cf9a4635844bb9773f6f4159669c6ceed3939975ea5d1a`  
		Last Modified: Mon, 05 May 2025 22:03:24 GMT  
		Size: 143.5 MB (143512640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcab254f67efae81e97a695dd4beb8b3e3307f42fc5e2c6c6624e56ebab533b`  
		Last Modified: Mon, 05 May 2025 22:03:19 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68dfb5cf67019719ffae710cd8fd16b522570d4f502d91ad13c6ff760b2b4ca`  
		Last Modified: Mon, 05 May 2025 22:03:20 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eb9d95264e6554191fd3096a3b7642ffdbc1e9ba2b3847b9e134cabd339942`  
		Last Modified: Mon, 05 May 2025 22:03:24 GMT  
		Size: 164.7 MB (164694224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:87550b6f7ed2b655878a579d59ef317ed1d67a047f38a1995cd1b38178fb20b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b78919b1a77c7fd44a32a4659ed11c791a85f8f7a33eccdf7597cc7c5cdb18`

```dockerfile
```

-	Layers:
	-	`sha256:01d5525c0791978912bfc12e2ff1c905d79719d32113961942d2a087494f0c0f`  
		Last Modified: Mon, 05 May 2025 22:03:20 GMT  
		Size: 3.2 MB (3241463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8532d002bd00485468fb85ded8074294506415581642fd952098291daaf89b56`  
		Last Modified: Mon, 05 May 2025 22:03:19 GMT  
		Size: 22.8 KB (22776 bytes)  
		MIME: application/vnd.in-toto+json
