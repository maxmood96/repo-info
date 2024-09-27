## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:da616f946311ef0d5009f0d0f544c9d581e234b4f79f1f76ca5ab1cd0151afb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c823a501ca91970a2a6d8c80d50d00054f89c7f9a821c61ccf4f5668f81dcb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275650806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9e050dd97eb1c80c1995511014a9b88bce608484ced8b0a7a55f5a34f491a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f746c70ddbc22c192dee9e199dab0832d564a1a7a693a05f0c9664b2efeb79bc`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289a2a61c47536ce2673d119f450b07190c56b8ce62227cbd8b0f38d080c4d3`  
		Last Modified: Fri, 27 Sep 2024 06:01:30 GMT  
		Size: 80.9 MB (80928160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4167baa9f6f3e8f0481009140eab610a8f4e4926a7b6be9e38cc510a2b86b71`  
		Last Modified: Fri, 27 Sep 2024 06:01:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e74303bb74143ad913775f41baad46b65463ab819a407de4b3b8475c7435f1`  
		Last Modified: Fri, 27 Sep 2024 06:01:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dd220d33eb6b418975ae4a1622de47701016b665f7e24a1ddd2025411f219309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7171446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2658a6d9c008294649ff91a79a015fec04cfb5897efa8f49a1f2250cf9eb76d4`

```dockerfile
```

-	Layers:
	-	`sha256:b2a0599224a2ac0c27217e6324e2b422682733605199636c777e34b83a98247e`  
		Last Modified: Fri, 27 Sep 2024 06:01:28 GMT  
		Size: 7.2 MB (7156006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d1b4e0d8b0e0706f12280b87caea38d60ea54fb62c83c200cc19497e60fcb3`  
		Last Modified: Fri, 27 Sep 2024 06:01:27 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3bb333b7d7bc50f1f5d2edf6094ce44c555fe9296d04ca69710e2a0991d91071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274336165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7443317cf6eda9a1401be6a74526de7320a2c1b0bd84d7dac8ccca7fd7b38da7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7200d0857db89d07cbd5e5cb92b246c83e764f2907e18fd7164a637ac306e4`  
		Last Modified: Tue, 17 Sep 2024 04:30:16 GMT  
		Size: 144.0 MB (143959449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1827d445965700cf4dc8657fd4750f2e26f81b263c08e815c60cb0d19b3cce24`  
		Last Modified: Tue, 17 Sep 2024 04:36:41 GMT  
		Size: 80.8 MB (80790047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5170a9decf21bbc6754d9929b55ccf80c17390331ca139ce283522f1f46e5481`  
		Last Modified: Tue, 17 Sep 2024 04:36:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab4b5d43f90c1e376973fafb9521442c6f0c506d3893d520081df05c75735cd`  
		Last Modified: Tue, 17 Sep 2024 04:36:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2bb6bb7f905a6f2c390fff5cc00244e113b07a7d7bd4cf8b54781abfdddc6183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7029350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104969e5f3f7381c1ce680146d51a3cc599d92c0b294f74cb33bc6ac7bfcb6eb`

```dockerfile
```

-	Layers:
	-	`sha256:cd205d6efe83241fd5da7d23bfd10745e1a71fdd9bc9acf4366d46496391ff82`  
		Last Modified: Tue, 17 Sep 2024 04:36:38 GMT  
		Size: 7.0 MB (7013374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc0c9e36607c94f7f7cdfa349d15d7235e26b76354be020c6c70f2c80e63ca5`  
		Last Modified: Tue, 17 Sep 2024 04:36:37 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
