## `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm`

```console
$ docker pull clojure@sha256:b9d5b8de9192fe0808dc6d40f2c5aa93b6a83fdcd8949fe406372a0ffedfcca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f12196cae6b02198ad7da2e048749fa8fd59a03cde3633afbf462c403f004a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184170464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a73e1fcd2b6766ae2d48aa5ce5036b91c4902bb692f22dedca98ce3f1e63eb`
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
	-	`sha256:4d47a21088cc96dc549c7f80e5ffef05865ef045ef3b6952e4a30e1bfdcdcd4f`  
		Last Modified: Wed, 22 Jan 2025 19:41:30 GMT  
		Size: 54.7 MB (54711758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e1f189f0a91a98357ab8bfb6d03538fd580371c8220421ac9f2406a90ef8d9`  
		Last Modified: Wed, 22 Jan 2025 19:41:31 GMT  
		Size: 81.0 MB (80978097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83b7856e9bd121c452158545d115bda5870007174d20c24090a194695532ecf`  
		Last Modified: Wed, 22 Jan 2025 19:41:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2dae4ff30ed67ad94d06ca2c8587cb32074f4b14f4e07af05c5f158dff7c4fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34d63b025d10f969bf703754a60ef0794ff0683c0dc224f86024b2b7930a3f5`

```dockerfile
```

-	Layers:
	-	`sha256:4b5b39e3bf17a8a3132594b956888f0e361baf5889c587d9e51dbcd2797b8b86`  
		Last Modified: Wed, 22 Jan 2025 19:41:29 GMT  
		Size: 7.3 MB (7292688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0683479ad9c41bb867c132dc30e69b5693ce4d85ec97cfd8a3a2532d2ae0a958`  
		Last Modified: Wed, 22 Jan 2025 19:41:29 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
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

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

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
