## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:3de1571a3103dd9a7a86e5b0884f46d1694fb6d74089adfa6f0a2d0285cc1502
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fcd989f8de734162b5f01672d675f95f54731c7bbc33faa1d1b1e53d63baa929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178564892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab59516411fbe38fd9f09e57e1d00f66c6e5328ccf8ec6c0870e6ad94488ae7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:05 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:05 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ee8aa26056fe0f6c56e49e5a0b788181fdad476c68cfc92e8e190e3d723a5c`  
		Last Modified: Fri, 15 May 2026 20:13:34 GMT  
		Size: 55.2 MB (55198722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5294ada8e8db87d2191028cdbf4804fd10ed8600a1cb19c0c46299ad3db0d469`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 69.6 MB (69602180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c163ba15fa5ead3e13f96c38a56d22cf05e8a167a0da29077cf66a013e0ca56b`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c0af4a48aa048dd7c5397c5f0e30434ebb8109fcf3e5ae9ff92d2886f5c3712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49f06f93f021abef4b4811d83b35463b57796f094ea6b16986dfddb97e33de1`

```dockerfile
```

-	Layers:
	-	`sha256:782ff131e65fa8d72dcac10a23f42eef7bfa2096ee024307fd8a0c9cf5d1efe5`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 7.5 MB (7528638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d2c344121880fd7ed749210d0658f390e48947fa58933fb6c3bb5fec5c9464`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d59c7f31eb3f6e9ce58ed8a0b01ad6f20af1c46947ee015cf0987a926f0b677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176297709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7ef011d1ab08531163063225cdf186086ab95e2f0f57fcb5513dfc890d3620`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:12:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:12:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:12:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:12:54 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:12:54 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360285be71c46ce369dca3213d431e2a076c69419fa48fc3029a9192287c2e43`  
		Last Modified: Fri, 15 May 2026 20:13:26 GMT  
		Size: 54.3 MB (54272904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60370579b87a4be051097a6315a8d970a0613b39068c1bd8663aedd3cd080682`  
		Last Modified: Fri, 15 May 2026 20:13:27 GMT  
		Size: 69.8 MB (69770948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bbce5dc2aa7a299db64d18caece840bed0979c597e446c0638d8ab9e9d9813`  
		Last Modified: Fri, 15 May 2026 20:13:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01ac16f393ef138435102881a162c51af12d5d8a50933135900bc627de0f0417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9928798be54be594943fdb3c2489deb6f607fd94162c66a3e3bd750c8f2cd8`

```dockerfile
```

-	Layers:
	-	`sha256:935c5b497e074cafff0c6d5aaa576a709fe086d2d9938789cabfe4a0f3ba92f9`  
		Last Modified: Fri, 15 May 2026 20:13:24 GMT  
		Size: 7.5 MB (7534437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37f4b3a3e7484e6684ccb470cd33bf6d8c42bc7fd37bfeb4e3a2b714dbbdbb7`  
		Last Modified: Fri, 15 May 2026 20:13:23 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
