## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:3f389772e493a044c3e24de5f1a56635cb91247ed5919b234e93c90e8828711d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:58d5355c599eb822d44e0a7cf0115d61b045240ed96c84d4128d8efd867d45c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184195577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d952945f06ce4bc563eecd7bcbf27f0dc5e95834af01f9ac075bed830d98f4`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29095b55e076344a3bbca81eb22a309e8665171416c55854c07118e296e1447f`  
		Last Modified: Tue, 04 Feb 2025 05:27:47 GMT  
		Size: 54.7 MB (54721258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c9fe67c6daa5241ebbc1c4c6642b4fc04176ccdffec207a564f5e84bd13984`  
		Last Modified: Tue, 04 Feb 2025 05:27:50 GMT  
		Size: 81.0 MB (80993987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4332715fbd8b7b773fc7b7d227d14b858703e74e9f04c023bf9d60f13cece2f7`  
		Last Modified: Tue, 04 Feb 2025 05:27:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c75feb9b654eec772f8c0bcb2ac6dff3dfb8b93d1563d61b1b5bbeae220194e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210cda7d221ab2a56ec32945b8f1ff8fb2a244c6deecf41e0c293e1a8d01cef2`

```dockerfile
```

-	Layers:
	-	`sha256:2e9b9e797c3e4cfd87c9463639b1fdc40c8b4cc9fca3307966504c04d575ac2c`  
		Last Modified: Tue, 04 Feb 2025 05:27:49 GMT  
		Size: 7.3 MB (7292688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019760b00b768c24f7f1025894045a0408a53e593b8bfa0fa7297db7273e4996`  
		Last Modified: Tue, 04 Feb 2025 05:27:49 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83c118a4a4d8daadcfea5c369992a823f7c57082fddabd67a2f63b9dc6e3003b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182975549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fb3d44b836fb9eb750ae440c6e98f965875f4676e3c0a65f56aa3cc7d8c0a2`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73158f818927f3d5d74c42ecfa65f28017e7d8107b6335006d95965106742209`  
		Last Modified: Tue, 04 Feb 2025 23:24:17 GMT  
		Size: 53.8 MB (53822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f51f1c5534c253ae924a133583a80f27e505ac8f39b8d48b602fb2bbaee4865`  
		Last Modified: Tue, 04 Feb 2025 23:29:06 GMT  
		Size: 80.8 MB (80845576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36669f116b4e68b7c87c1b4155ea7a89da191a392e49cb19ff51253ec3ba90a3`  
		Last Modified: Tue, 04 Feb 2025 23:29:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b4ceed9ed81f53b8ffddb8724049d3376ab60bebdadba83f634b5d28ffed0579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c5ba9b6cd26612001737736575fe3f9a198dd9d9144894f5cdbd01219cbaca`

```dockerfile
```

-	Layers:
	-	`sha256:cc0d6885364499e9efbce2550deca71a0765e6618c75a6798111dc0a895eeb89`  
		Last Modified: Tue, 04 Feb 2025 23:29:04 GMT  
		Size: 7.3 MB (7299149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57422dd16d1bf26d420e39ae967827dea3db764d91d9c7263c570306c0e43015`  
		Last Modified: Tue, 04 Feb 2025 23:29:04 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
