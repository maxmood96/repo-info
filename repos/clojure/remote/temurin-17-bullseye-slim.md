## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:908dba59bfe182eb7e341a1cd24e144bad00c2d04bd286c5b08b8d2976f7fd8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bfac13c5112050dfc4872eab73e3dfb0e2b1b41db527fe800fb6d5a55e807af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232266782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c55b8bf70572d4e1ccd6bd7fc7c8f7de95a45e9e59566ee11cad3f4c811e230`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:17:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:33 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2bc06a34f10c2e2601d77a2072bdbee2b811ad3e8568047495c1222602ba4`  
		Last Modified: Fri, 19 Jun 2026 02:18:07 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4dcd2363a69b97bb341055a48fb53752e3f4db010624351cf3b21abef97042`  
		Last Modified: Fri, 19 Jun 2026 02:18:06 GMT  
		Size: 56.1 MB (56100030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476ef384f21c97f4889a666e0325e733351c3d4aac79cbc364f73801322a6c3d`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bf64cec0f2964238d9826aa40d9e0a9f10b51f71213be2e3899369ed3cc6c4`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5e1be7844e240267d3ed71ae12883ce5a0665064dfb721401c0a9443d1b39a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dc799ef89892cca06df0b56e5f87eb38de0d10807826a7f43b3525327cc2f9`

```dockerfile
```

-	Layers:
	-	`sha256:262b4aef7b3bd3c5e5bf9f22f23d5c2c55ee273468c04a9ae4acece697002a9b`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 5.3 MB (5319473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e63e99c5f95bac37984f60174c74fabb6561bd99456d799eaf5dd1d90162277`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 16.0 KB (15988 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9fbd9e99466c80adaf8825f9f5b0ca2fde9d8b4ee89f847723343cf599d58ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229738966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18008a57602fca723d112f18ba0ebc26c3de1e1b71ca97fbd4b7d30f77523820`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:17:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8081cc972355522a44fd27f6c936facd55a46acd36b65bb900619c02973f6c`  
		Last Modified: Fri, 19 Jun 2026 02:18:11 GMT  
		Size: 144.7 MB (144724298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c74f4f7ea276d0443717b6b4f0fcef1e8ebdf642511e419c49683989ff50ee`  
		Last Modified: Fri, 19 Jun 2026 02:18:09 GMT  
		Size: 56.3 MB (56267473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973eced70f5b21f0f3752bd7b59475643c7bc2151cf0a85926507fdfc712efbe`  
		Last Modified: Fri, 19 Jun 2026 02:18:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3c5af5340021d726aa75dece2969b66da82eb3cc1aef05d8cec0d6af46b76a`  
		Last Modified: Fri, 19 Jun 2026 02:18:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4484f208d2c74a5bb81ebaa4481e167610c6232e964da6dd6a67ee67325ba5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9fce7fd4151265ac6231ff358af5ef7453e49e8918eed3044e88949aaf87af`

```dockerfile
```

-	Layers:
	-	`sha256:5acd1a7d2b86c02769999488c2b61855a6ecab27a293edffe699c57f09ad028b`  
		Last Modified: Fri, 19 Jun 2026 02:18:07 GMT  
		Size: 5.3 MB (5325205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d148070108dd816fe57dfc486bb30b93c0f2bfa9fb33acce4123f0b52827e4b`  
		Last Modified: Fri, 19 Jun 2026 02:18:06 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
