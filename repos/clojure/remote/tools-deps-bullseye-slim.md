## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e1e7c0ed664132d1cb3d1b5e8197e749c61c2215ffc8a4fbfda33a6bf0746fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ac6e17dd32fc09ce1ad1c157c912ed486344870b3b506f8ff87a574c5069b7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246627296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ecad9370dc389ff7fd89bd3d4332f30abf0f62b457bec4944835d36ded0f9d`
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
	-	`sha256:6abc1c181c1449af26b030b9b0f8b1bc07de21603f9bfc4163b7b2364f6e9fd5`  
		Last Modified: Tue, 04 Feb 2025 05:21:24 GMT  
		Size: 157.6 MB (157585860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f26370831911dd52c4e040f61101bfada59222b7e4f61a2b1c1b82469e68b`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 58.8 MB (58787808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7b6f676e1bd2138d8ca2943bb4920a22df6eb41d2f7c9a1229aaa60cd0725d`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0cac7ae494b9396c7f2232b3e144bc709c990049a969145fd938d36b90516`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c758b0fe4cf08712223ba074d5901c5f5ff6a05ea550d90f018025eb2f9125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259296f2e4c34ac915574ccea88a058c9e58ff895f6775f0d41eec83f78e856f`

```dockerfile
```

-	Layers:
	-	`sha256:2dd7850b4da8d17b177b500e0a69c46e9d8c6608985be0a88a3424b224130a5b`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 5.1 MB (5120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3fd3af530071536cb67b725a9a22c9e8fd0e60f2818610ea5c4898459fbfe5`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccc44e959b2487368f5c48109f36af4d33d63d8d9e964e206f6e19571d5cfe38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243514429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14576c7489440a871a0c7eca30f94234eddcecdf2efd74082ce5b56f05a9c2b4`
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
	-	`sha256:fcc3ea4febeac18700dd0fad07b719e7b913376667b87dc7052c14b9ab784817`  
		Last Modified: Fri, 31 Jan 2025 05:21:51 GMT  
		Size: 155.9 MB (155859332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f75f2c81d912fcec5c1c3db6c9c4d830f44e0ac996d49f824a2e7d3cddf4d70`  
		Last Modified: Fri, 31 Jan 2025 05:26:29 GMT  
		Size: 58.9 MB (58909143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed572e9edd7f545a466f2c81a060f2dd1b60659b89e5b4a6a1beda1bf3316de6`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e2a4b7264471e63b76123d7fbf638a9c7365643e4450c7dd6b075bb3e612b6`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29a928306371b66814127d71b736952215c7bca0a36c9abab138883df7535474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa26cd4cecf314be7e261c4452bb2b6c6e97e53d77061489dee5216c6a9a2ae8`

```dockerfile
```

-	Layers:
	-	`sha256:8299d9636b563e9974c6d4f5145dfd28f49d68e0599e97bf0952a06d63240041`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 5.1 MB (5126621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add9d1526d2aaf000603bff30af59dcf33d4f4907c0fc1be50ffc582736c76ea`  
		Last Modified: Fri, 31 Jan 2025 05:26:26 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
