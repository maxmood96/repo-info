## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:e63cfad7d2a8384e72810567c9f2797a649ebc0c225e696ed7ba078a27ac5bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9a8bcbce2cd1ee3ccf752be2af6e0cfa72606849320fb287e4b359051ed71454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242311327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ffff2c93c57cc3702aa686d7b1a8efb61711aeeb65256d44a1877ca2d934ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cb853c36db10cf61f94efb3559aaca3699195763cbf0f41d25d81cb4e8065f`  
		Last Modified: Fri, 31 Jan 2025 02:18:06 GMT  
		Size: 144.6 MB (144566498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7c9acd83940422dec857e3581efd30a9ae6d1e31276311c2dce75872045f22`  
		Last Modified: Fri, 31 Jan 2025 02:18:05 GMT  
		Size: 69.5 MB (69531370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a604b7f78c608919d607cbb787fc43f78fbc335a620991c45fee0588cc875`  
		Last Modified: Fri, 31 Jan 2025 02:18:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30f9a19dfebc66cc29543d54967bf16de33fe3297d2f369476a98423b14462`  
		Last Modified: Fri, 31 Jan 2025 02:18:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e3cd1c3a595673ed67254cf63d9c2484462b0ad138e2c414ce91547a08831c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c58b5fce0a8df4cddb3d560f86e4a736b36b2bbdfed3c597e229f31d658cf0`

```dockerfile
```

-	Layers:
	-	`sha256:b2a545b03ae6cfd829ca7d02ee5eb2b447e5a1fdd1dee1d3fde02fa0231e987c`  
		Last Modified: Fri, 31 Jan 2025 02:18:03 GMT  
		Size: 4.9 MB (4912567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c8011984901654c714560d6235163ebb2eff2f38acdbe40545cecd1a65d2e4`  
		Last Modified: Fri, 31 Jan 2025 02:18:02 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acb3b76cd785930fc910c0b985e6d56f608da8c33572ce42bd1b12903eedfdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240878365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2379176bd343b68588bd875ad8f1268b901dc2bac57169131d23fd3f4095c3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb37cf7cdecf9b1e9726ccfd0bf85f9f48dfbda7df3dfa592d25d1e074d5bb1`  
		Last Modified: Fri, 31 Jan 2025 05:11:09 GMT  
		Size: 143.5 MB (143454568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a95fab687c20d25b417852d2ed33ac697009010a61f54b1d4bfedec9d0cb1c0`  
		Last Modified: Fri, 31 Jan 2025 05:16:03 GMT  
		Size: 69.4 MB (69381727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adb84cf4123bf34269241baa3c7cb6732e31de39a25c6d0b6e728fed3dc958`  
		Last Modified: Fri, 31 Jan 2025 05:16:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798ac7e64d218f0f94a41ef5722db76b3a4a8413477fec7ca8b8d124236d810`  
		Last Modified: Fri, 31 Jan 2025 05:16:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84cb5bb673d84834780a33ef8c3adec84f8fe80fb39e85ce893912a3b039cd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9024acab2183860fa7ca1cf96174d7a432f8f6ef08edb063222300f70fc3515e`

```dockerfile
```

-	Layers:
	-	`sha256:aa33f798ec15be736102dc2a26a4d4171f42a87ef99deb982d52a089f18446d6`  
		Last Modified: Fri, 31 Jan 2025 05:16:00 GMT  
		Size: 4.9 MB (4918328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407cc711695e242a5d6d251d6b594ffcb7daf1f21bfd3b74b26a2ba2e69aeb1c`  
		Last Modified: Fri, 31 Jan 2025 05:16:00 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
