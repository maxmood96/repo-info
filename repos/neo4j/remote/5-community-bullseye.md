## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:96fd940f47033762cb8f3e4a7875358d9cb158e3ce274d48d1ceb9aaf95a4c9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:298d1487decab7ab94bd62d9109a28d2ff1fb871d4ca49d1c1079c0baea3a142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349153539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47f1ecd43c32dfbb195fdcdea06ae7b2f078732fae5bf2114b131d526992a6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 10 Mar 2026 22:37:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Mar 2026 22:37:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Mar 2026 22:37:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06a419691481fe2e08893337ba01fb3486238ff2113202f648aa294c7a5f094e NEO4J_TARBALL=neo4j-community-5.26.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Mar 2026 22:37:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
# Tue, 10 Mar 2026 22:37:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 10 Mar 2026 22:37:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Mar 2026 22:38:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Mar 2026 22:38:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 22:38:04 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Mar 2026 22:38:04 GMT
VOLUME [/data /logs]
# Tue, 10 Mar 2026 22:38:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Mar 2026 22:38:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:38:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea062cef4145560ecfa5c7fbdb088f5bfb5418bed3630f5d7249f31e0ec79b0`  
		Last Modified: Tue, 10 Mar 2026 22:38:27 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a509171a8ad0e92d74755069777d56ae056ecc570039b6cce9107dd0d4b6e1`  
		Last Modified: Tue, 10 Mar 2026 22:38:22 GMT  
		Size: 3.9 KB (3850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8619a4f0c6edc498c2920b365c65f7f0c6ee9e65f955e578023d77efa0b69908`  
		Last Modified: Tue, 10 Mar 2026 22:38:22 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa54400352086d4fb020fea217f8889c5457eebec1c75ab650bb8c6a1452211f`  
		Last Modified: Tue, 10 Mar 2026 22:38:28 GMT  
		Size: 173.3 MB (173252339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:06f7ba457fecfb4433a2b883b58ba86d6004ea55cd9a643f8016c109b47bb675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4509361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf79229fe3c9317d2b247361c321b10a49553d8a1f48929cafbe48ec8788bf9`

```dockerfile
```

-	Layers:
	-	`sha256:bfe1a190afcceea9c4e526af5f1e5970bb2ec6466262b595942e8404c7675aa1`  
		Last Modified: Tue, 10 Mar 2026 22:38:22 GMT  
		Size: 4.5 MB (4488407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89e28d6ca6cafa15b2752b0491f2be77bd2e7af35ca5ad1e473d0e38a78fab8b`  
		Last Modified: Tue, 10 Mar 2026 22:38:22 GMT  
		Size: 21.0 KB (20954 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9fb537af79f84b4ccaf007922c433e8eea91cdfa1f5fb92187d4f53c72dc0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345693682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357004d6b4e3c5bff193088f38442f1532113c410c057a582e8a4c571ef2a182`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 10 Mar 2026 22:37:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Mar 2026 22:37:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Mar 2026 22:37:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06a419691481fe2e08893337ba01fb3486238ff2113202f648aa294c7a5f094e NEO4J_TARBALL=neo4j-community-5.26.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Mar 2026 22:37:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
# Tue, 10 Mar 2026 22:37:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 10 Mar 2026 22:37:45 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Mar 2026 22:38:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Mar 2026 22:38:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 22:38:03 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Mar 2026 22:38:03 GMT
VOLUME [/data /logs]
# Tue, 10 Mar 2026 22:38:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Mar 2026 22:38:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:38:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9f1413382d4ec32cff2dacde8f9ce040f1ff064599fffd6105f9fce80b7007`  
		Last Modified: Tue, 10 Mar 2026 22:38:26 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9827d270b81f6c4680eb05c82325fd664fda65c87d8c56c5d01eb48e5d56127`  
		Last Modified: Tue, 10 Mar 2026 22:38:22 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22660af7ee6ca9f5f54b8ab1b3c9d8d8bbfe989926d8867a60760c10eca791cb`  
		Last Modified: Tue, 10 Mar 2026 22:38:21 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f46bce77e754a0e415ddf4ebde961beaed7973bf03182dc884df065bc3b22f`  
		Last Modified: Tue, 10 Mar 2026 22:38:27 GMT  
		Size: 172.5 MB (172498878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3f8d8a0f198923657a5c358d2b957a4b461b395e7b383c418e31d73a67d738be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4483334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0da22d53b44a705191082f8845f734ee953cf6ae167b6f62e9195b4f97d80cb`

```dockerfile
```

-	Layers:
	-	`sha256:717b973ce53dac94421f19c5b0230f282e9a1846d2367adc69cf118521f8cb36`  
		Last Modified: Tue, 10 Mar 2026 22:38:22 GMT  
		Size: 4.5 MB (4462212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20bfdf6af7a34ed620bae37de5870496bc70e4091a6a6363736cee17fcfeda4e`  
		Last Modified: Tue, 10 Mar 2026 22:38:21 GMT  
		Size: 21.1 KB (21122 bytes)  
		MIME: application/vnd.in-toto+json
