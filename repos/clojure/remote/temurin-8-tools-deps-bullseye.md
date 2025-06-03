## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:bfac9664dc0d070705ce92cdcd62868a4b1c90f8b434c901d223268b87bd2428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9c4b453d37053dace1a4452ac014a84deeecdec2f68b78b9a698f6336f605976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177876841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8a0f78af8e7aef4efbc5875676a31a2553826f6d233991f78e1cf6449d0040`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b300bb53a7798ad49001881ea4d6e47162b03ba3be625bd4f546eb76f7ee72`  
		Last Modified: Tue, 03 Jun 2025 18:23:43 GMT  
		Size: 54.7 MB (54716180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4a280a4f2435cf2a48fe5a19da953d9757601fa245180fc773e05d97533e60`  
		Last Modified: Tue, 03 Jun 2025 18:23:43 GMT  
		Size: 69.4 MB (69409823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20fa7b47deaed4bb4c01e61835282eadcd7132ce9bd7fbaf5664a9d1b72e4d5`  
		Last Modified: Tue, 03 Jun 2025 18:23:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:76c9363821e66bc9755cc277db6ca76917be641d4aa2003c61182f7296fe8cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7741a96a5fcfa3dc1b6d6d3a462dabbceea4abaaa64daf7d5b73af1f93fccec4`

```dockerfile
```

-	Layers:
	-	`sha256:c26669d9a50e412625d036feeb2d9ec6b4b322d116720496cb7e7654020acea4`  
		Last Modified: Tue, 03 Jun 2025 18:38:14 GMT  
		Size: 7.4 MB (7377796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448d63348251405ff0ee86bb3ad1011af69706038f560c755ee3f8550e83079c`  
		Last Modified: Tue, 03 Jun 2025 18:38:15 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1657a39010265efec41ffeb686ebeb7f0b3c3e58cce0b5cdccebd4f76805fc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175616672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3f3b00cefce59ca28a7ff9632c86644198d2ad0387326ef23053d77244a346`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5f701bfcb264810d9aa404e8040ce22b5b531c7f91508b60b5eea297f126c`  
		Last Modified: Tue, 03 Jun 2025 10:29:12 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0e5d77e8d4d1eec47d287fc77a30e9aa4d6365c1cd8fb77638ca60ae608957`  
		Last Modified: Tue, 03 Jun 2025 18:27:34 GMT  
		Size: 69.5 MB (69537757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc45bc743bf65499075a1e4e124f723752105656dd661a7eb471e0a0c7c1340`  
		Last Modified: Tue, 03 Jun 2025 18:27:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3f79fa3882c9f54a215d871f731faf5bfd5faee1dba460eb2cef131a8087a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d85ac37ba400ce72d757384efc71002f6b0e7e4ab6d88e9919ce64e8bfdfd9`

```dockerfile
```

-	Layers:
	-	`sha256:925b3aa50b6cd360721b8c24905347f181ab8bc1a00df2f78efc6f0c708ad208`  
		Last Modified: Tue, 03 Jun 2025 18:37:16 GMT  
		Size: 7.4 MB (7383593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f409c2f1bfa02e8ab73a8e75983e278c51b298e90c532ec3d2238fe242cea37`  
		Last Modified: Tue, 03 Jun 2025 18:37:17 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
