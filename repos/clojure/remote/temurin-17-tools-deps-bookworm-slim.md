## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:119f63a5afe62b4e70fb8ca6886df36a5085a06fdfc9a1f558419e9a2edc987f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c23825a18653551a3c5beed89ff9fc3e967fb50a8aec38b2aa1f75040e5945ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242311336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98885aa2757a4ea1b333515365d636154847993e78abffb3a45d37df5259ce3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda7d9691b1137d7fa30d3ca6568a945440f210d6495114d54a9ab0ce71bb421`  
		Last Modified: Tue, 04 Feb 2025 05:28:14 GMT  
		Size: 144.6 MB (144566522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2586c6218d31cbdcd19afe6d3239321aa0008fbc81ff077dac5d55f9a26c3`  
		Last Modified: Tue, 04 Feb 2025 05:28:13 GMT  
		Size: 69.5 MB (69531477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678be00ef9c48f5fdf069a0e189758aa7200c45a4de6e16c7115b5a88b6e5a3`  
		Last Modified: Tue, 04 Feb 2025 05:28:12 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b820a59c6f220306c6e1c8197b9731e809d0055e62c531de78cc0d76b81cb60`  
		Last Modified: Tue, 04 Feb 2025 05:28:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1710468420132d43a4c797dc6e32c764922b2892d80590e8ebb27d526e636b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590bb4c3c2f2db0f0a1c74f604563ea2a395d19d5a8c706e7640d683b78d63ce`

```dockerfile
```

-	Layers:
	-	`sha256:518e7a482b064be1479f65154337dd96f0273735d4357b7df31d993b3bb80717`  
		Last Modified: Tue, 04 Feb 2025 05:28:11 GMT  
		Size: 4.9 MB (4912567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6922d6d7f6ae8908d251ceeffc3f22682f03d72292613419578341f0bbea8cdb`  
		Last Modified: Tue, 04 Feb 2025 05:28:11 GMT  
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
