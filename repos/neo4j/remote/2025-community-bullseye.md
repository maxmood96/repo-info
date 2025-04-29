## `neo4j:2025-community-bullseye`

```console
$ docker pull neo4j@sha256:2900f8e4fd8e39a9ebfa4cdfc589694d8b202f48cf628afdc1ca659636ac59e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d268b83bf692bc3f2348d6bb29e7796d51c3f3c19c69ea59760cb42fa624bb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349006799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae33071afc35d5c8c4a1a5b0486b55ebe913bd45132120fbb4710ba92b37fc52`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Mar 2025 13:20:50 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 27 Mar 2025 13:20:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 13:20:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2908b0d901574a5b484aeba06c3744aea79a46d2cd9d5e538344d9e0ec9a6b2a NEO4J_TARBALL=neo4j-community-2025.03.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.03.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.03.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:20:50 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Mar 2025 13:20:50 GMT
VOLUME [/data /logs]
# Thu, 27 Mar 2025 13:20:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Mar 2025 13:20:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Mar 2025 13:20:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0019ac834e1725d34d1a91b6b94fb2e3704add7f269cef070945fc439c1005`  
		Last Modified: Mon, 28 Apr 2025 21:57:01 GMT  
		Size: 157.6 MB (157634490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615e3115e6691264795c7e3f195891036c9cd48723f8b697cb5a02737c0e6cf5`  
		Last Modified: Mon, 28 Apr 2025 21:56:58 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b619719d57b69f061934126c29e325a17bc0833d97957d9fda1ff5b81da6f6`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3c2306ddf4dc114ed4129bf9f9249c89094c62a16f023f96fe14d08b929916`  
		Last Modified: Mon, 28 Apr 2025 21:57:02 GMT  
		Size: 161.1 MB (161103810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c7d17682121e215cee6bb7b5dcf8151db37726b3f4b8e7cd6c8342273a5ef9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3268673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440ffa57189ab0d3e1250bd8f2f5edc230ea8163fc4dc29aeff6ebb605e13e49`

```dockerfile
```

-	Layers:
	-	`sha256:a0d7f6302511224a7259da637d23f17df7a0e19ae6616ae4d3e3b2c02c003021`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 3.2 MB (3244819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96bfa3f304dcf7516aeef7c4a0d91ae8bb07c5ee747f226a6ea29bd5e670046`  
		Last Modified: Mon, 28 Apr 2025 21:56:59 GMT  
		Size: 23.9 KB (23854 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:aee479afc910256f296d9c13bbd658daa8598b3c05a7a630f1d19087b239b00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345754040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a009272ac1ab4cf04c551cdef88a8e2661dcf912c99a956b5482c9a85891196`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Mar 2025 13:20:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 27 Mar 2025 13:20:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 13:20:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2908b0d901574a5b484aeba06c3744aea79a46d2cd9d5e538344d9e0ec9a6b2a NEO4J_TARBALL=neo4j-community-2025.03.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.03.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.03.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:20:50 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Mar 2025 13:20:50 GMT
VOLUME [/data /logs]
# Thu, 27 Mar 2025 13:20:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Mar 2025 13:20:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Mar 2025 13:20:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e90da1b2c2f39d3d6303cf5e3f5fbf94813274320d4f5340fe5d95158edc986`  
		Last Modified: Tue, 29 Apr 2025 02:11:05 GMT  
		Size: 155.9 MB (155928833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816b5923996b4db30d412207e84b34c84d0457ecb5a2c776adcdf299adf2ca72`  
		Last Modified: Tue, 29 Apr 2025 02:11:01 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384e7dd56033ae516933b7c67e4c23d40b440182f384cbd938f31466b78a306c`  
		Last Modified: Tue, 29 Apr 2025 02:11:01 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f19e4e2eb73c75eb9955960c93c2adb4dcec1a8fe4feb4f7b20d33947cfcf9`  
		Last Modified: Tue, 29 Apr 2025 02:11:06 GMT  
		Size: 161.1 MB (161066637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:62a4a3a4e7470ea077df50234f56ee19e82274023dcbdf6e01061b8eb776bae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3268752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140fda2bbb966b39d2aa25481bf0436749716f77d259dc406cb99f9f6dfd8dbc`

```dockerfile
```

-	Layers:
	-	`sha256:550c51a2420f23718ae361b1e2577913d69a40d981a9f9b0367e2263ed16a28b`  
		Last Modified: Tue, 29 Apr 2025 02:11:02 GMT  
		Size: 3.2 MB (3244609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f4505b1eb1e83c2a45a077d4034e15fcf7cd1c23a60c21221bae664fc28366d`  
		Last Modified: Tue, 29 Apr 2025 02:11:01 GMT  
		Size: 24.1 KB (24143 bytes)  
		MIME: application/vnd.in-toto+json
