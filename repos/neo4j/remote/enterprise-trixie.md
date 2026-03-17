## `neo4j:enterprise-trixie`

```console
$ docker pull neo4j@sha256:dc3b7bdc227f15493f8118563a8031bd0bd2c6d5d48b2b8567a5bbe718b4bdb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:c62e7c266eb5ce3153d09e492ca0876cc30d46106ec8e4e085d4c3e9f7b4fc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.2 MB (511209212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f8b1784d4657bbc46eb6fd2bc9652f288f5d452132740e1eace624c3091d03`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Mar 2026 22:42:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 16 Mar 2026 22:42:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3edc16e54b70b190f460fed9a5eb31e7e4e8c6a52aa823bff6b18dd2d2183c8a NEO4J_TARBALL=neo4j-enterprise-2026.02.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 16 Mar 2026 22:42:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
# Mon, 16 Mar 2026 22:42:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 16 Mar 2026 22:43:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 16 Mar 2026 22:43:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:43:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 16 Mar 2026 22:43:27 GMT
VOLUME [/data /logs]
# Mon, 16 Mar 2026 22:43:27 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 16 Mar 2026 22:43:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f973b6a7d9bace38586167ab7b1beefb6618aad8e0bdf2e87b1f7bf089161d1e`  
		Last Modified: Mon, 16 Mar 2026 22:43:57 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a172ff819370e1f405f913c51e57d0122378e411b01f7d147a91bf9be8abfe`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4e08aacc334832fafaaefd9ad33e0a3faeb1fee8088fe82d9b3af538881af1`  
		Last Modified: Mon, 16 Mar 2026 22:44:03 GMT  
		Size: 389.2 MB (389167344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:a3cb816a6c51f1e901f586b9f7f43b2d2e51e9b34580d258437bc7dc18e1357a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a882fda5086615420cee046641ae5ffc125eedaeb85bb46ff0756a80f43f00b`

```dockerfile
```

-	Layers:
	-	`sha256:918ab878d77bca934d5116fe50bae10ec1998e10f913e225eb1f21417ddbb408`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 4.6 MB (4647177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f634a8880867db874b9ef08eca5530de184f865f1263191eb2fc702dec13b738`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0d173ec56ecb5481abd9fc03751d9cc9aa4333584618e5ff33f1d228dc96297f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.7 MB (509672772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b605028e81b5c20e74b10b812f6c27ddc585c66ff0582b2deeba4ce34ca000`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Mar 2026 22:44:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 16 Mar 2026 22:44:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3edc16e54b70b190f460fed9a5eb31e7e4e8c6a52aa823bff6b18dd2d2183c8a NEO4J_TARBALL=neo4j-enterprise-2026.02.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 16 Mar 2026 22:44:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
# Mon, 16 Mar 2026 22:44:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 16 Mar 2026 22:45:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 16 Mar 2026 22:45:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:45:02 GMT
WORKDIR /var/lib/neo4j
# Mon, 16 Mar 2026 22:45:02 GMT
VOLUME [/data /logs]
# Mon, 16 Mar 2026 22:45:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 16 Mar 2026 22:45:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a160b84115850ac1271e220aacb099b2e0039add7d6213a0193119247b1d32c5`  
		Last Modified: Mon, 16 Mar 2026 22:45:33 GMT  
		Size: 91.3 MB (91288264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bf8cae5f5cc1935411ed48a61647d08863203400973e1f09f3c887bab1f0cd`  
		Last Modified: Mon, 16 Mar 2026 22:45:29 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16054d737366797d923d47a747f075ba868af90ca2ba87e0657bdceacf1e0683`  
		Last Modified: Mon, 16 Mar 2026 22:45:38 GMT  
		Size: 388.2 MB (388236042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:029afe7223daf01d8aa382cbf2e3c5cb382ae44a8d19799849e9f6552ed601ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4661793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44bae663e70a82d6a18cefd6ce333d007a05e509139a4b3a8b24ac9d7ad09b0b`

```dockerfile
```

-	Layers:
	-	`sha256:0bb2fc6e1399d3bcd6404926b1cc2e034d53079e6106e67afe897176d36bc313`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 4.6 MB (4641652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554b01d44ac40d68feb2a5c8ff87dd3762a3f517fd2e2a3615bb66c48ec0f89c`  
		Last Modified: Mon, 16 Mar 2026 22:45:29 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
