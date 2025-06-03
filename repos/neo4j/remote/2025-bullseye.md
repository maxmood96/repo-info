## `neo4j:2025-bullseye`

```console
$ docker pull neo4j@sha256:80cc874b30cc7a5a75b76b8deb7cb652d60c7d2fa5bad639155d0bdef1a48509
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:134125796fb29ada4e891c66d4708b5190d61ad62866fc59fe1ff30c1d3b1208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354692645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea8a0d431427b097227a66b9727187559897bb80b3a0b9462300d95b1deb6e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Apr 2025 10:30:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2977d505d57e28240b3196a6d74842f877ad7d6a1e244106c8285471901d19`  
		Last Modified: Tue, 03 Jun 2025 05:13:43 GMT  
		Size: 157.6 MB (157634492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7243c87fd3d75eb05ef432d6dcc36e51dbb8ee5ecdd1ecab801bfc31f593625`  
		Last Modified: Tue, 03 Jun 2025 05:13:41 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6b21c33de1f1ed7c6c605f794e88059449440cf3ba58d513668143cff9ffce`  
		Last Modified: Tue, 03 Jun 2025 05:13:40 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea50d0a287c3d1dd07b89966e8372e84fdb3b67ed8fb4b40afba6dd178b1ed`  
		Last Modified: Tue, 03 Jun 2025 05:13:43 GMT  
		Size: 166.8 MB (166788315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ecc951e799a4c481daac3c324a674cd4071fe9e4d4d5872280237edc76f69db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2f4c89525d8eb95845bf254b1e45655661338c1d204d4a5d2dfe5a34dbf527`

```dockerfile
```

-	Layers:
	-	`sha256:674dcb66e133fe3fb2b7ae3306bb5b8df84161ee9db455fc73d35c711b20e1e1`  
		Last Modified: Tue, 03 Jun 2025 05:13:41 GMT  
		Size: 3.3 MB (3272917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:582f6c0ed4cc3742d942ead9d448aa3a1164780b2f0a331b8beac9fb786de460`  
		Last Modified: Tue, 03 Jun 2025 05:13:40 GMT  
		Size: 23.9 KB (23854 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-bullseye` - linux; arm64 variant v8

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
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 07:47:31 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5dd4a400830c1868485517ab4720049a908e50acac3ddcd7aa5c80466d391e`  
		Last Modified: Tue, 03 Jun 2025 07:47:27 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62d428a8fc734dab2a214f894acef4fe8e43a6d560cb7d260668084dc0b317f`  
		Last Modified: Tue, 03 Jun 2025 07:47:27 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691c9fd4550689600f33df7bbe330c7686c9a585daf72db575924f36916f620`  
		Last Modified: Tue, 03 Jun 2025 07:47:31 GMT  
		Size: 166.0 MB (165967106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-bullseye` - unknown; unknown

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
		Last Modified: Tue, 03 Jun 2025 07:47:27 GMT  
		Size: 3.3 MB (3272707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98710c0321b83e18f6450bd6a60616777b999d68685fe1d2557ce93732c86c03`  
		Last Modified: Tue, 03 Jun 2025 07:47:27 GMT  
		Size: 24.1 KB (24143 bytes)  
		MIME: application/vnd.in-toto+json
