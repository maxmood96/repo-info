## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:14a7e8652fc2f4f9a159f80e54e340a5b8936d81c720f7045784dc528417deea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0f94ce73a9f403cd6c3de12b139ea6a520176b5a0ade8f117ddcaaca19151951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235228820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26ad432f46b6206a1bc3f96785ed3b297e056127447a7052f8a2070f651e897`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:26:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:26:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:26:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:08 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:09 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8283282eabeb94bbd1f30a102df65529a94a59a1251665550494cb370a3c5a`  
		Last Modified: Tue, 24 Feb 2026 19:27:04 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95060ee98d9c1f71c007b11d2342eab53ae17f5eb77b297b9bb2eca2058e2d2`  
		Last Modified: Tue, 24 Feb 2026 19:54:36 GMT  
		Size: 59.2 MB (59163050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515ae3f157fda78a82965ece0850b85b237775cc1b9993821fdd8e66751d8727`  
		Last Modified: Tue, 24 Feb 2026 19:54:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:15b8b10835b336ad99e4c925bee4359415d5192b5261689f91594ad4fa476ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba525e2368a1c14e0e7ed64e17f41778237c2086908f591d46f1538605084467`

```dockerfile
```

-	Layers:
	-	`sha256:79281c6cc2aca801c7af5fa945acda55438c83ae1ed31378df3da89ef8b2da86`  
		Last Modified: Tue, 24 Feb 2026 19:54:35 GMT  
		Size: 5.3 MB (5340305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f77062de70159ec4d69a18eeedf50ea31c60b09b915669d06c92d0dafa8955`  
		Last Modified: Tue, 24 Feb 2026 19:54:35 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:52110366c1d7fb66b5436263949eb7205d55a139312fd731aeddde099ad4e43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230549828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08701317d6adb4522c9d9f63c696c828c6677a495154b0b3e1a36a9aa2276d15`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:04:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:04:57 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c691f8e4d1bbe8ce10f408e6d34863fddf9888f42b39c3a49c2a32936ff3226`  
		Last Modified: Tue, 24 Feb 2026 20:05:33 GMT  
		Size: 142.5 MB (142501433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0290773a3d85ff0cbe46bad5a4739b17570be355428b7469d88d4f0f16e51e5`  
		Last Modified: Tue, 24 Feb 2026 20:05:31 GMT  
		Size: 59.3 MB (59303282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f82227f25eede08fab548015fed702d9519b30d724997e11c88b228b0710e7b`  
		Last Modified: Tue, 24 Feb 2026 20:05:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0b22815c215a87555a0b83311908a001af52a2f06ce3624612426a1cd3c56c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7204454be48ac1a62d3aaee49d949c9f46c191687251760c2f782d5f71b72312`

```dockerfile
```

-	Layers:
	-	`sha256:4fcb09f4218cd746a2fc06f2f8daa4aff3a512d46120074c03ead0fceef800fe`  
		Last Modified: Tue, 24 Feb 2026 20:05:29 GMT  
		Size: 5.3 MB (5346655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa77b58166f53c31027f2de38a2a7abcc9b4d72ce7f56af37fb802b9ec6de9b`  
		Last Modified: Tue, 24 Feb 2026 20:05:28 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
