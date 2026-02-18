## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:dc58321b1647d04f11c4bed534ccc54455ce1aaef3b58513bb6d36dd880d9610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:bb8f41ccd1648a7fa7caff715285afe5e5a1d20dd323fa6e7a88f28a341c10ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.2 MB (490245072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476e81e819f66e83ada9aa9410f26b6586eef9fc3a5b21fad025eda267ef9579`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 17 Feb 2026 21:24:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:06 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadc078380e583b4f0c914cf7e3acca0a3d4c73e66272729cc6867e5b905f8e4`  
		Last Modified: Tue, 17 Feb 2026 21:25:36 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4a8764f8e7f9c6ea090b1e22633bc0c67cc1b84cff34f6f634d676c49bd9b9`  
		Last Modified: Tue, 17 Feb 2026 21:25:32 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025482e3af921e529bc2a2437a76389f4778af082581870a619f336cd2cb3d8d`  
		Last Modified: Tue, 17 Feb 2026 21:25:41 GMT  
		Size: 368.2 MB (368200135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4fc1c0122621eb9b168fdc994319ecd50b5dbd56b1bd3f0b566ecc01cf53055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4650079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286dd5ec263f6b63473146cdcf93a3dfff6b59b2f7d7e74881411ff592eab4dd`

```dockerfile
```

-	Layers:
	-	`sha256:8769e16b5e26df43dce58d89ec28eb44e3731d6418ed47983a2479c762672d92`  
		Last Modified: Tue, 17 Feb 2026 21:25:33 GMT  
		Size: 4.6 MB (4630116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f64f7a1ffa5e46eadead8d7f9c4222ec5f626356f556cc471c27721920cd36`  
		Last Modified: Tue, 17 Feb 2026 21:25:32 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8549f05b2f42a440df2c4efc8bfc84971d2a479e85566ccf17edf75da32c811a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.7 MB (488714031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d8e8705a2671f4b5a5bc50a6c6e933844ae63c5f4492fa97a975ec666eda43`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 17 Feb 2026 21:24:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:09 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:09 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15c625656a3cf4f264686edb238ae3a4061fc16be8c9971b330340282beafe3`  
		Last Modified: Tue, 17 Feb 2026 21:25:39 GMT  
		Size: 91.3 MB (91288277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0accd94252e69b053cab64083ed5c287d206b416cbbd26da8baa6c674a94d16d`  
		Last Modified: Tue, 17 Feb 2026 21:25:36 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f211738254141ba3b389779801a7de3176b1ed9946caec504325d41e4efe8ac`  
		Last Modified: Tue, 17 Feb 2026 21:25:44 GMT  
		Size: 367.3 MB (367275637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b48a5d33fba1b6cdaadf0bb5c879083f60afbf22566ef34604d7af27a9e8ca6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a071c58fa75d98c7b6291f98d0f7557212b8db1b1dda9cd456dbc1f26ef85cb`

```dockerfile
```

-	Layers:
	-	`sha256:56fbb015bb2b119b354d38cef4f9206b3d7f2ac951d0096b14750859510fe597`  
		Last Modified: Tue, 17 Feb 2026 21:25:36 GMT  
		Size: 4.6 MB (4624591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a45eff6c8be3ad5cca95bc9e03e1183e2a150e82958ce9b2f34a14f1ed93c4`  
		Last Modified: Tue, 17 Feb 2026 21:25:35 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
