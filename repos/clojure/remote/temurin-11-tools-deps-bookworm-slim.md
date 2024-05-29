## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:3eb1c38438d3d59742f5a8e68391cf2568ab49d0bc8033fce80d40354ea8712e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4412dcb68aaef6f2b67579f6301a53d49640b8def4575999b6a5b9bea5d7e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243524074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45b7fbb014391f23abb74a871903ae33f5fe6642aea6873880ca8a054ff22ba`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfecf24d02923304d7eed435a58df7f5b32412879eea0d20fcd5400dd4e0309a`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 145.5 MB (145504843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dc56babe90b7b60df2674c061b01ca0210db1f4af9a1d012ffa1479634df8d`  
		Last Modified: Wed, 29 May 2024 19:56:59 GMT  
		Size: 68.9 MB (68868175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948cb0887dfc70dbd1873f1e149c5cd4aed62692bfd4a09f09a8a861a550830f`  
		Last Modified: Wed, 29 May 2024 19:56:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9fd30125a306a63de0e70cbbcc69d9e8b596caeda36ea8a9bb483221fd1a307a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1175c84083a2ae4cd9017909be91ad0c59b3df35395e2e719c7ddb45ea469c5`

```dockerfile
```

-	Layers:
	-	`sha256:597d8cdf63858deb7148009909261878a6e3da961a828d30c77537b2ff06ef47`  
		Last Modified: Wed, 29 May 2024 19:56:59 GMT  
		Size: 4.7 MB (4704939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6258864772ddb0cf22f0d078b4a7edfe1c82afef95aa4cb38c276ec5774eb5`  
		Last Modified: Wed, 29 May 2024 19:56:58 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bfce42e06fbcc96cb7d8fad4f1a544a58ccb13b908b62945f3f8b55e80ecd43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240302706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78f2f9cf166ea7a906261b2c39c8e49adaaa2b7001b5b8f593582197a9aec50`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:50:48 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Tue, 28 May 2024 19:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:52:58 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:52:58 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:53:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:53:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:53:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c60673a7880f3ab3c9e739e642c4cd253b6e5561260ec565111b879f04e33c`  
		Last Modified: Tue, 28 May 2024 20:11:28 GMT  
		Size: 142.3 MB (142304343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c783fbcb36630cfc85d7acb17c9750246f094b0312053c05ae5db70175cf5f74`  
		Last Modified: Tue, 28 May 2024 20:13:02 GMT  
		Size: 68.8 MB (68818243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b3127aaf09b9c3007d33b078ab8b63b5f963397bb0ecd5a2d7db0fcebacc2d`  
		Last Modified: Tue, 28 May 2024 20:12:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
