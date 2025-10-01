## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:7c86cd53946a711a488079a82d4fe4e4342e56655e3d175383949fdd1d3ee18d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7baa01b3d9b537dd4214cde82d0865aa33cdc3421da78ed5ddcfbea00431a29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.1 MB (538130471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cee2941e1abf6994a46342d4f6722f7058300079946803510d98b67da431741`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Sep 2025 16:30:37 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Wed, 24 Sep 2025 16:30:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Sep 2025 16:30:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5914da159fa7226f0d94c7af9179705c15df88cdf7e488560c0c21fa9f746fbc NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Sep 2025 16:30:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 16:30:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Sep 2025 16:30:37 GMT
VOLUME [/data /logs]
# Wed, 24 Sep 2025 16:30:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Sep 2025 16:30:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 16:30:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72809d519ee4b500100bb08329750bf828dc711b2ccad161cb1158282f77e54d`  
		Last Modified: Wed, 01 Oct 2025 14:44:29 GMT  
		Size: 157.8 MB (157804739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2593492304b856e06ab245e045ec30083466ec9bfc1a1c02a1109a5f37781da6`  
		Last Modified: Tue, 30 Sep 2025 00:15:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978965a56c73891555641f4a7b26b7e64bb2821ab0f17092b52bc14d98d03583`  
		Last Modified: Tue, 30 Sep 2025 00:15:09 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f4e5d9fd0ae8f43d85a392cf6fb05918ff3ce2fe45bec172fbfd01797b8353`  
		Last Modified: Wed, 01 Oct 2025 14:44:45 GMT  
		Size: 350.1 MB (350053477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e448bdff42a14ba172b5ce002bdbd8b3747107bb79ba7a955179e921b527fee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4866753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b902f15277c7a9deb9b4f193705132eb5ee81733d1f1c05726a892fec55dd27e`

```dockerfile
```

-	Layers:
	-	`sha256:16107799cadc065f3c5ad47470fcc583179199cbf6f2abc6f393005da6aaa3b0`  
		Last Modified: Wed, 01 Oct 2025 14:43:26 GMT  
		Size: 4.8 MB (4845049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9532e6898aa03e8096122c5f230941614ed53b7b40d2f55d2f75701b501009f8`  
		Last Modified: Wed, 01 Oct 2025 14:43:27 GMT  
		Size: 21.7 KB (21704 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1630c6cdf61487ac741930165e37ac65e20e1712230f7ccdf45deede7a9ce7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.1 MB (534141910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797528126bc9297b7378fbe6527d03824020e346cea653195536ccd2b5269c91`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Sep 2025 16:30:37 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Wed, 24 Sep 2025 16:30:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Sep 2025 16:30:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5914da159fa7226f0d94c7af9179705c15df88cdf7e488560c0c21fa9f746fbc NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Sep 2025 16:30:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 16:30:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Sep 2025 16:30:37 GMT
VOLUME [/data /logs]
# Wed, 24 Sep 2025 16:30:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Sep 2025 16:30:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 16:30:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cecd0f40a1d09b0d9c50caa73c3a1b265ce291c0d2518cb15e4de998a944db3`  
		Last Modified: Wed, 01 Oct 2025 17:03:03 GMT  
		Size: 156.1 MB (156081234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae4d4ecb83dd96a09747b84094c6cc8ce35b8af03c4be50689d060c1ee391b`  
		Last Modified: Tue, 30 Sep 2025 00:19:05 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13a9f0a3bacc0946dae18380258f45f21caf112b883a31b052eb98b6af1d628`  
		Last Modified: Tue, 30 Sep 2025 00:19:06 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc65a91572387f3dc5da7fac7a91cd0c5c8f27a50b1f14704856cb2b541ec9`  
		Last Modified: Wed, 01 Oct 2025 17:05:22 GMT  
		Size: 349.3 MB (349298329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:6d462381dfecb709bbe460f7b4f66d474e78cfa32c07a4e4a1ed77d1e154760b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce142ba207e49d973aa7d78e1c91f06955326cc9eb664dae9e3aa1082ce251b8`

```dockerfile
```

-	Layers:
	-	`sha256:81415d7687d598796573ef76e9e9f56c61b0450d1739f1009ac09322b6b2e4db`  
		Last Modified: Wed, 01 Oct 2025 11:43:43 GMT  
		Size: 4.8 MB (4818878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be13635150bca58a91db469570e6933e95e19e1540d4460721cbffac22bc9f3a`  
		Last Modified: Wed, 01 Oct 2025 11:43:44 GMT  
		Size: 21.9 KB (21897 bytes)  
		MIME: application/vnd.in-toto+json
