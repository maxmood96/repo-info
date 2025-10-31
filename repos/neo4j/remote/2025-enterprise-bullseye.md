## `neo4j:2025-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:3e645ef464425a12d4706d3f757425317c8bc05d8e9275582ed4a48269c8a37a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bbeb84b59747c9c0fc4f152a8ce00efea25f24feb5e3634ee9be588e2ba5f714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.3 MB (544252857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1654243f24590bfec452ebbcf31478e802d2931f0bf831c99b4686fcba2058`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 20:49:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Oct 2025 20:49:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Oct 2025 20:49:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6ddde9170f21067bde1dbb3f910d6f5faddf48026177e3c43d1410d4b5cd3b76 NEO4J_TARBALL=neo4j-enterprise-2025.10.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Oct 2025 20:49:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
# Thu, 30 Oct 2025 20:49:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 30 Oct 2025 20:49:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Oct 2025 20:49:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Oct 2025 20:49:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 20:49:34 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Oct 2025 20:49:34 GMT
VOLUME [/data /logs]
# Thu, 30 Oct 2025 20:49:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Oct 2025 20:49:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Oct 2025 20:49:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700f577e2a41dbcc6082b00bf42d9b0ae73f8d531c9f09df42169e9c039085b`  
		Last Modified: Thu, 30 Oct 2025 20:50:08 GMT  
		Size: 157.8 MB (157804740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c67f932d28334177bd471ad863a2929a9a980a504ef6f67e052044ce1cc3f`  
		Last Modified: Thu, 30 Oct 2025 20:50:22 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b613283dbb0303b5251b7754d47e6b3d9d395de04c0057542191605c8a9f8f52`  
		Last Modified: Thu, 30 Oct 2025 20:50:23 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5be4424fc5d5444a3b40b288fbbba284064a783d59467b5e81c317743c6132`  
		Last Modified: Thu, 30 Oct 2025 20:50:10 GMT  
		Size: 356.2 MB (356175856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e745362a2f3db205a677eeb5ef4d66c6ffdbb1499ea424b62aec77b495cf8283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4873184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e87c612cc996962f791672f4c47aa5fcb282690507fc82d172374954f6ffaa`

```dockerfile
```

-	Layers:
	-	`sha256:c8c90dbeaf7747282f506d2cf9a7dbf61209f449757fd535cd8236910180ac01`  
		Last Modified: Thu, 30 Oct 2025 23:43:41 GMT  
		Size: 4.9 MB (4851523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8f4b7cb8d7a11ccf28ba4c0b5a6ef625034182f95a7217f895ba800936803f`  
		Last Modified: Thu, 30 Oct 2025 23:43:42 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e98641e7470a601cc8e4216a83fa1f47ccd5ab5ef95050c58612e404ce534af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540262418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4467bcb09f720619154f2727fd41980c3856eef6f4cfbe0aa7cb79ef45ef1a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 20:50:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Oct 2025 20:50:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Oct 2025 20:50:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6ddde9170f21067bde1dbb3f910d6f5faddf48026177e3c43d1410d4b5cd3b76 NEO4J_TARBALL=neo4j-enterprise-2025.10.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Oct 2025 20:50:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
# Thu, 30 Oct 2025 20:50:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 30 Oct 2025 20:50:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Oct 2025 20:50:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Oct 2025 20:50:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 20:50:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Oct 2025 20:50:44 GMT
VOLUME [/data /logs]
# Thu, 30 Oct 2025 20:50:44 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Oct 2025 20:50:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Oct 2025 20:50:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d651151550c350914ccf3a3acb898c096d94b92b062b3dc72be5df00e88ebf6c`  
		Last Modified: Thu, 30 Oct 2025 20:51:17 GMT  
		Size: 156.1 MB (156081259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab99895b18e801c8909d3f9261022bfe5b9147acf0f1e9755532b26d3d7f802`  
		Last Modified: Thu, 30 Oct 2025 20:51:27 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608cc2ebef0bb3000fc9dfc0f6b41dc6dfaf4f93f2ef4d72da6fbcfbf3c7255d`  
		Last Modified: Thu, 30 Oct 2025 20:51:27 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e3998bf95a5aeba57ac46f69536c5196a5436a550dec4fc4b314ed027ab360`  
		Last Modified: Thu, 30 Oct 2025 20:51:21 GMT  
		Size: 355.4 MB (355418833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a2579f1af82ff87802164100291b490f225b294b73cacffe13df66c1118f19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4847206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458c85220ec95bd63bd3ea89d96378f8f02638b30aa249a6b792cf7a99035313`

```dockerfile
```

-	Layers:
	-	`sha256:d22774916bede7abc68ad39c95db1c2c6e76c6b369f5ff2e3e1f1f7f7cdf5d77`  
		Last Modified: Thu, 30 Oct 2025 23:43:48 GMT  
		Size: 4.8 MB (4825352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b84a4a4bb94da3b7f78ee9c8b709523a3c6c88e7c0a6500770cd72ec36f5573b`  
		Last Modified: Thu, 30 Oct 2025 23:43:49 GMT  
		Size: 21.9 KB (21854 bytes)  
		MIME: application/vnd.in-toto+json
