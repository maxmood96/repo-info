## `neo4j:community`

```console
$ docker pull neo4j@sha256:176a724378d0521aa4fb4b70c408c54a717280d844b395a47b05c4181ac707e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:b39586218dfab88e37fb2f7557bba474d5ee2af000e8e9fbb767a37ed58b20d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.2 MB (421201652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679cd414d7b3437d29048967d5db9eaa22f260b81877cc6b8d1fbd5fd882be37`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Tue, 01 Jul 2025 15:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Jul 2025 15:46:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7f8d0e56c4b8134d112e05e7b498a055c5f66f726af4d0047ee1ab6d2a0749a0 NEO4J_TARBALL=neo4j-community-2025.06.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 01 Jul 2025 15:46:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.06.0-unix.tar.gz
# Tue, 01 Jul 2025 15:46:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.06.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.06.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 15:46:08 GMT
WORKDIR /var/lib/neo4j
# Tue, 01 Jul 2025 15:46:08 GMT
VOLUME [/data /logs]
# Tue, 01 Jul 2025 15:46:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 01 Jul 2025 15:46:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 01 Jul 2025 15:46:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637bced0eb325b52d6071d1c53325bff2c17036f292530e5213a8d197634649f`  
		Last Modified: Wed, 02 Jul 2025 05:44:12 GMT  
		Size: 157.6 MB (157634482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c0b7e84c5ed4c41d531bddd36afc91d3b31903c5c2a225c081282f1e40c066`  
		Last Modified: Wed, 02 Jul 2025 05:43:30 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a4729dac7a087460e4910e7d2e68b7e021779a35b7143e109bebf24c31baba`  
		Last Modified: Wed, 02 Jul 2025 05:43:34 GMT  
		Size: 10.0 KB (9975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31c4f7b739b43707d75c3e15d74261166983358198d609da4682776b1467be2`  
		Last Modified: Wed, 02 Jul 2025 05:44:13 GMT  
		Size: 233.3 MB (233297275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3e7fa6daf6fdfd79f1903da9ff87d9a86a8f7f55e6134e11f6e611f06a1450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4621505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60b2755fa4770f269d9964a1c4c13426aa0a7359dcec9add2ea07efbafdb475`

```dockerfile
```

-	Layers:
	-	`sha256:720249ddd58ee4f4a40c511ab61e976dd2c8b571517ecacbf4dd627817e4d0c0`  
		Last Modified: Wed, 02 Jul 2025 05:43:30 GMT  
		Size: 4.6 MB (4597399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c29a9bb2d7fc3e5f668b08ee9e8b792c428be4a42b1aff2761f6c9e125d959d`  
		Last Modified: Wed, 02 Jul 2025 05:43:31 GMT  
		Size: 24.1 KB (24106 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d85740cb2bdb5fe71df5728020a2e011c819175429a6a636b70be2f80f269c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.7 MB (418715818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c1a3096aaa50c713a67bb04e898777c5422e44bd4d81aff36e2420d71295a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Jun 2025 13:23:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 19 Jun 2025 13:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Jun 2025 13:23:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7be4a4e8f374c66df880abd6a236ff789cb61c1b22746b17cfad343abc3e5505 NEO4J_TARBALL=neo4j-community-2025.05.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 19 Jun 2025 13:23:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Jun 2025 13:23:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 19 Jun 2025 13:23:43 GMT
VOLUME [/data /logs]
# Thu, 19 Jun 2025 13:23:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 19 Jun 2025 13:23:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f209ff44f683a19134a65d227eda78e676586776061dfd6857f025b7df4f82e`  
		Last Modified: Tue, 01 Jul 2025 08:48:37 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb53471bb492ad075b867700e47ab58cb4f431239b226018037f0fdd6615578`  
		Last Modified: Tue, 01 Jul 2025 07:17:40 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46b87a4c30e6f57ef095ad0107e98851cee6678de4c9d0f40a323c2753166ef`  
		Last Modified: Tue, 01 Jul 2025 07:17:39 GMT  
		Size: 10.0 KB (9979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca59d1f4ead5d94ef711b00714859abd572572aa2bd0e1ec3031767bca6010`  
		Last Modified: Tue, 01 Jul 2025 08:45:06 GMT  
		Size: 234.0 MB (234028977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:2731e79278388c2b32fa429ec8efce566023039197b4d1068432b1e5e608f771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4600310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cb8339d5adc28a06f43f3ac4d6c0bd05a6c2e07478a21714072efd26970fd6`

```dockerfile
```

-	Layers:
	-	`sha256:ff5dac263e9e9ec1c3434fb911d92be89cc5f442169f5a51fcc2585ca87880d7`  
		Last Modified: Tue, 01 Jul 2025 08:43:21 GMT  
		Size: 4.6 MB (4575915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92ccdbb0a2b351ab3bc838dd68b5a41e039bd67e4c44394d2387a11c6b9bf25`  
		Last Modified: Tue, 01 Jul 2025 08:43:22 GMT  
		Size: 24.4 KB (24395 bytes)  
		MIME: application/vnd.in-toto+json
