## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:82dac8cdd62600690d502fc6c1d4fa5002d9109c705acc792671b03c5c5ab275
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:685e6e807d98b47731bd2eecdda674c09cf93b840814a35c016ad884fde039c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.3 MB (547269108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c740e89218c50a856af77e0b0c884c0583afcfa920dc36402543ec2b31992c1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 00:37:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 00:37:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 00:37:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=22fe6ea9bb332e5a1250b0fd1c226539e0a4babec699e0b1e7d2aa5043f65e05 NEO4J_TARBALL=neo4j-enterprise-2025.11.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 00:37:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
# Fri, 16 Jan 2026 00:37:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 00:37:59 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 00:38:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 00:38:23 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:38:23 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 00:38:23 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 00:38:23 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 00:38:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:38:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f641b1edd9e8d522d51af67e108dfc77aef2019d7a37c3f6265e14856786939`  
		Last Modified: Fri, 16 Jan 2026 00:39:17 GMT  
		Size: 157.8 MB (157826001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4821351039431040ee20ad4d1dd16b8ff5a92d31696f158e4cd2a5b0a40b0d`  
		Last Modified: Fri, 16 Jan 2026 00:39:04 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78c1d0e23a1e7257f8041288608a2fc019bc0305f2f9a00ef2907091bceb4ac`  
		Last Modified: Fri, 16 Jan 2026 00:39:04 GMT  
		Size: 10.0 KB (10017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6815919a7e4aa6bdeb9718dee410e472eeba8cb9358a4a0dd4a15f58ad28d1`  
		Last Modified: Fri, 16 Jan 2026 00:39:34 GMT  
		Size: 359.2 MB (359170721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e12415f3993d05ce77ba41a7be6f07c777ff6fc00616c5907618906fddbbbe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4868421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de10dc73bd560b52140de677ea67c14d45205b145acf3fa5fc7f90c5f6c06836`

```dockerfile
```

-	Layers:
	-	`sha256:bc7f3f1ed5e8305262fa307e80a47dd80564084d8b2513d36e907f894353088a`  
		Last Modified: Fri, 16 Jan 2026 03:43:41 GMT  
		Size: 4.8 MB (4846760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975d1396cd5288ab2f908f44f7d425f048bfb50816e0cf9706a7406a5c4db869`  
		Last Modified: Fri, 16 Jan 2026 03:43:42 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:237755af86760eac26cf2fc16452c144ee5d60b98639216a079984b2ba1d9aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.3 MB (543285337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942934f450adb56be1b67980cf219a379045c302392cb98c38d74faf377b0904`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 00:40:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 00:40:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 00:40:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=22fe6ea9bb332e5a1250b0fd1c226539e0a4babec699e0b1e7d2aa5043f65e05 NEO4J_TARBALL=neo4j-enterprise-2025.11.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 00:40:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
# Fri, 16 Jan 2026 00:40:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 00:40:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 00:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 00:40:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:40:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 00:40:32 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 00:40:32 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 00:40:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:40:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116c2c64440796ef4fdb0c4931a657d7d4188d401e9d952ce6aa7635fb068088`  
		Last Modified: Fri, 16 Jan 2026 00:41:04 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e635f424c8253853b9018ffb3c59afd12045ac20f130b5906314068cd2aef51d`  
		Last Modified: Fri, 16 Jan 2026 00:41:13 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd3cacd80940479cc59eed853c29ba6193ee83b75323f9775b03f7edb0ffbdb`  
		Last Modified: Fri, 16 Jan 2026 00:41:13 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6534d8a8123dc24a7d94ea3778685b80c66e59aca6b2502ddaf46132305b8`  
		Last Modified: Fri, 16 Jan 2026 00:43:24 GMT  
		Size: 358.4 MB (358415262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:83eaecd720e8db4f78dea923ed0c4e36f3eb9dea204a769e0c38b8e9c879bf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4842442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0af08586730b8573f461f5d5b56a57055dcedd80d0f85c1a29ac3cae20d01d4`

```dockerfile
```

-	Layers:
	-	`sha256:ee4b2bed937a15523b7762d48198cafcdae18b12b125da04d1c9828bffb0f1d6`  
		Last Modified: Fri, 16 Jan 2026 03:43:47 GMT  
		Size: 4.8 MB (4820589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b3f0688f595324eb99f19608e235e439e7a76ec71e3edf9f1af936e97dea37`  
		Last Modified: Fri, 16 Jan 2026 03:43:48 GMT  
		Size: 21.9 KB (21853 bytes)  
		MIME: application/vnd.in-toto+json
