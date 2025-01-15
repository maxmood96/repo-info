## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:ecc56a0f5b03af18e31d84b28d94127469d16eb163a5c273deb7b36928fff7c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9ec307ffd0abe7af37326888cf6cbda2b66d1902d2a56dc3afe9be9735003cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233092884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5473bcd6200db56ed65ea6b303bc1a9803d2e23b7b1dae16fe811c1c5ca3fddf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c032c85b01daca122a8053c2fd383b8257f36a67f10070d729019ee0ce34c67a`  
		Last Modified: Tue, 14 Jan 2025 02:43:28 GMT  
		Size: 103.6 MB (103633965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ddae3ae298271774595c0c051f986b65d61f8eb6edf19ee150e8eb37598fdd`  
		Last Modified: Tue, 14 Jan 2025 02:43:27 GMT  
		Size: 81.0 MB (80978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6eb5ac73d4758f6647002271aa7a0a30d91f4af8fc1efe7b64a43553009cbd`  
		Last Modified: Tue, 14 Jan 2025 02:43:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c29a5aba4b78b29a85b76fde9fa8d3ff28b38af8484ce69ab8f5a4060eb1823f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b19439dff2cf9285a0932d437c70d363893660ef8e14ac8aedd2e1e9b72515`

```dockerfile
```

-	Layers:
	-	`sha256:32651110f26354fd5e54834f1a6085b001f76ad8f8f2e3b46550d227a5c87751`  
		Last Modified: Tue, 14 Jan 2025 02:43:26 GMT  
		Size: 7.3 MB (7293298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c816f87ab7c28ad7f57878cc0e8c25c0830eb55a802a5b4fa99981b3ceed30`  
		Last Modified: Tue, 14 Jan 2025 02:43:26 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8785c2bd4d0e37e64453307d246de18c5947f7907b75dd16948e39b21167bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231881496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6f3f742e252c36f8692056cf7c697e2fbe42c5e4caca3c361ac534a89c4d42`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde06ded3b21717f7750e160046bdf99c7f6dd63c53555ea505430f5e141c14d`  
		Last Modified: Tue, 14 Jan 2025 12:13:16 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdc4fa07d84150791205a585084d110c74f3774e6147ff075577f6a259f4aac`  
		Last Modified: Tue, 14 Jan 2025 12:17:00 GMT  
		Size: 80.8 MB (80826241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8144f4dc4b96e7b3f53ae8a9b89f8d4644e23c9295041716efe8508cbb667e6`  
		Last Modified: Tue, 14 Jan 2025 12:16:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:092edba2aff7db1ea90b727051d36776a267dc3e09098734833e39ec12bc2a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3cfdcf02e28c75f0a8ed0bf0b9470eb71aebc949fc88849a28e34702477e68`

```dockerfile
```

-	Layers:
	-	`sha256:ae82f065d2d8aa5255ca7c1c81b2f71fbe7dbf952e9330ca476db43dcfed5b39`  
		Last Modified: Tue, 14 Jan 2025 12:16:59 GMT  
		Size: 7.3 MB (7299759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175ae0fea931cd8615827ead6a0840d25ea51153e77f14fa9b5792505a1c1608`  
		Last Modified: Tue, 14 Jan 2025 12:16:58 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
