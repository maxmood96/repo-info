## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:dfe0050749794bff6b9214da64523fcddddf9ec370845067626c60008e80b31b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7fb491b767495e3299edfc54159792ee251c44c60b6b0d8beb4db39845390024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234095556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a0e6589947cb19583c21584c37753ff70da0f699220c11aef77e7334db6dd9`
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
	-	`sha256:cf791cc6ffb4b486af50652d206e51b1029b1fdc187080a16968f7868e981b44`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 103.6 MB (103611899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8172e149ec6b1da2c2214bf4becaa56a0f62422939e48e78db6df564e00dbff1`  
		Last Modified: Fri, 27 Sep 2024 06:01:13 GMT  
		Size: 80.9 MB (80927963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bc9be9b9e9e0288d29859044375ac040ae64d80e4ff508bda1bb32b8111342`  
		Last Modified: Fri, 27 Sep 2024 06:01:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9934c11c8f10772cffd44cd4b36141915ab82d33bfaa6abdf69bb4a4b64beb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7292664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0f740a6d0091a55a6277eb3592129077b76b17cadce4b0b04127a91681c110`

```dockerfile
```

-	Layers:
	-	`sha256:98d0428a86980b36231c2e0f890e6adf3b4103480113790ab650f35a9be85218`  
		Last Modified: Fri, 27 Sep 2024 06:01:11 GMT  
		Size: 7.3 MB (7278812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54073f61949fe6e77dad62ce0a9b4c93edcfb6a1a9c9819701901e3347582396`  
		Last Modified: Fri, 27 Sep 2024 06:01:11 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eec4a8c368e7ff3b9239cf80f1505fbbff1ced47465960885489d21a97f6f73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233105291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3bc542e175ea9cca71e9a78c9deefef6fa1d005fc3f7a5a68fdf786a50c258`
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
	-	`sha256:22506feca16d1399f16de0c102b0b2250234c9f2d1ddfb76fc7c96b7f82fb0d2`  
		Last Modified: Tue, 17 Sep 2024 04:07:49 GMT  
		Size: 102.7 MB (102729254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d595ffd0d9e524356e1953b0d7c59adcce257a561dc3ba29825f17fb2e4871a7`  
		Last Modified: Tue, 17 Sep 2024 04:13:22 GMT  
		Size: 80.8 MB (80789766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764603c660e4b90df6155863b64c2a4ebe6f3adca4f199e0b5ad172bd689b0c7`  
		Last Modified: Tue, 17 Sep 2024 04:13:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:67086288f3fad7afd042a30b2a858afd02272bf059ab127450c364c2031ed182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7053252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a27bdcc16fcdcee992db42638f6792ac472ca52d25e37f554b312d84941b92d`

```dockerfile
```

-	Layers:
	-	`sha256:e913b0eb6cd8827dde362b78c4aa62f3cfea9f87491539b106960ffad9be85c0`  
		Last Modified: Tue, 17 Sep 2024 04:13:20 GMT  
		Size: 7.0 MB (7038865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:753a3eb9a4eb5520050f6de2336be6d20c0fd570bed4e1373e42180843ae6150`  
		Last Modified: Tue, 17 Sep 2024 04:13:19 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
