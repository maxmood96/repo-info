## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:8502ed892877645fbba02dc25203d843d319a0b8934a881ecb6d046200bcac32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fcc7702a3fe5455dbac537261e897a4cf0956f6faa7154788b8cc8dca328ed4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650195532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaf6188ae29d528dcd6646a225369a970567a6d7b2115ae52f78f1ebfef6591`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 04 Sep 2025 06:40:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Thu, 04 Sep 2025 06:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Sep 2025 06:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=15a484a00722e15893250d9a071190cd97309cefb7c85bcb3a2e69d3764fa447 NEO4J_TARBALL=neo4j-enterprise-5.26.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 04 Sep 2025 06:40:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Sep 2025 06:40:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Sep 2025 06:40:51 GMT
VOLUME [/data /logs]
# Thu, 04 Sep 2025 06:40:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Sep 2025 06:40:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 06:40:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a82decd02f9f32dce18f5813652660a96a395e650ea731a6c021a69962284`  
		Last Modified: Tue, 16 Sep 2025 02:48:45 GMT  
		Size: 144.7 MB (144693569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4338e0d769a9d8187185f411d86ebb22a7371a42ea54c468a7dd1439de3ccae`  
		Last Modified: Mon, 15 Sep 2025 23:19:47 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d762f84176af80b09c719031b7575b232e8a86bfa12d07dcb58147a6e4413b`  
		Last Modified: Mon, 15 Sep 2025 23:19:48 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd9affbf4acb2e4c035ca5d2a333da0c976dba538530ff107f18edff11d0241`  
		Last Modified: Tue, 16 Sep 2025 02:49:28 GMT  
		Size: 475.2 MB (475231959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:086dcc2fede05346bbdb5499859c522dfd99a1eb22ff7f33cad821f00eea7347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0be523134ae1b3bf4a0bb784a1c11fb8e6201da9e730ce0e33e4739ae66dbe`

```dockerfile
```

-	Layers:
	-	`sha256:47fafdf6daa8811548d1e4bb5ebecbfc0e88330e452124a6cc31589621440522`  
		Last Modified: Tue, 16 Sep 2025 02:44:47 GMT  
		Size: 4.9 MB (4854954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff8c02a6f74c16317df74738f2528522f42a3d3754b3a0941cd44aed9384885`  
		Last Modified: Tue, 16 Sep 2025 02:44:48 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:900271bb01c5d579c0946392ccfd408886143ef174b989184f3df3aadd94c982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.8 MB (646782536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d552dd607c9e43068ba4f52c8c395ef58806b21f6e5cdd4d34c3d9bb1ac2c4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 04 Sep 2025 06:40:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Thu, 04 Sep 2025 06:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Sep 2025 06:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=15a484a00722e15893250d9a071190cd97309cefb7c85bcb3a2e69d3764fa447 NEO4J_TARBALL=neo4j-enterprise-5.26.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 04 Sep 2025 06:40:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Sep 2025 06:40:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Sep 2025 06:40:51 GMT
VOLUME [/data /logs]
# Thu, 04 Sep 2025 06:40:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Sep 2025 06:40:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 06:40:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56ed7075a448667e9eb38709506ebc6936b3a41d79ab6f6782e01bdfafb19b1`  
		Last Modified: Tue, 16 Sep 2025 04:24:26 GMT  
		Size: 143.5 MB (143542121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3f8ee14ed2942ad8b5599aa9398bdcf2c04c9b8416e20fc81a8066489b48d`  
		Last Modified: Mon, 15 Sep 2025 23:19:45 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9174120f1b724e39efd8427c15e1f6070d1e58187e4a0ca05f2140879bfcf58f`  
		Last Modified: Mon, 15 Sep 2025 23:19:45 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72adbc14174be2de1c0ea9b5e90f6f5b0fef30e33ee675f6a8783deb8686498f`  
		Last Modified: Tue, 16 Sep 2025 04:24:34 GMT  
		Size: 474.5 MB (474475993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7540be8143b89fa583312d269500db43fe9594a21c605ff7a610fd6d7e19761c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4849956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556c97a907e0e2d2e88ea1960370addeff1fa2bfb33418889deded9b170183e2`

```dockerfile
```

-	Layers:
	-	`sha256:a87e4ff1d26e6161fe6b8e55466a88722688bded8b84b8ea0af60462ea319656`  
		Last Modified: Tue, 16 Sep 2025 02:44:53 GMT  
		Size: 4.8 MB (4828759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:006e61a410429638742b272bb792d2a04584651c53af188ae60ec6a33f51473f`  
		Last Modified: Tue, 16 Sep 2025 02:44:54 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json
