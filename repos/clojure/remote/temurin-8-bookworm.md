## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:fd965a7757c6ec7f37fef09c2fab9de5f76c5a3cb83708ea5cc52e065308dc88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1656686516aa8f6f77eb19b6727642796970b7994c78f9785334bfd7dde4089f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233475948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3201dff2da2cd86b294666ec873ed77e92f11aafa3c1ec049324efcb69e4ce5c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f28176026b7610ed955787195c16f28a97a6e54b94da8ea7264f6d643d8806`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 103.6 MB (103600229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ccb12b625db845f19d334b6e82045e6305f0f088068da7ef0176f2056c8f5b`  
		Last Modified: Wed, 05 Jun 2024 06:10:03 GMT  
		Size: 80.3 MB (80298681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1d4b488c65ecb0af4424366bdd521fda04d0ef1b57f898e4f8afcc05cee98`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ce5e7594bb3187ca595e5edaacaec8453570d69b47fb8d8b5de4251e5f98ea0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103ec60b33019f4669a67a45b329c22c6e0d231d6c376f123e50752c0ccf7184`

```dockerfile
```

-	Layers:
	-	`sha256:491dd50f52d001717f20225146fe67bc17495d176e126afc3ed3173bcd43db04`  
		Last Modified: Wed, 05 Jun 2024 06:10:02 GMT  
		Size: 7.0 MB (6983154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927010bd102c7c7cb8b769d2623ba708a14fdbf41c24f428043357ca1a4ea399`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80673afb6f294dae96c2bbb8591d48f57697c7e6a6d84859cab10a619469e5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232359282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca9a0d975f0f7d00833403cf38d2817c2cdca0ce66baaaa287bf8c228eb1069`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6e9ecbdc3ddf118977ce6146d477e95e017b027a376970e58b440ff008a5b9`  
		Last Modified: Thu, 13 Jun 2024 11:09:40 GMT  
		Size: 102.7 MB (102700388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d57c15b94be762ea9595f29ef21f8e920090b15b7c45195d49e434bd400f06c`  
		Last Modified: Thu, 13 Jun 2024 11:23:59 GMT  
		Size: 80.0 MB (80044843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c136e552c3c401165b050089010f937b995a05368d5ef1a03cb827f2b358ec0a`  
		Last Modified: Thu, 13 Jun 2024 11:23:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37c8b9c93257debfb3f0816bd1956671b50f2a9c4ccff1224a0884963cd19802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729c576e6018b3de1894c6df8280c38bc99df32b36e3b9432fd6b6e23c6c392f`

```dockerfile
```

-	Layers:
	-	`sha256:620e5b8f911c7df9b9bde6dca6eba5f9d4e486f2bd50b64ce02d012a2717dbcb`  
		Last Modified: Thu, 13 Jun 2024 11:23:58 GMT  
		Size: 7.0 MB (6989541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a47a9042c1cf709e6b9acceeebd31c42ca51a769f339d57412f7eb66c9719c4`  
		Last Modified: Thu, 13 Jun 2024 11:23:57 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
