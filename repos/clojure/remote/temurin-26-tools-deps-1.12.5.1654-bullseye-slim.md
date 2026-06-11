## `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:8d2ef27548b803e41ee96c3f258caf59eef6395fd5a414e766da31db0d4597e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:977b6adb778b804229fd58a521f8f951f760f13d72e9089ac23ac465437537fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180885969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16988c4a5049dde45ed906bda139046a9c6124d83a0ac7cd678cacf97ed795cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:07 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:07 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceadb361438e0abf4a0bfbcb86651bb13d7212b9540d98c21898d0202229f4a`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 94.5 MB (94524374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea7cdf4d8a9715ca810c78e7b01fd7c471767e66eb2b9c812f5f46098ce467`  
		Last Modified: Thu, 11 Jun 2026 01:22:39 GMT  
		Size: 56.1 MB (56100298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb646535f2d3a9dbf3b163eabc069124513a4ba66e0e7bcf3567e30631846c2`  
		Last Modified: Thu, 11 Jun 2026 01:22:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d014a5fb6adefa7c3792a53f923073da9b995739e4d5359389b20c12749f767`  
		Last Modified: Thu, 11 Jun 2026 01:22:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:709392890ab791448fdebb5d27d63b96cd7f8ac444e642224cc6918ecd31b888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd2fd77072c6694cb09e9a1583fccf0b2dc93df8930c461e692a68095cca1d3`

```dockerfile
```

-	Layers:
	-	`sha256:cfef156734132fe522ae0dd926aa7defa27f7faef8e3ceeb98c2502a136da8a2`  
		Last Modified: Thu, 11 Jun 2026 01:22:37 GMT  
		Size: 5.3 MB (5282740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:366c551202df490a994ca22ddac747fa7f65bd3544e56a991f98a59fd8b9fd84`  
		Last Modified: Thu, 11 Jun 2026 01:22:37 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08cfe6f0848374f7d8ad81330239b51d9469d30b613d991c3e52aab246d8eadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178519031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa93fac53d5e1979f66b9745fc6184b077fa7c0ee28e64672c4fab8897515546`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:26:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:26:23 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e86049d9885802bdf593ab8e2d4cd8ecdee7636a3a3149a0d849aa5031559`  
		Last Modified: Thu, 11 Jun 2026 01:26:57 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70c808150c747ae4f4dfead2a75cd248dca047b391784021cf1762453d3ae57`  
		Last Modified: Thu, 11 Jun 2026 01:26:56 GMT  
		Size: 56.3 MB (56267490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78ab34f314895476733e67a0a2e9e8e6586df3d73f4c9c81ad3ac7766ee3351`  
		Last Modified: Thu, 11 Jun 2026 01:26:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4808af0129d7c4d6ad9163ddccc5e30d7d2f72dff07773c8d33e967da5525434`  
		Last Modified: Thu, 11 Jun 2026 01:26:54 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dbb86252ebcf04584c13f072d086a39df4e245f3296832b235f8729be9488efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff67b08e811f81efad0cdac90e9c33ee551d3b97ab630c3cd184bb9f7f27cf9`

```dockerfile
```

-	Layers:
	-	`sha256:27ac73e8e04b6daaa45ca402cc751758bff3650d63777e6da1d6f7dcaf69c255`  
		Last Modified: Thu, 11 Jun 2026 01:26:54 GMT  
		Size: 5.3 MB (5288469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d740d17d76c98eb066687522addb8e54bfaf09bd715882b75c3b78053d7465d2`  
		Last Modified: Thu, 11 Jun 2026 01:26:54 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json
