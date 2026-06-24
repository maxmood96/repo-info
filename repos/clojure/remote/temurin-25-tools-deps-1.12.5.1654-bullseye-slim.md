## `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:dbc7e284c8641fe36cec8005c92a1131479dee332ed4c6b1ae2d9a6b3a1c4413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb4d5dfc445ad1108e16c95347094fdb0228a74a00fdc3d207409fd2e43b6680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178935480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330187bb4c4e4eb68e3d7002b0b4586eb20538e617286be4c979dd5a0dda0ca3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:21:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:26 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:27 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:21:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:21:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb02207ebe98c760ded4a8bf6e6bf3f6811d8809a932944d45f9d7edf7c0c83`  
		Last Modified: Wed, 24 Jun 2026 02:22:00 GMT  
		Size: 92.6 MB (92574577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c239a1961f109590fff1f32af969c597d046fdcb5e0a2da8ccac1d1fb1fee6e`  
		Last Modified: Wed, 24 Jun 2026 02:21:59 GMT  
		Size: 56.1 MB (56100414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deba5ef03c30cc05e33bfc1f7b04ab2edf472700bfa6e71d02480904f33f7398`  
		Last Modified: Wed, 24 Jun 2026 02:21:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416e29febf7b6c3672fbdafd51254ae7994954f55d7cee57df04bfe615ac2a0d`  
		Last Modified: Wed, 24 Jun 2026 02:21:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ca387fa9684be13975dba84f6b16c5e419510ee887d3eae090d429cee97f7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5302618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627183fea1b9281032002d6807c8bbedaf352c50851796f41e1e10edc1a6a90f`

```dockerfile
```

-	Layers:
	-	`sha256:efaf7457940ba335c67e349501e28a98e262ff8d7e23131bf3459cf1cbe8de20`  
		Last Modified: Wed, 24 Jun 2026 02:21:57 GMT  
		Size: 5.3 MB (5285939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df705b76c0bfd29472ef9e7a433382730dcd68968e6eac745e564a8d8c626d43`  
		Last Modified: Wed, 24 Jun 2026 02:21:57 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:522930fb003bc421a0835e95a3177d61507d718c37d21ba3c77c179ef623fbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176557611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fe1ff26830b1eeb3df4654c4165d54cb5e8e6b11d55737c0c629696ec3f8aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:27:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:27:55 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:28:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:28:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51a6dd549f11196a26f65bb948b5b0a187f462f14f20bae36edad52cbf4e4a1`  
		Last Modified: Wed, 24 Jun 2026 02:28:28 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab7d87b87473e8ee72889086cfc2dd91f80bb45b7c209ab8622888e7cdb6488`  
		Last Modified: Wed, 24 Jun 2026 02:28:27 GMT  
		Size: 56.3 MB (56267397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94347dac1ea3102efbdc4b74b8547d7fd6cbf64bc5434c34fa56c840686f9c44`  
		Last Modified: Wed, 24 Jun 2026 02:28:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96e500c167d01a4db57ff4a4adcfae27177b013fce61409fe254039c41f79b6`  
		Last Modified: Wed, 24 Jun 2026 02:28:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cec7707a13209f6462495fccb1e2c25f8f7334f2199a5b3c6ed4d8a4b166d42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a22618deaee46e3de5e34b69e5ed64a06bf78ba2c6e44791ee8a515c59e208`

```dockerfile
```

-	Layers:
	-	`sha256:0ee777caab33a22872aea5a0ecc9e99dbd30e1c13fb547bb331bbacaac8985a8`  
		Last Modified: Wed, 24 Jun 2026 02:28:25 GMT  
		Size: 5.3 MB (5291692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa03605b124e81723bc615bde54ec179d46261f2bc26e45874b29667b5d4a41f`  
		Last Modified: Wed, 24 Jun 2026 02:28:25 GMT  
		Size: 16.8 KB (16820 bytes)  
		MIME: application/vnd.in-toto+json
