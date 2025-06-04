## `neo4j:2025-community`

```console
$ docker pull neo4j@sha256:a7b18625ac8c261a3c6f5144317a6392ce1cb434a1c20286808795d4f92d7792
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3dfc1454d9cb70a3e9cbf3c3002823c4bc169eb7741d7baffde1214e7fd3d336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.1 MB (427097225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14407187fb4c0672c93df6a1f1e46df49c74b95d8542a5b2a32e0887950bf14`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 10:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=561f985e6355e98cf6f2b4f106599bfceb27a5adeffdc0856c71a2c5bb008f68 NEO4J_TARBALL=neo4j-community-2025.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Jun 2025 10:48:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.0-unix.tar.gz
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:48:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Jun 2025 10:48:21 GMT
VOLUME [/data /logs]
# Tue, 03 Jun 2025 10:48:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Jun 2025 10:48:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:48:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2136e2a64baaeea92fd450383b42aba04b20ce1b5306a0bcda0a1fdb1245b54c`  
		Last Modified: Wed, 04 Jun 2025 20:44:38 GMT  
		Size: 157.6 MB (157634483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdad3630f2c6223cff3125eb67a4f5732b627395d47b933fb12836cf8ea08f2`  
		Last Modified: Wed, 04 Jun 2025 18:36:49 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f50ef3f6bce0f7c95c9069406135e257fb7bf4d628ec385edcec35a56b27620`  
		Last Modified: Wed, 04 Jun 2025 18:36:49 GMT  
		Size: 10.0 KB (9980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df757536bc8863b2677575e46306121a9daaf2bb105533a0471f7d7a8d515c8`  
		Last Modified: Wed, 04 Jun 2025 20:45:21 GMT  
		Size: 239.2 MB (239192949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:720b2897069edadf6d8998091ec9d9640d814edeccdc2fd1e0b983b890ff3691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4532433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55008be5f462792ebc37ceeed0beb290c984dd8f3c1a2dc06c1d4d4d6fd297`

```dockerfile
```

-	Layers:
	-	`sha256:98da55153b0cf67772945f2859863f77192119fe9a5e0e6d0a1a98706e079544`  
		Last Modified: Wed, 04 Jun 2025 20:43:21 GMT  
		Size: 4.5 MB (4508327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594d6e33ef5617fe2e4e4452ad94a43cefa6ae4de3498f3d9c39168a8f05b95b`  
		Last Modified: Wed, 04 Jun 2025 20:43:21 GMT  
		Size: 24.1 KB (24106 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa3e5b2c436f05dc546051a5f2567310d2b10a1ff4e19152eb2e4654a343f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350656108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc1e02fbbb28cbe77b1921ae68d2199dc2da7609f7855fa72ecc2286fdf92b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Apr 2025 10:30:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 29 Apr 2025 10:30:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Apr 2025 10:30:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=118cb439904d1aaad67f2421be518d2acc2b754f621acc209ee3362e5b67ba65 NEO4J_TARBALL=neo4j-community-2025.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 29 Apr 2025 10:30:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.04.0-unix.tar.gz
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.04.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.04.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Apr 2025 10:30:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 29 Apr 2025 10:30:01 GMT
VOLUME [/data /logs]
# Tue, 29 Apr 2025 10:30:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 29 Apr 2025 10:30:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 29 Apr 2025 10:30:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5dd4a400830c1868485517ab4720049a908e50acac3ddcd7aa5c80466d391e`  
		Last Modified: Tue, 03 Jun 2025 13:32:36 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62d428a8fc734dab2a214f894acef4fe8e43a6d560cb7d260668084dc0b317f`  
		Last Modified: Tue, 03 Jun 2025 13:32:40 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691c9fd4550689600f33df7bbe330c7686c9a585daf72db575924f36916f620`  
		Last Modified: Tue, 03 Jun 2025 13:32:44 GMT  
		Size: 166.0 MB (165967106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:631460c129c15007d8e087ba27ac2bb896183c935371312f567481bc703d9223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567f1ae4f2b95d49e693faf40f442149de522c7c35bef5ab412c160c1b1bb7ef`

```dockerfile
```

-	Layers:
	-	`sha256:337c35d3aa28a1b33b2a1aef5511ec9a062ed060b7ce29ff40079802b2dd94b2`  
		Last Modified: Tue, 03 Jun 2025 16:55:20 GMT  
		Size: 3.3 MB (3272707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98710c0321b83e18f6450bd6a60616777b999d68685fe1d2557ce93732c86c03`  
		Last Modified: Tue, 03 Jun 2025 16:55:14 GMT  
		Size: 24.1 KB (24143 bytes)  
		MIME: application/vnd.in-toto+json
