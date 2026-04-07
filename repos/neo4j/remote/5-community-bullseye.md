## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:1deeea210145005f3bf473a6eb8bfa23781309ffe1faacd21091337f1f92c8a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b7975b11d29a3c2fd74a2c2a2cb459c5348460f479097d030bf7550eb53eb172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350932281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f944ef17f6e44746a1eed8b1a59476b89cce998d8b42a9fd0f5d57e6dc28c93a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:58:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:58:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:58:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 02:58:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 07 Apr 2026 02:58:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 07 Apr 2026 02:58:39 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 02:58:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 02:58:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:58:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 02:58:59 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 02:58:59 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 02:58:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ae677676ce4c2256bce52e9be3197c518a7b147f498958600be664fc5bf1d6`  
		Last Modified: Tue, 07 Apr 2026 02:59:24 GMT  
		Size: 145.6 MB (145628717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a307b2f73869d81b5761b4bcf2080b5ca9f8945db82a6858c19e281978706079`  
		Last Modified: Tue, 07 Apr 2026 02:59:19 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca86f5131563dc90ee730908503300701e6973f69a73e495df84ba02fad790b`  
		Last Modified: Tue, 07 Apr 2026 02:59:19 GMT  
		Size: 10.2 KB (10247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188683239a3ba873e5771be1a9f100a94badf604d7b6cf440c93f7330522ded6`  
		Last Modified: Tue, 07 Apr 2026 02:59:25 GMT  
		Size: 175.0 MB (175031425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8fe3b3fd653b2204c171374e2100519262ebed8d4fb963bc7e8c0ae751e11581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4509006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fab41beb1832e32a8f88a61bff33b3d9f05598bfcf9705c5b06607ae84f44d`

```dockerfile
```

-	Layers:
	-	`sha256:da721012e3045707aafde3988667bf8470dd1ad3021cdb0d39b59fd75e25d793`  
		Last Modified: Tue, 07 Apr 2026 02:59:20 GMT  
		Size: 4.5 MB (4488052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50eb0c97237899f64a9987ab9d66bae7d73814aeddc0f79330b789296e5a4de`  
		Last Modified: Tue, 07 Apr 2026 02:59:19 GMT  
		Size: 21.0 KB (20954 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a244b85bafb432d2b0a9a4cd17dc49792e4c34ab4d23b5a187395416b894e72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347472306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843f5b9c2455b774bfbc7ca23815dcbd2f76b4c25828846aefa5cdfcc31acd6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:11:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:11:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:11:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e17d344f00a50a5befb8ef8eb29f08bb56945e5334562c05457a03651657c85 NEO4J_TARBALL=neo4j-community-5.26.24-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 03:11:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
# Tue, 07 Apr 2026 03:11:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 07 Apr 2026 03:11:12 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 03:11:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.24-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 03:11:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:11:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 03:11:30 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 03:11:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 03:11:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:11:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc525c6b57927bfbacd16890254442b6078dadd32746134d24c032a9417a03f1`  
		Last Modified: Tue, 07 Apr 2026 03:11:54 GMT  
		Size: 144.4 MB (144436227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce859fa45a4cd46d808ec1a559a80b8b8aa62156aa25b220f0ed2308141ca98`  
		Last Modified: Tue, 07 Apr 2026 03:11:49 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f8961e10e7f422334a52fd7f56e4ae94f463cf6f29fbbcbfd4f31f20779107`  
		Last Modified: Tue, 07 Apr 2026 03:11:49 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05269c06b873f618395543796b4fa5c0f79330b7d3706c577227f1420c9d7083`  
		Last Modified: Tue, 07 Apr 2026 03:11:54 GMT  
		Size: 174.3 MB (174277242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e48b050d032396db7b05cac676e0a75a35dc4e520f612ab066a01cc169f644d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4482980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0868cd9078b2e587f4230adcfd9f6f9a3966e76ec00fb4debe360eb400f13071`

```dockerfile
```

-	Layers:
	-	`sha256:6ebd630d26bfff51d04f0ee62889b2b1220e0124db68fb12ddcdea3b690abe31`  
		Last Modified: Tue, 07 Apr 2026 03:11:49 GMT  
		Size: 4.5 MB (4461857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15cd5e975de2afd25810951b2b3fdf262762dcd172710cbd7a1bbf89dce25dfa`  
		Last Modified: Tue, 07 Apr 2026 03:11:49 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json
