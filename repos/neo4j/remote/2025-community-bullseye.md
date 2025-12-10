## `neo4j:2025-community-bullseye`

```console
$ docker pull neo4j@sha256:155c8aad10d5c838bc3bbc476c0418779086547822acb214ec5e3d49ba336907
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:50f60e043049e3c15c3d3906e13a5b9ca1182488f49cd6038565a3ebf7f079f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401733268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff6e5ba92302482483cb07e6278ed76511ca6692acb93a4df3df07d1fea88ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:11:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:11:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:11:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Dec 2025 23:11:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Mon, 08 Dec 2025 23:11:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 08 Dec 2025 23:11:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Dec 2025 23:11:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Dec 2025 23:11:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:11:57 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Dec 2025 23:11:57 GMT
VOLUME [/data /logs]
# Mon, 08 Dec 2025 23:11:57 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Dec 2025 23:11:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:11:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477c5c8acb3e9b7ac3b17b889f0959456c2ff1f5bc9f0292697c455814f15d2`  
		Last Modified: Tue, 09 Dec 2025 00:45:08 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e97f1658ceba0c6b1da86f5d45a431b03216e6f0bcaba12bf422a035f811d5e`  
		Last Modified: Mon, 08 Dec 2025 23:12:32 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0a437b0654cd90aa9c559490d3d0ace9ad8d830f8d9bb12544d65da05dc2b0`  
		Last Modified: Mon, 08 Dec 2025 23:12:31 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7367f0c01a0724bda2e153dedf1287f84170c55fac1b92b64ace8ff277bdf46`  
		Last Modified: Mon, 08 Dec 2025 23:12:58 GMT  
		Size: 213.6 MB (213634886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9eab35f3172ae3fcf48c12b25982baf709fbc4879666ceda3364fdde55d771c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4630359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1209a9cb718117f8eed78c39a12778aff9cdea37947d2a525e653f7945cc5a9`

```dockerfile
```

-	Layers:
	-	`sha256:f3486482bfc2823ef9432e4331f73fc78d419d25a254e83d7046f373a8451e43`  
		Last Modified: Tue, 09 Dec 2025 00:43:31 GMT  
		Size: 4.6 MB (4606293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec34f8f5b3659c515572c2013bc3651f52128825589dccac8a17c54f405d4b99`  
		Last Modified: Tue, 09 Dec 2025 00:43:32 GMT  
		Size: 24.1 KB (24066 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a19e0f9e0ce9e4f94a9ae615f36f3add16156c28092fee6a4466c9bda6b9c155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 MB (397746766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f22ac5e3d8567381cf1dae44fc48c37729ae895585e00ed6c1904162a45710e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:14:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:14:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:14:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Dec 2025 23:14:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Mon, 08 Dec 2025 23:14:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 08 Dec 2025 23:14:42 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Dec 2025 23:15:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Dec 2025 23:15:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:15:02 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Dec 2025 23:15:02 GMT
VOLUME [/data /logs]
# Mon, 08 Dec 2025 23:15:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Dec 2025 23:15:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:15:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ceffc7422f4dd238f84ad273ff57e70f420e0953dc4cc981a24d9d40851ebd`  
		Last Modified: Mon, 08 Dec 2025 23:17:30 GMT  
		Size: 156.1 MB (156107625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a176348cbfcc67577d701b2369e174b60d8436b34f883cc2dfdd850c765ae1`  
		Last Modified: Mon, 08 Dec 2025 23:15:39 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d10c853cc3e8c0dc56d02c5e33d8e015c9a3bde1c6f70e2e85f81db9647475`  
		Last Modified: Mon, 08 Dec 2025 23:15:39 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192e02efde2492b5358247eba5ed011768cadbcbfe6a76337e457d8f6fd95419`  
		Last Modified: Mon, 08 Dec 2025 23:15:48 GMT  
		Size: 212.9 MB (212876742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:66317aecdb014f0e87188b57bf58cb287e5d981a1a9aa56e0aad2920d7d6b884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6787e402470b2b11b026202f2a06e17cae122f38c52b086df23e85294fe31c74`

```dockerfile
```

-	Layers:
	-	`sha256:f09586f84086595cb0410bc84855847b817a01dc4058471f8fa509f2c5791c33`  
		Last Modified: Tue, 09 Dec 2025 03:43:28 GMT  
		Size: 4.6 MB (4580218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7713ef92916829260101bf4e8f359df350893c5bc4fa34c525961ff1ef4c1fb0`  
		Last Modified: Tue, 09 Dec 2025 03:43:29 GMT  
		Size: 24.4 KB (24355 bytes)  
		MIME: application/vnd.in-toto+json
