## `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim`

```console
$ docker pull clojure@sha256:06459185c33743da64db71f08c5ce43190bcaa8c5e381ccc03a5c63fd9e82bf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:91dd4650a8fb9699c00b21972b0e824db7cc5f1a90861a55e3671240c8d15443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250056865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2736cc9f26c098a33247d93427c6b5b73f0eb414afdefa31fcb4620d2d9a910e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28420c33f9ab500c969026ff796e8be979d6780a674398d043716c00e1ed424c`  
		Last Modified: Thu, 05 Jun 2025 02:46:10 GMT  
		Size: 145.6 MB (145635638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f9aa676d7ce930fa56be6490de2f79ae3fe436349c18053d683358ca688d5c`  
		Last Modified: Tue, 03 Jun 2025 18:24:36 GMT  
		Size: 74.7 MB (74665200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9748439c40432facd472f749916095a27b3c47e71a8456ea6285eb347323089c`  
		Last Modified: Tue, 03 Jun 2025 18:24:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:118d14ec23e1c47d5b32b8be8bf0f6e619175e0e740e112be645f17fd8ee939a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5607fedb1485a101e843e961a2757f296b9310b79409682b4f6587f5442d12bb`

```dockerfile
```

-	Layers:
	-	`sha256:787c8961fe59cbb24643a540e3ab3d9d6cbe7c3f820ff6a3842fefbdbb2a5b6f`  
		Last Modified: Tue, 03 Jun 2025 21:36:43 GMT  
		Size: 5.1 MB (5132206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0333826606b9de18afb2b40a78e4ac8c68e1760971f3813af7574da405da99bd`  
		Last Modified: Tue, 03 Jun 2025 21:36:44 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e07758da81a5d2a48bb228658f120b21ab9530131ee1ebf96cbced819a4bc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247508348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33babe11788e666159ce946fd1f300557fa4b90c333ed48f1192f568a0270b87`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bffa601d4109bfae01c726b3c589fd4f5f2a729cf77bf75617f68d7e04065b`  
		Last Modified: Fri, 06 Jun 2025 13:07:25 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190de332d7a1944b6f3f36075d80c64087c10d20d1bde72da3937ddf35b925ee`  
		Last Modified: Tue, 03 Jun 2025 18:38:03 GMT  
		Size: 75.0 MB (74967583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c3d23bebbd7f3f9e74f0442c07a334b47faacd6f905124fce8839cb3ec937b`  
		Last Modified: Tue, 03 Jun 2025 18:37:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32db827b7054c31a39ff4d86f592a66a546cdcef4d7579e5f2891629a4f1f3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05897bd2735512f5924ed238678ce12e97ace96bcdd681f73780ae4f92bb73c`

```dockerfile
```

-	Layers:
	-	`sha256:7948f96b2e06918ad44a912875ac645c343cbe05edfd7391c60ab2e355bf3e6f`  
		Last Modified: Tue, 03 Jun 2025 21:36:49 GMT  
		Size: 5.1 MB (5138593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ceaf6bfeb7a65be151d1ea6c3846084014d8073c3aa1c8ecef09a2ab6a8629a`  
		Last Modified: Tue, 03 Jun 2025 21:36:51 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:56b442f9005edc4c1af92e51fec417f1f2c9cc1b0e4dfdb3d10cd82e701317ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246793677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2317cfc35b3056fac77074345ddade7e478b934ed4a1a936a137e4ec011b852b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c18682abc822fc2db69cf01e2aaa0cd74ec88d2153d1db29a25210375b8100`  
		Last Modified: Tue, 03 Jun 2025 08:33:50 GMT  
		Size: 132.8 MB (132810533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ceb1e71824cff87fd78fc3c2d45244fd3e2a9f4730738515a01996e5e9fc5`  
		Last Modified: Tue, 03 Jun 2025 18:47:55 GMT  
		Size: 80.4 MB (80401934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c395a4038865914645964615566eebfc857affb5545fc59caa65d586e48b8ff8`  
		Last Modified: Tue, 03 Jun 2025 18:47:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:55733e47b06519a6ad5944f41b50ffee704fad8de99e5df0224a7c23667fbf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d39643377b426ec7087e9e287673ff31dc377d349b041921c7412ec4fe37e5a`

```dockerfile
```

-	Layers:
	-	`sha256:c8d59bd0304052f4e6fcb328ef8203a886e15032aa25f45fa4ef5e45e7eeed3b`  
		Last Modified: Tue, 03 Jun 2025 21:36:56 GMT  
		Size: 5.1 MB (5135962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3745216191558200d73cdc59a11a8c59de050e610fa23cd536a12595ad97bf`  
		Last Modified: Tue, 03 Jun 2025 21:36:56 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:256e0bbbc70b6a652bad1c9d7c6ae0b6d9dd561593b5df9f2055fdefc27df601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230821802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d0194d8061d6b75917c558501997feb26c8661b9b0bd1660a41ccc1c567160`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6e2d8c49d3bdaa5b7240371085b6676318ff2eba1026dddbb17010c7fad79f`  
		Last Modified: Tue, 03 Jun 2025 06:05:26 GMT  
		Size: 125.6 MB (125585353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeae239ad7a669d8440b9e8967f51803a4bf07b23574ff8af5752e4c694eca0`  
		Last Modified: Tue, 03 Jun 2025 18:30:51 GMT  
		Size: 75.4 MB (75406185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85d582dd580f358bcae48faad8af28ee1f7664433f8f584ae0070ce5f35ebf`  
		Last Modified: Tue, 03 Jun 2025 18:30:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f43a6d671fbdd794df823800f5d5b3d8de38facd257787f4465158725b0705c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5a5cb74194bc31de1163491427f45ea11aba5737db95ce4ee86986327bc84d`

```dockerfile
```

-	Layers:
	-	`sha256:08af8a66f522f08cc4cb4e36cde7b738d6ecbab86131d3e213a4494a3fd87197`  
		Last Modified: Tue, 03 Jun 2025 21:37:01 GMT  
		Size: 5.1 MB (5128134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33428f45dc63ae41ade40621059daab4d9aa5f5b375fc9fca03df1973f4441a`  
		Last Modified: Tue, 03 Jun 2025 21:37:02 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
