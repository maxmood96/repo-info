## `neo4j:2026-bullseye`

```console
$ docker pull neo4j@sha256:b27cae04581ccd9b4a5c787c1b6a14b56b0823d58c039929c4e7e8617581ebb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b26e2b995d87f5d7ec72769676dd5a99f9d97655ed375219c39c88d3021782f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.9 MB (447911448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f4ac6e6e46aafebdc0bc97861c51314b2951e8ce83e65f3a59fd1d20ec2437`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Fri, 06 Mar 2026 18:24:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Mar 2026 18:24:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Mar 2026 18:24:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 06 Mar 2026 18:24:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Fri, 06 Mar 2026 18:24:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 06 Mar 2026 18:24:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 06 Mar 2026 18:24:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 06 Mar 2026 18:24:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:24:28 GMT
WORKDIR /var/lib/neo4j
# Fri, 06 Mar 2026 18:24:28 GMT
VOLUME [/data /logs]
# Fri, 06 Mar 2026 18:24:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 06 Mar 2026 18:24:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:24:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79fde9d018fec6454d176df8b0cb189011d1f5bc7c89712186079e4e8ec2695`  
		Last Modified: Fri, 06 Mar 2026 18:24:57 GMT  
		Size: 157.9 MB (157857047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c314511ffee0ad0d4f5441b721e2d26548ac54bf573e877bd9d37321eafdda7c`  
		Last Modified: Fri, 06 Mar 2026 18:24:51 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3063f75571f5d4de2f9d79ddb68fe55b4ed817bb7e17cdbe63de16d2ba661ae`  
		Last Modified: Fri, 06 Mar 2026 18:24:50 GMT  
		Size: 10.2 KB (10191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767df50324bc15174c6eb281e9286a656941e5b7d9e79d66fd02e698613a342b`  
		Last Modified: Fri, 06 Mar 2026 18:24:59 GMT  
		Size: 259.8 MB (259781958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:854cc05387143959c817e179f24488e730c769b8c6f6a5ee3c0ba58a59ad4701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4634319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563ffb4123b31e217c5d8fd6f8df73a4f73b25f5e41de586c5fac522a400d541`

```dockerfile
```

-	Layers:
	-	`sha256:1fd150b51cd7463f0b6544b0080e6bcf8ecd4dc2ff6b344bedb4c6db5f162181`  
		Last Modified: Fri, 06 Mar 2026 18:24:51 GMT  
		Size: 4.6 MB (4612696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6c0761326a79a6eadd7b62e74b5c0f4e9362ba1fffa010e7ea0682dc8320f2`  
		Last Modified: Fri, 06 Mar 2026 18:24:50 GMT  
		Size: 21.6 KB (21623 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5700b64a943a01320831e190707adc61336d7f89aee046bd1b787523b2c80d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.9 MB (443920322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca6b6d2e4cd4b9edcc15698783958da1514442632729e2bf8396c95d283a1e3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Mar 2026 22:44:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 16 Mar 2026 22:44:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Mon, 16 Mar 2026 22:44:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 16 Mar 2026 22:44:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 16 Mar 2026 22:45:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 16 Mar 2026 22:45:11 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:45:11 GMT
WORKDIR /var/lib/neo4j
# Mon, 16 Mar 2026 22:45:11 GMT
VOLUME [/data /logs]
# Mon, 16 Mar 2026 22:45:11 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 16 Mar 2026 22:45:11 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9192d326ee6ba2e0c88ae631fab3d02e7980329d1b0a9984224ccadb5bbbbd8`  
		Last Modified: Mon, 16 Mar 2026 22:45:39 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56c38df2f159aef466acbc6602526c6e7bbf797104f28cc1955fd1072f9da75`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bb14d92405aa53b2a7aad72ec8d3e6f8a6c3d43d53e39a004ab9b0dc1f9667`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ca1a769c031e2a6c1c078734db64c06e1060015843fecf41e8d5ec0755b616`  
		Last Modified: Mon, 16 Mar 2026 22:45:41 GMT  
		Size: 259.0 MB (259028610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:50f01943f587066a63930a12c68ad1a2a73954dcf1fb2932706bafdd2bdddea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6b2a5fdf3dd27dd9b6054e38ace8f2ef821b14e2ebcec50f18f3ccf65ce3f`

```dockerfile
```

-	Layers:
	-	`sha256:7dfeb8faf1b8267e7515850cd9091aa16a58c9ef8bfe9612252c21e8ee0f4a39`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 4.6 MB (4584901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d015235ae0bef8102348bb8445ee41ba20157db833613f01ae2fc0f68538c6`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 21.8 KB (21817 bytes)  
		MIME: application/vnd.in-toto+json
