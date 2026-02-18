## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:545926621145551ccd7542be6a5a1a7c7ea93f769e431bc09803f107cd1407fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a8132ddac0165de150caab10db0c154f336729d62248171914d41af89814d8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306665143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c85d6ded0c92457a5d156b1684a17ba91fb4cf61010db4823699f299ff6e72`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e7479438004924167ceb707f9620ee39db7d06870e9ce00d52573350f3518dc4 NEO4J_TARBALL=neo4j-community-5.26.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
# Tue, 17 Feb 2026 21:24:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Feb 2026 21:24:44 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:02 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:02 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11623aee50e10257b7825c5496f1ff49b8522825efe4e70ca516cfb097f9ac45`  
		Last Modified: Tue, 17 Feb 2026 21:25:23 GMT  
		Size: 145.6 MB (145628714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a079da31a9b4ca732ad567d66ff2a7fe1f4754ef5bfbbb39212e60213ebe26d1`  
		Last Modified: Tue, 17 Feb 2026 21:25:18 GMT  
		Size: 3.9 KB (3851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64d6d2915f5535ef9d65245e0b692c9946c3f2fe1828a8f777868fb4e4a37e`  
		Last Modified: Tue, 17 Feb 2026 21:25:18 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cff6dfafdcbe2755c6a5755fdbb9109ea15868467feac6807814fd6446cd0f`  
		Last Modified: Tue, 17 Feb 2026 21:25:23 GMT  
		Size: 130.8 MB (130764024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9bc3d73683d329f94901e2a4d3e74a631dab342a4eaf506a50b2768299ffd44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4502127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bde6b1b78632e6a26975d48b2a463bc46299d6210d25377807876e59360a5d0`

```dockerfile
```

-	Layers:
	-	`sha256:c3f43feb497f2861d7c8d88a2a1189997c0c51204dcd47bd831ab6fb174934e3`  
		Last Modified: Tue, 17 Feb 2026 21:25:19 GMT  
		Size: 4.5 MB (4481173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07d014c179289e8aac7d5e263c865fa980b11ee711c87ef3cdfbd3f97873d79f`  
		Last Modified: Tue, 17 Feb 2026 21:25:18 GMT  
		Size: 21.0 KB (20954 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:204ef6b29be4a688dd2615961b40fd0e5ae9e51aa0d928621103694f6ca71637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303203065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e052b885ea2bc578d55c3fb5800030980eeee719e98832c44b8baa9623d152`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:24:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e7479438004924167ceb707f9620ee39db7d06870e9ce00d52573350f3518dc4 NEO4J_TARBALL=neo4j-community-5.26.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
# Tue, 17 Feb 2026 21:24:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Feb 2026 21:24:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:07 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:07 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:07 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2244154de3441e80c268ed705dbea029c1cfeb2470b0d3424f653519606f609d`  
		Last Modified: Tue, 17 Feb 2026 21:25:30 GMT  
		Size: 144.4 MB (144436206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae34137e7195318e885e0458ff43ecba6a0f4be8ab28fd01fdd7e26cbee25dc`  
		Last Modified: Tue, 17 Feb 2026 21:25:25 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31d335ca0529422343389d89634e98938ed1d5b0d2ce21b563ca9b6736804f2`  
		Last Modified: Tue, 17 Feb 2026 21:25:24 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320fb3221aa2ece35f149d4f6156cb29e199fd0a9896a903b74c44ba65c8989`  
		Last Modified: Tue, 17 Feb 2026 21:25:29 GMT  
		Size: 130.0 MB (130008277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d675c287f7a6a1a307052430dacdc1d264d421d0c79b1eb5bac58d7f8f1c3014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4476101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea84deebb6fa9ba32e5a96b1fc7a6f344baabd828fe313ed6f51c3b546f24526`

```dockerfile
```

-	Layers:
	-	`sha256:efcc280f443e721cfc131ca38e92554a52dea0ffc2bb7a4f79c1ae503d72cba3`  
		Last Modified: Tue, 17 Feb 2026 21:25:25 GMT  
		Size: 4.5 MB (4454978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c59708362183c0d700f158402286b9ab96a54d81ec8a9138b073a9d8b5c142de`  
		Last Modified: Tue, 17 Feb 2026 21:25:24 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json
