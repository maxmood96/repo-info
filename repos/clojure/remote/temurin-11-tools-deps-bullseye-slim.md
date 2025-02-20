## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:04b7587668c868fae52aa0f1380899a9573de4ec88551f9d63bc3b4b7c2f5785
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c5fcbfa4bc333c77faa930ec02e64f130004f242f50d8489094b4b93c249583d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234640463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187c74bf17e78a8055a6a3a26358730c7831ab4962d21d67658c79efe52caca7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9c3a064b3c253962d07acbce516b0664abf34d7b734b00c71d5bf86edda84c`  
		Last Modified: Thu, 20 Feb 2025 04:11:01 GMT  
		Size: 145.6 MB (145598915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f9e36ae0016a4d854fce74a3b40cd83b521d3fe51be958f1b7179ceb65b813`  
		Last Modified: Thu, 20 Feb 2025 04:11:31 GMT  
		Size: 58.8 MB (58788316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4127cb80393bc9b34b5cb0d29986ec5022af1546095698dfd6da4e89249f0c2d`  
		Last Modified: Thu, 20 Feb 2025 04:11:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b55ef8812dcf6280e3f0ccd0b0306d7559868948f7df9b30b23f89d885cac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10ddaf6685b406f56206bdf5b3d22b0f688c002e443e68ad41c2fcb149ec3d5`

```dockerfile
```

-	Layers:
	-	`sha256:d1ea58ada841d820a45ffaeaca73194354efe9798d3cee96d0d4fff9ae840f71`  
		Last Modified: Thu, 20 Feb 2025 07:34:26 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e441d7e7c2de64bed281bfeb738b48ca425e040cad17c4556dce8fd4ca148f3`  
		Last Modified: Thu, 20 Feb 2025 07:34:27 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2654f1552de1717389812f2bc7e3f6976edb3a9ac90099f07607bbb1f5702aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230040161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91af6cd2b7d9a1e40aaee99e56a301a43cbc7c48b04000b6c00e2ffb6e55d6a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d675225baaf53e26e9c42dcbe4bf812ba2ecef1c2c7500ee0fa37ceace522`  
		Last Modified: Wed, 05 Feb 2025 05:45:54 GMT  
		Size: 142.4 MB (142385434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9549265c738b02dcefad898ed08eef1b4d13fc3bf8cb2f3b8d564e8a732f6c`  
		Last Modified: Thu, 20 Feb 2025 03:48:47 GMT  
		Size: 58.9 MB (58909274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5991b8b8e6593ca907fbe141c9cc502ed8aea8b395818f6ff1a2a7a208bef1`  
		Last Modified: Thu, 20 Feb 2025 03:48:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2f4b7e5640b6b70dd535b40b7193cac75d04063fb7db2e676acb9efd0347c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a8145543ed71767e2fb74327d73883b66b5af7bed02317d11c643726268332`

```dockerfile
```

-	Layers:
	-	`sha256:a071500b65ff77787540c674e71a53181b166bc4e90044a6fd9385bae7167203`  
		Last Modified: Thu, 20 Feb 2025 04:34:53 GMT  
		Size: 5.1 MB (5143558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816460810f157681f43fcc03e479a6459b431b87487f326fafa94c24f17b077e`  
		Last Modified: Thu, 20 Feb 2025 04:34:53 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
