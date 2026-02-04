## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:2dd50c40a924ba62b977a195555f5574cc715c3f7df267a482545680ecaa9686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bbf4e98327dc68f39e9d6eada786f9912867eb47b4215b54e6b68018935bdd7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.8 MB (683771014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eb58002e3bacad47a3d1a26c9b0ac4fb84afc8fbc771233c9bd28eacc954c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:10:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:10:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:10:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=053f019a4a5854e7676b7339bfc0f554091bf35d6be9f74a79e503480b0b7bda NEO4J_TARBALL=neo4j-enterprise-5.26.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:10:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
# Wed, 04 Feb 2026 21:10:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:10:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:11:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:11:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:11:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:11:25 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:11:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:11:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:11:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5614ed8eb38a6630e266a9db007221bf439b1b4202c728e9bef2a87d03fdeb`  
		Last Modified: Wed, 04 Feb 2026 21:11:59 GMT  
		Size: 144.8 MB (144847977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea475517a805a35c05a1607f50b5070058218c4be0c655520fc0628a6f03e62`  
		Last Modified: Wed, 04 Feb 2026 21:11:54 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0702161e7590bd102b220823fda43019e531f899e3c607b586881d7fe8edfb29`  
		Last Modified: Wed, 04 Feb 2026 21:11:54 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2244df6323f4865fdad73fe6b7a74344dcd3a7b242dead4134aa81fb4b379217`  
		Last Modified: Wed, 04 Feb 2026 21:12:07 GMT  
		Size: 508.7 MB (508650640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:43662ed4abdae5a9463dd61cad76d579407fdcb98d85ca49bbea14f6a75ae291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4866313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4073de93787405ea834a495946c736a3675688f67df0c786475e8e5342b76cc8`

```dockerfile
```

-	Layers:
	-	`sha256:0cb74af277641bc4984f81653e50e2bd896ec21fef1f683eb6bb7f72d4ceb499`  
		Last Modified: Wed, 04 Feb 2026 21:11:54 GMT  
		Size: 4.8 MB (4846270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea09dbc0ad639a3aac43f9a05cc7c1b966904ed13e32e31dea5cb60d64c8dee`  
		Last Modified: Wed, 04 Feb 2026 21:11:54 GMT  
		Size: 20.0 KB (20043 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b182bc3f149cdd1d4da0ce0dbad04865bdecb0be5d7c8225a37ee4d25fed660e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680333030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a509728d77116dcb4190f0f3eeff8dd9db75e631ee6cadcfa1034d25b229df42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:08:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=053f019a4a5854e7676b7339bfc0f554091bf35d6be9f74a79e503480b0b7bda NEO4J_TARBALL=neo4j-enterprise-5.26.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:08:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
# Wed, 04 Feb 2026 21:08:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:08:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:08:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:08:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:08:50 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:08:50 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:08:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:08:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:08:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef01185f2140b9206b5c98b3501e59db78fd767c7e06fbe8afccfbe9611a5cc`  
		Last Modified: Wed, 04 Feb 2026 21:09:07 GMT  
		Size: 143.7 MB (143679941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2295fae3bb9f66fdea0080e85f66dd4db4cb8dec4532e1841dbfe31b349b1d`  
		Last Modified: Wed, 04 Feb 2026 21:09:21 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5de8d1932b49a517c69d4c22a060c4a895a3f6e22b2620d59c0d8ca4227598f`  
		Last Modified: Wed, 04 Feb 2026 21:09:21 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41b36c971dafb5b2400450296c31d924a88d5da2cb9b6c76d6047b89f4fb90`  
		Last Modified: Wed, 04 Feb 2026 21:09:34 GMT  
		Size: 507.9 MB (507894506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e510e1675955318a0a944ff13c471449d2db3fb0520e92ad1fac748214d00c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fb21cc02f0830ea83bb9068b76d9005f20bcc3af6eec403ead4446e0bc09a7`

```dockerfile
```

-	Layers:
	-	`sha256:2e15a8ceb9fc711c8fc5b853ad5879b6d839e9073883df04c969dcad47bc762a`  
		Last Modified: Wed, 04 Feb 2026 21:09:21 GMT  
		Size: 4.8 MB (4820039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb93562ce6ae0daf9f63c42ecef503fc1f13f52bc0c74b41cf8e69cb532ce8`  
		Last Modified: Wed, 04 Feb 2026 21:09:21 GMT  
		Size: 20.2 KB (20176 bytes)  
		MIME: application/vnd.in-toto+json
