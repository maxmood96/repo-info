## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:c684e1eed56c9ba9a0a10be2867069f6b72ecf66cf833e6116705c1684742d28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:648664c268c56584c2c8328c5f40db7fe7120990b078652de8bcf0baf0aeaf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268875132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de161cea5be4ca0dbfc58a691a039d8bbf60b426ed89db7c70a15c1534d545b8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f2ce86b7d0323e9e60bb36e2d4871beb29324eeb47434162a712499632ea9e`  
		Last Modified: Tue, 19 Aug 2025 04:27:41 GMT  
		Size: 145.7 MB (145658172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d99c23d63a0237121d0fb18272a197b2d7d48a17e50cce5b180a58c5cbd904`  
		Last Modified: Mon, 18 Aug 2025 16:52:50 GMT  
		Size: 69.5 MB (69460973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c8fda4d1c37f650fecc2fad9843bbe792c2889219bcbda44f6e87ec0f29f9`  
		Last Modified: Mon, 18 Aug 2025 16:52:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2f2fdf6f46f39a2824c5e8a3a6e09dc75af401974bff7f49c0c83450a64f78e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37aba8d10f649fa64fd7b84bac606c7acd31361296e6e2427b1e34b2eb3a4c8`

```dockerfile
```

-	Layers:
	-	`sha256:fe8cfd81b15b6c22eccde8360878e75ab624dd7bf609e64a9170b2d861974110`  
		Last Modified: Mon, 18 Aug 2025 18:35:17 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f397752138680d2860967eddb211f33799224902b86db9421a7d6c31c842f20b`  
		Last Modified: Mon, 18 Aug 2025 18:35:18 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78d1b272a5a981197956e549b7e7e9e6fe9a36afa99a4e6950fe0a93e6d4a34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264297817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f2b1fecb7102090fbc6ffa5541768ba731899a6bd48250073077ca44070999`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61737f5a5e55be362f75457232f49e7bc4d9d42eb74342ca632255e8150a311`  
		Last Modified: Tue, 19 Aug 2025 04:11:00 GMT  
		Size: 142.5 MB (142460513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffaa120aabbfa4f937ae75ee7466dc59ff2db408eed35ccee7f193d5e3b6bef`  
		Last Modified: Tue, 19 Aug 2025 04:10:59 GMT  
		Size: 69.6 MB (69588249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7cf118b5583886311507d7ddb7291da3895d59ced800822e4d32ad69164001`  
		Last Modified: Mon, 18 Aug 2025 17:01:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6a41c41f422a81d4b907b0e4ed7e52a7e3d3dd8571450e81ce88c379b97f2fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe6f3cdb5609724ce118f3207070ba3705a69a09de54c566bba2e492a2b1d6d`

```dockerfile
```

-	Layers:
	-	`sha256:4c87f19ed581e6bc061879bde3bbccf7347c12bb9c6e9bab6a8713358431e736`  
		Last Modified: Mon, 18 Aug 2025 18:35:26 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:712ff7e26a092c3827b85210051108fab4b47941148e592f591fcd6b22bebbdd`  
		Last Modified: Mon, 18 Aug 2025 18:35:27 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
