## `neo4j:5-trixie`

```console
$ docker pull neo4j@sha256:7a7e514888d668103d4a3a28516613ffdbb79f2161f91e49dfbd57c2b7f10d8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:704ef2a31ae2d46840b84f01f211b68b2eabbc2f243a7c597b722413c6e194f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365432117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851cbf891463f12f4a5917f00ed5c86989ef2aa903733c2de88093d36cdb055c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:57:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:57:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 02:57:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 07 Apr 2026 02:57:59 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 02:58:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 02:58:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:58:22 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 02:58:22 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 02:58:22 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 02:58:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4905befd0b435d073e97888696f8eed85871988758a17f818cd43af9647c0963`  
		Last Modified: Tue, 07 Apr 2026 02:58:48 GMT  
		Size: 157.9 MB (157857048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b8a6b61a0c6b5bbad5225f01a3c5a6b3a89c0c5f349d3b778700184a6d1fe1`  
		Last Modified: Tue, 07 Apr 2026 02:58:42 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66088584c6fbef059877da9212f0fb3d984670834ea5fd6d67e359c03ec62629`  
		Last Modified: Tue, 07 Apr 2026 02:58:49 GMT  
		Size: 177.8 MB (177789336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:4ac07b5b95924beb4feffa988666b0a15b8d735b07ac6a5213586e84ab536d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8128ecc1e1cc1faa557c7ff01adddabf35bfd46cbb726935364f62ff9fce7de6`

```dockerfile
```

-	Layers:
	-	`sha256:851f88ab79055a7e13e87a038c9c785acd0510db6fa09368662bfc7645d88849`  
		Last Modified: Tue, 07 Apr 2026 02:58:42 GMT  
		Size: 4.3 MB (4291107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9734c711dd6f625fbd63612877cb79ed71fd23d5a2910114c2aea7c5ad185d09`  
		Last Modified: Tue, 07 Apr 2026 02:58:42 GMT  
		Size: 21.1 KB (21067 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5163941dd4bbf2a2232586fbc68c428d987fffa988f26ce2aa71c69b928ae36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363141425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca179949718cc74f3a6a0e8f30ba878f5475d9d1cdb68d4f92fadc8cc40dc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:11:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:11:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:11:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 03:11:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 07 Apr 2026 03:11:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 03:11:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 03:11:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:11:29 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 03:11:29 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 03:11:29 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 03:11:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:11:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4113b02cf88ba708e21d62567e6cd676fef7a57dc6a7cf92990be5223b7b0300`  
		Last Modified: Tue, 07 Apr 2026 03:11:54 GMT  
		Size: 156.1 MB (156133058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020b10f06870bdcdd90a7a989bd455d043192d16d588931892c2a932ac8a9241`  
		Last Modified: Tue, 07 Apr 2026 03:11:48 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed97cb7d873b96dd4152a5fa04d80afda8479077ab3dd826182657bccb13359c`  
		Last Modified: Tue, 07 Apr 2026 03:11:54 GMT  
		Size: 176.9 MB (176859724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:66b79b6214b2737366d4a9d9353eb201f8e016914a51aa838a79a2a238214d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f917f9fce267fe29a06e3adc9ccf5747bfc0de80c2d020646a97ab88563799`

```dockerfile
```

-	Layers:
	-	`sha256:fdaeed7e8e80ecd5598c859472cbeddba28637e7853e1a1df7f7a394ff0c474c`  
		Last Modified: Tue, 07 Apr 2026 03:11:49 GMT  
		Size: 4.3 MB (4285633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc6c02e92a8c06591d0f3a181f2ba457913df77419eb50a6a884301055eb8f9`  
		Last Modified: Tue, 07 Apr 2026 03:11:49 GMT  
		Size: 21.3 KB (21294 bytes)  
		MIME: application/vnd.in-toto+json
