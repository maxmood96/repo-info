## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:be3f245d0f7339463d0601c58701e16eaf0312b4390b12c7516c0c39124f8032
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7e2b76565cc2f30d96ee0fc941ac675a6b0277f744efee60c6e7cc3eeb45a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152456364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ba492bbfcb4baa5018e7443eedeedb1ce47c770297ef4c860f59a02838ac1`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b0b4b33300104851870ffe74371a4b52c88c757bbdac19854fe23822c1e88`  
		Last Modified: Wed, 29 Jan 2025 20:27:23 GMT  
		Size: 54.7 MB (54711727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b3cbce045f37c7389a2b8b412a169fdabd2aedb6e73fedfbe7c8658d332f6`  
		Last Modified: Wed, 29 Jan 2025 20:27:24 GMT  
		Size: 69.5 MB (69531574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37091518fcc9a975ebde13a0a14d422938a4910b8ed139b44b6db3d98109a694`  
		Last Modified: Wed, 29 Jan 2025 20:27:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aec3c059fbdf46d1372cedfbee63fc80fa1d10fb0f1488dd529f7062fb992452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215c0a7af9b00f7f0e111b51c42a2ef40d9727f4a72d59987744dadc8c3df276`

```dockerfile
```

-	Layers:
	-	`sha256:cdce5bc889a76fb4dbc84f9386f17d2dfbb09a2df8e1ab79048236875cbf3d39`  
		Last Modified: Wed, 29 Jan 2025 20:27:22 GMT  
		Size: 5.0 MB (5034177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c2d09a8567ff830782f3fbb260aa994089f871a5dd6297d948165e16250475`  
		Last Modified: Wed, 29 Jan 2025 20:27:22 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97e3c919c80ea75c339b63093b68409caa911e41b77de0034ae5733a80892572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151239707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5266b3f5b09c38809ed6e0f3578459963a1fc7934c91b97775378a3f4ecbc54`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ed982e50b4bdb3d1279aa12d665dff931239bde8ac859554117a355d2b785c`  
		Last Modified: Thu, 23 Jan 2025 02:25:58 GMT  
		Size: 53.8 MB (53816412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f295b10ef30d00ce9a4ed27b5516461fbc3460b1ab9afae4745cac34585cac`  
		Last Modified: Wed, 29 Jan 2025 20:38:34 GMT  
		Size: 69.4 MB (69381619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a518bc64f20506ec9aa0140c11495e0e77ff24aacb8f74dc8c1327b97bb0f8`  
		Last Modified: Wed, 29 Jan 2025 20:38:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1ebb8d0e8401bf5e8e0f4e6a90ce0ea2889c84d41f498cc8defeb25f680eb93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb5f52f408773eb4925e81aaca87968cc816b2e1606652ae7e3304d4333d6c1`

```dockerfile
```

-	Layers:
	-	`sha256:7376cffff6ed6f47e265029b2ea8b4f899a287c72036b070d4496c2d1e9e45e0`  
		Last Modified: Wed, 29 Jan 2025 20:38:32 GMT  
		Size: 5.0 MB (5040636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0b0cf7c30d9176b45bfe05640008cd5500cfb22384cfd5226ebeaf1e28bc3b`  
		Last Modified: Wed, 29 Jan 2025 20:38:32 GMT  
		Size: 14.4 KB (14408 bytes)  
		MIME: application/vnd.in-toto+json
