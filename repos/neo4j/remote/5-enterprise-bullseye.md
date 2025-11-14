## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:b1962737e5c7942be06a16a905a2b29cafed6092b161d203474a6884fedfefed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:943965a37368dbde057fe4c93a0d6986cfb08f92296eec04d9ccb8578f83ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.9 MB (667889880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762eef59bd235605da6f8a89bbc166b6c70822eb57dc897bba1caadecd829522`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:30:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:30:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:30:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ff006f997021433017e5e768f83f963f8c181531fafbcffebd53b8f6a585bf96 NEO4J_TARBALL=neo4j-enterprise-5.26.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 14 Nov 2025 00:30:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
# Fri, 14 Nov 2025 00:30:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 14 Nov 2025 00:30:11 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 14 Nov 2025 00:30:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 14 Nov 2025 00:30:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:30:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Nov 2025 00:30:36 GMT
VOLUME [/data /logs]
# Fri, 14 Nov 2025 00:30:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 14 Nov 2025 00:30:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f633027fe4b0c3d0ec1535d93fc4803a1abcd01005291e0bb599d73781603`  
		Last Modified: Fri, 14 Nov 2025 03:45:46 GMT  
		Size: 144.8 MB (144847977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34ee00844df63ccf7de3196fa300c4b6f5e42a7d0f51f8045d2529d4b9de88b`  
		Last Modified: Fri, 14 Nov 2025 00:31:20 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12b6a52203c98e290445e9271b5c80476c9d56732fb67c3833f396510e96438`  
		Last Modified: Fri, 14 Nov 2025 00:31:20 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010a5dedcd72918be9d0bf6ea9274fb364510d1bd6e01e748ad79c9f6f5763d8`  
		Last Modified: Fri, 14 Nov 2025 03:45:52 GMT  
		Size: 492.8 MB (492769371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:51b6d37c582e50933cba92355b6d4322eaa560c2fa1ac5425fa49424176b054b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4864204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1111fe397429885656e6400f6ba358c44e79ff873ff414e107b84f88eda5f8`

```dockerfile
```

-	Layers:
	-	`sha256:5dc2f1f6e529adec58b1241b8d13d26539b3f434a32e6ee304a9a01ed9f312eb`  
		Last Modified: Fri, 14 Nov 2025 03:45:25 GMT  
		Size: 4.8 MB (4843220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3798370bff9872d5d375a5d139c5ef6dc178f147bddc4b379297d7b15da4bc`  
		Last Modified: Fri, 14 Nov 2025 03:45:26 GMT  
		Size: 21.0 KB (20984 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:37f64f1a607953ef2dd92fb88d4a83d1c383b1a331402ab0b57cac032b9284f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.5 MB (664456204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc829285425f51295a3b4243179e7e8a93945470e2775a1a842debca95b5fb60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:30:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:30:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:30:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ff006f997021433017e5e768f83f963f8c181531fafbcffebd53b8f6a585bf96 NEO4J_TARBALL=neo4j-enterprise-5.26.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 14 Nov 2025 00:30:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
# Fri, 14 Nov 2025 00:30:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 14 Nov 2025 00:30:29 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 14 Nov 2025 00:30:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 14 Nov 2025 00:30:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:30:54 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Nov 2025 00:30:54 GMT
VOLUME [/data /logs]
# Fri, 14 Nov 2025 00:30:54 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 14 Nov 2025 00:30:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38779648f0194c2af49321f9fae6cbeaef4cb4db87c1575ad0ede830a46de88`  
		Last Modified: Fri, 14 Nov 2025 05:00:27 GMT  
		Size: 143.7 MB (143679912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85914353c90009f14686ec5e177e6f1b4238093fa187690b4407e42e7649358`  
		Last Modified: Fri, 14 Nov 2025 00:31:43 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5e0a229d4020f9eacf47011cea838154559037d9e6011794b1aa13e9e5fd0`  
		Last Modified: Fri, 14 Nov 2025 00:31:43 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b28527c686c0807507b4dcdf20f155ed7cfd9d9650cc8ff64b04d6f95ec710`  
		Last Modified: Fri, 14 Nov 2025 05:00:55 GMT  
		Size: 492.0 MB (492013779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:75c73c2dff0da66d51ba7115c9e944a885fdd22efff784dfca4ff29931d0cb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4838179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5787f1faa0b5827ada9e430554dc509b6c038ba9eae07df53364f5beb540078a`

```dockerfile
```

-	Layers:
	-	`sha256:85a124ecca166f41b3e452fea9bc078c863bee20f08c5910b102cc42a0dad3b8`  
		Last Modified: Fri, 14 Nov 2025 03:45:31 GMT  
		Size: 4.8 MB (4817025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be3e198c42622d05f55920388f3cd82c98f1e551ad82a63d1fa4041eb83db98`  
		Last Modified: Fri, 14 Nov 2025 03:45:32 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
