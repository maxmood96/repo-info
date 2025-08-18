## `clojure:temurin-24-tools-deps-1.12.1.1561-bullseye`

```console
$ docker pull clojure@sha256:6e14e4ba8d8fc0263405a0c8722cbb63f8aba38f0b9d9bd227a3206ae946388f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1561-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7de4ece539e4039a6273463ba9b6e3a449e1698b629f95b363d54c34ac47b57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213192400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b66643b04eb6ae44fca58778cf9ce090f3503cb5dbce1916a4bfb240c497547`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7507c9230c9a26321c6a0172bc176bc6102e69e9c63a0a63117a4d17b4d79a7`  
		Last Modified: Mon, 18 Aug 2025 16:52:46 GMT  
		Size: 90.0 MB (89975170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5cffacbd9f2ef9594fcd708bd6eb8b1b54e6f1f3e419ebaf8028981dbeebc7`  
		Last Modified: Mon, 18 Aug 2025 16:52:45 GMT  
		Size: 69.5 MB (69460843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94247c19b85d6e8cac405e576101c52dbe5bf663fcfdfd74bc397c39968941c0`  
		Last Modified: Mon, 18 Aug 2025 16:54:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0147831d7bd1c33ae60d51fe18c03ab076dd3b7c24ea67e16d8aa0ce071d8fcf`  
		Last Modified: Mon, 18 Aug 2025 16:54:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1561-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0fd6c6f3e1d40d1c10d7e92aa8790180c005b8719a81b3c9092e505ea3d4a1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba89d15ceb342f1da06ab9aea654e5a80f83623d1fbc082ebf2a7d4b296ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a60ae6a43128d595f11cad5cb7f4f7b8fb6eea3b9258c6386f6bf7e12b3812`  
		Last Modified: Mon, 18 Aug 2025 18:42:47 GMT  
		Size: 7.3 MB (7346315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b284981913f8d83d73dc25814949e243a835913f0fab920809b63bb4f8694e`  
		Last Modified: Mon, 18 Aug 2025 18:42:48 GMT  
		Size: 15.8 KB (15813 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1561-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44eb57db50f3fdade9b29217d111ea97ec63fbb6796ec689f87551a8af74058b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210930316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1704ed8f0b2a449202a0748599530418dc3dd1a66ce7bc151bd5275b39aeb5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d7a8f95adc91900fbf66d0e8dd110fea36466371b29ff44ca7ef3116102a21`  
		Last Modified: Mon, 18 Aug 2025 17:21:54 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfdfef6734717af4242810d177d6af6157a3e578e5bed86d1c3d9249b56e086`  
		Last Modified: Mon, 18 Aug 2025 17:21:50 GMT  
		Size: 69.6 MB (69588337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e95feb02aa6b3d891186bc3eddcda8c69c653764cef7b814167b020551ffa6b`  
		Last Modified: Mon, 18 Aug 2025 17:21:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da68257fb77892aa9260cd6d59f1bc090553e56412a2f78fa5e87f16e851ea04`  
		Last Modified: Mon, 18 Aug 2025 17:21:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1561-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a25c702a7e1c153e66557bacd9ec3b50dcef18ecf83383b81a2e56da2fa1eca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7d4ea7632a759bc8cc51035edce9fae0662ea6dc2f61213ee44eba76d5103a`

```dockerfile
```

-	Layers:
	-	`sha256:38703915215ca0dfef32d3a43cb59fb79a0b002472eaf4b30c8dbf3833e6b09a`  
		Last Modified: Mon, 18 Aug 2025 18:42:54 GMT  
		Size: 7.4 MB (7351411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c23090828f1b7ddb96d3eeacd25c4ce16524d655033a2d6d92506388d19eb5`  
		Last Modified: Mon, 18 Aug 2025 18:42:55 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
