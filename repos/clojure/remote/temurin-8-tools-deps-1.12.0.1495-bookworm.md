## `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm`

```console
$ docker pull clojure@sha256:e40cd3ea226336f4d2ca445021ccbef2a7ed7b84718f556a632fcf8402dc94bd
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
$ docker pull clojure@sha256:ef543b0e546c717aeb4760f5c5896479e37697181b23eb8998e43c5b2ada21c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182950408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c0f05cf8c87caa972d6bcc4197f95cfe2f71fb96f9a6c524d1e10bfe3fc7e`
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
	-	`sha256:bee6e7e7404e5fee83e19aa34b8768a574ebe6ad47bb0cd7533ca8f441d20965`  
		Last Modified: Thu, 23 Jan 2025 02:25:11 GMT  
		Size: 53.8 MB (53816418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2903219ada06cf9739cb7cc8091b4029885d69697a681981367ac213203bb5`  
		Last Modified: Thu, 23 Jan 2025 02:30:16 GMT  
		Size: 80.8 MB (80826449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d2aad114c8fcd41d2d9cdef8f9c2717c4109a37ab030f082658a511c9b18cf`  
		Last Modified: Thu, 23 Jan 2025 02:30:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1495-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1f1eba5e5cab39f21970d536e12b6f94802deb71a3ee5abcf704bd4d58dde65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d3f41c3209db0beeb6902171e482db38e3556f7c6320cb1b5f65f520f7cf58`

```dockerfile
```

-	Layers:
	-	`sha256:b28e0c782cddb09fd40e800a566c5cf79e62d1f722e945789e8562e3b5f09cf9`  
		Last Modified: Thu, 23 Jan 2025 02:30:15 GMT  
		Size: 7.3 MB (7299149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e536f3b982369bd72589902d030de8e0f84b9b748350f814873831c470f4586e`  
		Last Modified: Thu, 23 Jan 2025 02:30:14 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
