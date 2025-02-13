## `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim`

```console
$ docker pull clojure@sha256:49a00c9bc7e7d9387287bbafbc7c6bc8516563a004c92e7dbc9acf864a305cf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - linux; amd64

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
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abc1c181c1449af26b030b9b0f8b1bc07de21603f9bfc4163b7b2364f6e9fd5`  
		Last Modified: Wed, 05 Feb 2025 14:18:17 GMT  
		Size: 157.6 MB (157585860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f26370831911dd52c4e040f61101bfada59222b7e4f61a2b1c1b82469e68b`  
		Last Modified: Wed, 05 Feb 2025 14:18:15 GMT  
		Size: 58.8 MB (58787808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7b6f676e1bd2138d8ca2943bb4920a22df6eb41d2f7c9a1229aaa60cd0725d`  
		Last Modified: Wed, 05 Feb 2025 14:18:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0cac7ae494b9396c7f2232b3e144bc709c990049a969145fd938d36b90516`  
		Last Modified: Wed, 05 Feb 2025 16:56:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:82a50a5d6cabc0e0f66ffb20f8df28a87480bb277933a12d66b81d9a56a9263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243514273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f630674a9f8196556ae306038d45a0553de34175b47035323312fc93e56a1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1444b3218878a3b35e8951a2bc0e44515e7eeec8e85c72e00762e9498d1e33`  
		Last Modified: Wed, 05 Feb 2025 10:11:28 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5122ef6ee995187b589d34e032b1beaf447256f2d1fa25ecca66e98731f36`  
		Last Modified: Wed, 05 Feb 2025 10:11:24 GMT  
		Size: 58.9 MB (58909147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70c1c1194c8083918ad48c6a248f53e17c3510c9d3d0f0d06a4218b39190949`  
		Last Modified: Wed, 05 Feb 2025 10:13:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dc9f97ce1a50a3cc2418e15f041364faae1dc901cba8061ad298274b4428c4`  
		Last Modified: Wed, 05 Feb 2025 10:11:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9af2ddb617126cbbdd9dc66d6abe0ca6c07ce00f11cccecb95768c9d46d0e513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9bd8ac029df165c94efc9bde4df352d21e6740f3cf64c92f4ca55b05e46d14`

```dockerfile
```

-	Layers:
	-	`sha256:fbdedabec0bb366038596a716f6af52eeb2e14ad9e238e91a3077657a1eeae69`  
		Last Modified: Tue, 04 Feb 2025 23:58:19 GMT  
		Size: 5.1 MB (5126621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb00926d4204f9fcec93ec2f7fc79a2a3cd415f54eae38e30ece0a50507c1029`  
		Last Modified: Tue, 04 Feb 2025 23:58:19 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
