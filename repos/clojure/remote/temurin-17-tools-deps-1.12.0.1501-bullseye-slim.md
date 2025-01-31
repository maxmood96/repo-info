## `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye-slim`

```console
$ docker pull clojure@sha256:c538433fa0bc6c9735b493bd0290bd07532bec42754df17a54baa8a64c5a222c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:28f59d25869aaa039c4fb62a8ceb3b5e8cf47f67bc77ec09ff790d63e2e3bbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233608022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00dd84b150f2da280d7f1d18ec148b1f3edd2e05cb5fc6e1bcc0581292780bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bdcae561b9adcc11b05409921a57db1dae9059b99c6b983b5bca1dba6f7d34`  
		Last Modified: Fri, 31 Jan 2025 02:17:55 GMT  
		Size: 144.6 MB (144566554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b570b0bb78e4b909c8698117364a2aec4debcce57ddbd92953bf70ba425f494`  
		Last Modified: Fri, 31 Jan 2025 02:17:53 GMT  
		Size: 58.8 MB (58787760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f3da68d4a94abf26e4c50319bd78fd6fc65000ca75f93cc4021ae8d4e0a67a`  
		Last Modified: Fri, 31 Jan 2025 02:17:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8143c3429f48d691cf32f38301993209affc02ccb26c36ba002f2f872162f87b`  
		Last Modified: Fri, 31 Jan 2025 02:17:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7dc1a6889c679e026fe9c382d337245216da230b9e2afced79ad1bc37bb0aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0102f3730465341b07e4a85fec6fea62f3425d30ced3dfa4326ead8ec7f05a8e`

```dockerfile
```

-	Layers:
	-	`sha256:121cc4fa84d8dc5b49230c9f3bf38154cfe768ead8f4441e4ae7c492c9462667`  
		Last Modified: Fri, 31 Jan 2025 02:17:52 GMT  
		Size: 5.1 MB (5117067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cc5b1ae7a91b677fb7c1d1eeaa391361de43645c2909aeb2d23a3270423375`  
		Last Modified: Fri, 31 Jan 2025 02:17:52 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:932dae40f31d2e58376a88228f5ad5e8d4222df0129a5f8f4d9f0f1c7d15eb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231109667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7561a6ec745bd70344019b51dca3e60bdfed432f7f174d732e155652bf691d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702780dba269095091384ce9987de0680435590fb8ec57cd60e694133d6db9b7`  
		Last Modified: Fri, 31 Jan 2025 05:17:23 GMT  
		Size: 58.9 MB (58909125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a4504b60b8068cf7cec3976f09fd51a1b292b78173e3a22d4420803641c27`  
		Last Modified: Fri, 31 Jan 2025 05:17:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a40a4e0274ff4d4280a548f90cb2d9e9a1a6686bbad68d5aa7d28e6c58208c`  
		Last Modified: Fri, 31 Jan 2025 05:17:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3ab5c33002203268a2a91566c3cea81e1a211c513d772203f3c23de4f04f6fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab8bf190ffa6463c8815bdac753b7c7ad01b5685d98705eb3a17f101eaf9ddf`

```dockerfile
```

-	Layers:
	-	`sha256:6fca6adb6b5dc2a36f08fcaf2eef18411580db17d28cece7e2b97d306966dd4d`  
		Last Modified: Fri, 31 Jan 2025 05:17:22 GMT  
		Size: 5.1 MB (5122799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c2a81e3d825e401428aa1e4df83147f57ff205367f969ea5cf3d2b2fafaed1`  
		Last Modified: Fri, 31 Jan 2025 05:17:21 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
