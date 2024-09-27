## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:24cfab79c5091ffda1697ff26ee517be0d12343b6432733877ef7b3fdec6ff17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:31caf22aa5b5c16a927f96e67c814c6c96b70c3f3d94b80a2624beb3f1f94728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276033680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20963d89fb7e4b967e6ffb796dd7a87a1082e9d570fc6bf3a78c3e54a2a9048`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c58a0aeb5cd152f7aaa6d85e93a5786b4f213b3f0e1927df7ad086df9a5182`  
		Last Modified: Fri, 27 Sep 2024 06:01:12 GMT  
		Size: 145.6 MB (145550046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df15cf0be69021242f278367f1818d1211fd8fe5b2c975548bf7fbc24e08deb`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 80.9 MB (80927938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3decfa3daeb181d3d950c368b8ae5c17b81de0b5fe2ade1918fbdbed5e53ff3`  
		Last Modified: Fri, 27 Sep 2024 06:01:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:15287d2a02d97728ae3392e5170b734352d0fa38e4d13d01d4c66b543fd5c520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7190677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391f9d03b8e768c622b1fac9f7051c004402f60e3bfd43cc48ecea4ce203629`

```dockerfile
```

-	Layers:
	-	`sha256:9e68d2b9cf3afccfeb6a51e8abd6613aad3779b3c3e6b0231fb85929f4224b85`  
		Last Modified: Fri, 27 Sep 2024 06:01:12 GMT  
		Size: 7.2 MB (7176813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6381fea56a2678d645eccdb1bb6bf0e4f153753d44c2ce0e420a7f81f9ea0859`  
		Last Modified: Fri, 27 Sep 2024 06:01:12 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad1c6249a6339f6e4f1f3d5cfcb9ced6385430eff7ca56390b3356db4d1bfcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272731251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef19a93f537d7a45fc0e286d92c423e929477678eea95686abf165b2ae351`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3df7a0f576d2d0cf07728e3349cf460816062dde696437d39d2061a179a83b`  
		Last Modified: Tue, 17 Sep 2024 04:18:28 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875a6f1e310d9ccd79b78ceef8b0bc6d16a6497e1330a867eb9e4b82b5960819`  
		Last Modified: Tue, 17 Sep 2024 04:24:18 GMT  
		Size: 80.8 MB (80790166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1597d5fbdbde4e55710ef0faf9aac772c2222c50863580e825aa63c1de336e20`  
		Last Modified: Tue, 17 Sep 2024 04:24:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d68f06e411eeeb95579fa0abb4f46c3acf04e64800ecce59e24142f5ece42a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7027774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463df34ed22f9bae38fb224bd166022181b11b50515356ee0a5541178e5b5c3a`

```dockerfile
```

-	Layers:
	-	`sha256:e65d6e36112bfcdae71e0bc85bc9124ab4449800b7c895024157159475d297f0`  
		Last Modified: Tue, 17 Sep 2024 04:24:16 GMT  
		Size: 7.0 MB (7013374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55166c27319e7fd99d8370ed2c1ea5ca74ad66fee98f86056a88fefba1a9ed26`  
		Last Modified: Tue, 17 Sep 2024 04:24:16 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
