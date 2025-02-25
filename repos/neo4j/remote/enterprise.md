## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:de1f09d251b66872535b0c4f01a06be4fdf160209d9459285fbd97ab08d96bac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:944f6afa7ee122da85169339f0da94143ed2ff91428e086073c0ecb69015a8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.1 MB (621068520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7fbc7aaf5f2c3e55da5373839de6e70047d01c2219470b3d99b57e736de488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 05 Feb 2025 12:33:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 05 Feb 2025 12:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Feb 2025 12:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=df89af2f412ae2b200c47dec0dff0d5381880e49f314112544817bc151dfbfcc NEO4J_TARBALL=neo4j-enterprise-2025.01.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 12:33:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:33:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 12:33:33 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 12:33:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 12:33:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6fd145a13e6644604833789ca225460b2feef2c362b143bc0b1c6be425a1f7`  
		Last Modified: Tue, 25 Feb 2025 02:27:19 GMT  
		Size: 157.6 MB (157585931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135db7b2ce4e468e7beba9155dbe40e1e6254adaaa4be92820a5e7b08d07827f`  
		Last Modified: Tue, 25 Feb 2025 02:27:14 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a902732bfd51c28155e9d47305a6855d2eaa19ada59e2ba23fbcadeab0ba2`  
		Last Modified: Tue, 25 Feb 2025 02:27:14 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9af768f2aeb3a1ee9e3652793075118c776c58f29f96cf28dd72b9bb38f523`  
		Last Modified: Tue, 25 Feb 2025 02:27:24 GMT  
		Size: 433.2 MB (433214751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:721700cd9d1943d9d23e97a79de30a027d1a04b4c106db3866c9da0c86988fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60111aaee4c9ea89cf8ce302d7a54229b146da29f6f365f1b56d5562ed6117c`

```dockerfile
```

-	Layers:
	-	`sha256:8124073ff93f1a8fea7174da02707f2a1a42aac74c2f9ef53a83574029801e51`  
		Last Modified: Tue, 25 Feb 2025 02:27:14 GMT  
		Size: 3.5 MB (3531331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a4f4d7cacc4d359f9387d5ff0a3f15be4aa7699debd436bccf9b9055e03cf8`  
		Last Modified: Tue, 25 Feb 2025 02:27:14 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cce672398048e4b4250dd85f181ccdc4df84b72ecf896367cb70535a8492377b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.8 MB (617793221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3413c692ae7f39b57d9da0c5d73ff6b7e9c5bfa814651c3e35f959505e70d13a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 05 Feb 2025 12:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Feb 2025 12:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=df89af2f412ae2b200c47dec0dff0d5381880e49f314112544817bc151dfbfcc NEO4J_TARBALL=neo4j-enterprise-2025.01.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 12:33:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.01.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:33:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 12:33:33 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 12:33:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 12:33:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1444b3218878a3b35e8951a2bc0e44515e7eeec8e85c72e00762e9498d1e33`  
		Last Modified: Tue, 04 Feb 2025 23:54:01 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad142d7b5b157fd08e9b145eaad61faadc1dc536e10fcc50a65441dd3734da2`  
		Last Modified: Wed, 05 Feb 2025 19:30:01 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7692c35ffec576e057d1cf687f0d918f724b9331bb08009aee0d33014b498b6c`  
		Last Modified: Wed, 05 Feb 2025 19:30:01 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ec8ce5b9b51917583bd00b604d067b001b0a3a55bbd9ec7ce85ef2f6009053`  
		Last Modified: Wed, 05 Feb 2025 19:30:14 GMT  
		Size: 433.2 MB (433175206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:902773e581173947e2b07aeb4ec31f6c633e028d7f5afbdcb33f14f9a17c8826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8e6c293c5dc850b76d225dbbb1053dec5ee3f3717f7d6b157227810bf8118c`

```dockerfile
```

-	Layers:
	-	`sha256:6c71e8133c6bf41b91ce78d457f23bf5cf33f36bfd637aaf141e44894904d0a9`  
		Last Modified: Wed, 05 Feb 2025 19:30:01 GMT  
		Size: 3.5 MB (3531025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7c3201c90c42ac676afc8e11aa9b9044d90d2028844310cd34530af422354e`  
		Last Modified: Wed, 05 Feb 2025 19:30:01 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json
