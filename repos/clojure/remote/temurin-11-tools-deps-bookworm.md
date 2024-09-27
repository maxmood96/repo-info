## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:fe9e55046b0d36734c57e22247f0d7ba0bcf1e92127b7369c4190b377de31fac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ed7d7201a48ab780a13bdcdb6a19fd77e6fa26c859c0c0c55a82f1fc0c80677f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272730624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8269bb4f1474eeee29f219d6d3d9751e0b1c46a8751bda16062d4e6446cc50ae`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
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
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d8eb94179008dca8e8b0b4cf8c92e0d9775ce3f4db5369ad871915cb8e3178`  
		Last Modified: Fri, 27 Sep 2024 10:23:17 GMT  
		Size: 142.4 MB (142354745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1caa23c87eca88b23af7cbac8baf3bf137c38da45b8a62f5814dd291d203270`  
		Last Modified: Fri, 27 Sep 2024 10:28:04 GMT  
		Size: 80.8 MB (80790349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18665d5e4576675039fa213c7791f814102ba5f4e3d541cee05255176f7b9d57`  
		Last Modified: Fri, 27 Sep 2024 10:28:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a62e455d326d674da4176042ac60279fdb7384fc574925fd23380dd4699b0c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056277e5f40883a0b856a3663a7a228e658f3208302b709d023d78321431b66c`

```dockerfile
```

-	Layers:
	-	`sha256:53dc6bcb52cb2163889530c3e1b58db5d69ba1d5ce15f591f28e9bcedcddef5e`  
		Last Modified: Fri, 27 Sep 2024 10:28:02 GMT  
		Size: 7.2 MB (7183200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a4062b7d309570ed5043c11f186a42c10b85d1ee8fbff0722e033243bac22a`  
		Last Modified: Fri, 27 Sep 2024 10:28:02 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
