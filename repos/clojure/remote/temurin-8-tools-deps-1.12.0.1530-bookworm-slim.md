## `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:f4d45822b46c51f81673c1bb7c3e0b13392efb8962a91e45a97218c01853b007
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e40b17295e2cf0f1cb263b357b976b76e32ac71f3033d6cfd85060296d624486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152477228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2caa0cd4fe2da46a992dfaa8114ac979ed7b27cf90286e026f0942f20440fff`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9482b26d5cb7220aa2b058cf61b9a52dca25e8ad321f92f17ef640b39227893`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 54.7 MB (54721244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2372eb1019cec59436c8db38cb9acfc36f87be1132aa4282fc3c6b054ce645`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 69.5 MB (69528078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e651c427fad7da9735b555a234e2f932f302627e743e0c0654a00d084466ded`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d8e20d74b806037d17799a594736ca83e0b28a351b25b05549b22774cd7f7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310eea8d7503406b32b8f28102f9fd192524663ac85337654155bfae08e2e66f`

```dockerfile
```

-	Layers:
	-	`sha256:70a4977ff62e6b942341f56ead2497c96f4a9d10cafbe4dbc5e8500216db2f50`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 5.0 MB (5035575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9eee349a3754b271de992eba8096991cf3cff997d158f010afe80bf2c1570ec`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08ceb21650cb3010609f60fdea87da623466149997f746394912e23d5eab42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151267739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7034c92ac52f706ef6887b27b6dc49e61aa2011afdfe7ae046bf5e9f27352a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816d872a5165a56e55df8bea6933fd7114deda268519e3d3e5ba5725dbdc956`  
		Last Modified: Wed, 09 Apr 2025 17:12:23 GMT  
		Size: 53.8 MB (53822736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a960f6b11cb1ad17bf3c05af39a91e9f4f127376ffe0c5ed9890af0d53d7cd0`  
		Last Modified: Wed, 09 Apr 2025 17:17:04 GMT  
		Size: 69.4 MB (69378039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959de21762964d4ba64c11c4cb89baae63ff52fc2a633cc6a7be254991deada3`  
		Last Modified: Wed, 09 Apr 2025 17:17:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d0b8a2eeb32899af355f157eb8244e6298fcdfad1b6c3007bca849e9c522fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade8666d8e5cfd02edaf09c1a8acb0dbac3afe03c3539f0be2db55a9a8a994b8`

```dockerfile
```

-	Layers:
	-	`sha256:321819a00e00fbfc8fcd1032dde90bc7d6f92d40870983c31616b7fed4d6949c`  
		Last Modified: Wed, 09 Apr 2025 17:17:02 GMT  
		Size: 5.0 MB (5042034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fad4df2a983f68716a9de155731587eead9bab354c3b7ed07677caed0430658`  
		Last Modified: Wed, 09 Apr 2025 17:17:02 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
