## `neo4j:community`

```console
$ docker pull neo4j@sha256:c902d0c3e0d22b2dc96b649a54feb4640efb2f65f8c151a111cce199d9c86485
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

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

### `neo4j:community` - unknown; unknown

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

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:74332a78dbd77bc683d8e8ee12aa0c302b96e7adb47eaf39856a236cc20d4809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422341670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d0a789771884f67cbc14e22ee6ac3402ceee72ca3bd10118c1d2677bb32321`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dda333c6387bcec3380c61245072e9474b18248f798d3607582966e88c85ff1`  
		Last Modified: Wed, 04 Jun 2025 21:29:13 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21802c0b41e3e1e837360249fd1eff7a40988e8ae3836def351898e6deccf13`  
		Last Modified: Wed, 04 Jun 2025 21:29:14 GMT  
		Size: 10.0 KB (9976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29c2000b6f6489602113887973b848cd7f41cf00ae5325d1f51361e1f38fbfc`  
		Last Modified: Wed, 04 Jun 2025 23:44:43 GMT  
		Size: 237.7 MB (237652722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4921979685329a25126343a76d220acce0a61859e57248d61b670346e6c7b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae5100e9478c307cc314163cf8e288e6fac4dbb64635bfe3ceebf79e66ddc0`

```dockerfile
```

-	Layers:
	-	`sha256:c169d05b99afe80e476d46c9b7e6d13cca70f51cd78accf12cb47fde45894a9a`  
		Last Modified: Wed, 04 Jun 2025 23:43:22 GMT  
		Size: 4.5 MB (4482252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8aec338f781186d534dc81dd01ec31d9e9aa2b17ace076411ddb5ffc73a4841`  
		Last Modified: Wed, 04 Jun 2025 23:43:23 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json
