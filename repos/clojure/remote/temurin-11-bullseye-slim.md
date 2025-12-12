## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:138c0dd279aa3b8cdcf01e882e753c1b8676b153f3490dddeea82a065b684510
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cd1b3b0770d60812ed3cab9e2048393f41a80482e7641421d9a35afd888a9baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234375739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f79b93714cf06367851b66ba5304fc6db607141c3aa65d42aa978aaba058f73`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:32:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:32:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:32:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:32:26 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:32:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:32:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:32:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7b307e07565c880943eda34e196721088715f39136f294e491f136c031625`  
		Last Modified: Fri, 12 Dec 2025 01:36:34 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78b4dd4299b3cb796389dc98e97b3d6ec0dd3cc69ee317b8248f4db33b487fc`  
		Last Modified: Thu, 11 Dec 2025 22:33:13 GMT  
		Size: 59.1 MB (59149976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a34881eb73eab9a8a4a3e2d096f743a7443d222b583f1b40e09497b2e9d030`  
		Last Modified: Thu, 11 Dec 2025 22:33:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7639c13e2c4df8e65b99340fa638147e0a99aac131f3c27b92656837c720bbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e520876284457b453bd102e3f09d1a9731d3bd5a0cdfba0b25470612106d6`

```dockerfile
```

-	Layers:
	-	`sha256:f3fde5a7ee6287a015214f1df41e388891886ad072d511b6fc01b9bcd5a95409`  
		Last Modified: Fri, 12 Dec 2025 01:35:27 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3a9d85d82eef1c9d38fd1102375f69e1b3dff25863859bcdc4b3a75219b73b`  
		Last Modified: Fri, 12 Dec 2025 01:35:28 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7849a4d8cb0ab457a0f16f215e3d1addf592fe4e620fec5a6b838a1d9a221617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229764412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624339b82ec8caa8cc03d1c215de46b7e5bd469bda8a46c3d544bf5a1e619ed3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:38:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:24 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1830643c09be237dbba5c8da5f571b36f7f157a1bbe07cdff026eb14899f8cd`  
		Last Modified: Thu, 11 Dec 2025 22:39:20 GMT  
		Size: 141.7 MB (141731576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570a54b420bcc71f8076047556f5fef4854151521afc48f5a5804c63667f3bcd`  
		Last Modified: Thu, 11 Dec 2025 22:39:08 GMT  
		Size: 59.3 MB (59283708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d39636b4c5cf89b058026b27bd9f169a86a534e95292a75c0db68bdbc1d09f`  
		Last Modified: Thu, 11 Dec 2025 22:39:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3560a4dcc4fe63f98655246eb8913115cd720244ab2fa0e860703792d983175c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e043f90dfb8899a9f014dc76a8392d00db677a51e865aa8487c1d98bb0ed2f7`

```dockerfile
```

-	Layers:
	-	`sha256:65bec773f668382af8cd6fd6fdcea3177a38387ee5a021ff77d63665559b1358`  
		Last Modified: Fri, 12 Dec 2025 01:35:33 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95125949de28d2431ef5976ae99931437ddea535a5c4c1bfc11edf98ab006723`  
		Last Modified: Fri, 12 Dec 2025 01:35:34 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
