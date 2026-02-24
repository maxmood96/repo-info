## `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye-slim`

```console
$ docker pull clojure@sha256:f58c5831368b7907ddbb20e2810037d13e6741d1a81eccdeb81143c9d0406000
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1ac7d56f120d7073084208ae4c2ffa721dc008b1dc2fc7089467633c07055c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247279739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcc2ca92080cbefc8f79bcfbc9fb235b19a947ea88e00dccc87683295af7a2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:56:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:19 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:56:19 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:56:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:56:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120d53c14bbfe57b0d5b8a0de85bf2e89d57ba18577d6cda3a5059a318ece81a`  
		Last Modified: Tue, 24 Feb 2026 19:56:57 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad7905dbf626bf319abd96c43852a7b7cec4077d489e6f86229db36bdc8029d`  
		Last Modified: Tue, 24 Feb 2026 19:56:55 GMT  
		Size: 59.2 MB (59163222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235c2066d5c949d44262d263528280c9247d56944787024897a1832bfaa2ffd0`  
		Last Modified: Tue, 24 Feb 2026 19:56:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a4a2db3cda63ed7ab5ed7198284e11a4bd20a13401fdf6c316fed6c6c108ec`  
		Last Modified: Tue, 24 Feb 2026 19:56:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77df7d5df4e9865f36cbb356e5302f5dca4d8f45f9e42133c4687a166214b7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d517f4af5e7e628ce8ec63f2931436c0c5c0681feb798d56c8a59a176d5d2996`

```dockerfile
```

-	Layers:
	-	`sha256:904e157445f5a673cfa5108eeb9ef2d205e37e2b0e6b61ccd5c2f08f8f1012ed`  
		Last Modified: Tue, 24 Feb 2026 19:56:52 GMT  
		Size: 5.3 MB (5322016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5c189a080498b1afc44bdb6c5402d7cc147d8b1c125b0d3ff6fc5d54e56732`  
		Last Modified: Tue, 24 Feb 2026 19:56:52 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf85969b417d905fef62292b44da914cd698d8ad178917d06ed7078254d69752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244181990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba74729e204e6fa9b1c2242a6a2885fb844972daa75e6c01757d52234cf4a3f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:59 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:07:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:07:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15696d268a7544c981e5972322cfa93906fd30e21f8f7b2b5c4a40bd9b51e499`  
		Last Modified: Tue, 24 Feb 2026 20:07:35 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea49286c7eba0d44af1aebd971c11c205c3fcf82ab4b123fa85c35ec763af46c`  
		Last Modified: Tue, 24 Feb 2026 20:07:34 GMT  
		Size: 59.3 MB (59303388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e693ccc336e224333601c59201568a043e01c8a8e98678501dc8032a73712b3e`  
		Last Modified: Tue, 24 Feb 2026 20:07:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d94ce5f4cabac0d8a66d994b508029e93aee247fc7ced25e80627d67e83bc81`  
		Last Modified: Tue, 24 Feb 2026 20:07:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2815b9870deba814e2ee7763dd39b19551b6d900c42a36623e2ea002ce9290a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b7abe96b84b304fd87c82350d223db1936de2f0cccfe8488f7069bcc7683d`

```dockerfile
```

-	Layers:
	-	`sha256:d51505ccc21eebaed371ff19c2ff61160de2a6816d254a01e91ac1f9cdab7b7c`  
		Last Modified: Tue, 24 Feb 2026 20:07:31 GMT  
		Size: 5.3 MB (5327748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d0124c4bd8bc8612c9351efc119f6229f5e025d5b9806447e1d7e701dec7df`  
		Last Modified: Tue, 24 Feb 2026 20:07:31 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
