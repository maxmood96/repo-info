## `neo4j:2025-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:dafccb2b80e42eafa8a3343132fe5691241509c1ac3c4e34da51e6a9d0aa0545
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8a780d1859bac7c2d57542eb3ffb4b0633dce5720385c09c1d77aaf0ff9536e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.3 MB (509258401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72e2a09b35014e468d1de8c5850292e14276f4192dcd71906da72d81347f5a0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Mar 2025 13:20:50 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Thu, 27 Mar 2025 13:20:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 13:20:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=39d74d8f0e1f6d31a3ab459a2548f8c66eff86678bb141572513c6f68f893d45 NEO4J_TARBALL=neo4j-enterprise-2025.03.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d497810db2bf289a816fa7e7b6c3a22df9f5134a7c0de1033b4f70397de72520`  
		Last Modified: Wed, 09 Apr 2025 02:15:06 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d9de9c08b8771b60ef0b9a35612fd1246c5e9617964bbe901be90a3ce0fa0f`  
		Last Modified: Wed, 09 Apr 2025 02:15:03 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4854ebb2e70600839070113aaf1a1d9050170de5d71497c94e203a4286f35a2d`  
		Last Modified: Wed, 09 Apr 2025 02:15:03 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b128d06ef88cf0e037cdd6c30d6525c0ba734cc919b4838ba82bbf93e96098d`  
		Last Modified: Wed, 09 Apr 2025 02:15:09 GMT  
		Size: 321.4 MB (321401187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f1e4d68e843c08bc5ffd80fd2ade8416aa361404b580d3e296f05d9174cae1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bad36b8fb2cfd1dbaa52f8dc8d8cce3a6ec41b5332f703b31a2ce9e3baba1a`

```dockerfile
```

-	Layers:
	-	`sha256:d8a23de3776bce1ba795c71babf9f5c71881c3d0916c4b0e9387469d884bf807`  
		Last Modified: Wed, 09 Apr 2025 02:15:03 GMT  
		Size: 3.5 MB (3539743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fea5141c6e60f2ae028f8a241b7edecee33921353c7de2792d2b9da41b2c05`  
		Last Modified: Wed, 09 Apr 2025 02:15:03 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:aaeeba9625c9aefbdd9615be6453c70145d5d703c9e900f31d5b2b308dc7c8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.0 MB (505990993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95194bccbe32f5d00d83e20e22a019755f5fcce260f11ad783e032b7e8b183fe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Mar 2025 13:20:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 27 Mar 2025 13:20:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 13:20:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=39d74d8f0e1f6d31a3ab459a2548f8c66eff86678bb141572513c6f68f893d45 NEO4J_TARBALL=neo4j-enterprise-2025.03.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3092970dfc6ff6b5baaf45f0ff4fdbdd2c181b6e2eb0565cc8b269a2c08eb8`  
		Last Modified: Wed, 09 Apr 2025 15:16:05 GMT  
		Size: 155.9 MB (155859263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158fe5c744a629704afd0e2e6e42bbf155462448b58121d7a6801e225275dbfb`  
		Last Modified: Wed, 09 Apr 2025 15:17:14 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722fe16fe8f4c93bb549d9c6a342d4ae1d8dd44bf7bbec4e7ff22bf6584cec74`  
		Last Modified: Wed, 09 Apr 2025 15:17:13 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb943da62aa8cba3d0b78e9b6bae3e54cac5be7110940b59f40656e31a32089`  
		Last Modified: Wed, 09 Apr 2025 15:17:20 GMT  
		Size: 321.4 MB (321368301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:73dd67c82eb6c7b4293729a1ccbe7acff7c35db99b20692624d71433c7054095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52112328b3e91fcdbf9295c532065787f45329741bbbb88396cc38ed10cb4e57`

```dockerfile
```

-	Layers:
	-	`sha256:1420fd0f06b84530af343afdf50556b597213c46331f7f566cebb7a25a532732`  
		Last Modified: Wed, 09 Apr 2025 15:17:14 GMT  
		Size: 3.5 MB (3539437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f8c9abeae080615aa4a4748712614f076228a7bc9663eb61c246a9ac56a9bc`  
		Last Modified: Wed, 09 Apr 2025 15:17:13 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json
