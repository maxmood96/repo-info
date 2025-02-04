## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:c84a4bded938bdf97c9746ca1dff41dd2218f3161827ae5a85f7511903b044c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a8e89ab9d80900f81c8abab279d8aa15112c743facd86c6c88e8838bec697acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233607954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b9ad39f11eeeba7130cf126bc701476dc770323ee3d8ae7f0699bf56ab47a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f354d0c243639024e6b8ebe6a50ea49a87b3f125a6b05c59b864607763bdcebd`  
		Last Modified: Tue, 04 Feb 2025 05:21:28 GMT  
		Size: 144.6 MB (144566522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4b02f4c1fefd727d3cd53a16ce49cd60b3072a9c48bba8d94eafb641139539`  
		Last Modified: Tue, 04 Feb 2025 05:21:25 GMT  
		Size: 58.8 MB (58787804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf34abcced0b9ae3a567eb52e6407e150a0afb607520d3be17c01f1703d698b`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2838a0bb4d9287b3a6cf2296789271a55eb40c92621431fcb6e946fc57ba9fc7`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59b165504b77bc1e22e6aae43d7482ad596bd80c070c4698c6731f6e6887f0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fa1d7ce0fc85eb4940d1cbfdc60f9a275eb6363169726f4a6c0698cb252130`

```dockerfile
```

-	Layers:
	-	`sha256:4527aca0f536f156749b7f92e4a6710857d41e8269f6c86614318a38930eaef7`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 5.1 MB (5117067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79fe451a448fe504209d6332d198d9cf8fa6f39bd0994c42ccf73af6e2a1eb9`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

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
