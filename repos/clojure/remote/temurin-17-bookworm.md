## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:9b1bfae1a6b5c80b2310c4fe78f045a8e1b6d861ad333ced28a701a62853b2e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3fa20443f0fc43cf0068811e39e0c28d9830a10030ff5f3aca6d6b429557c186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274335735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20076153b09daa8b0595cb9c0586f282488bd6c4109624bc34121f0bf987d348`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab36cdfd38f8929e26dd2e2b0952675c53c24e11c25f07811292073f0544e52e`  
		Last Modified: Fri, 27 Sep 2024 10:31:31 GMT  
		Size: 144.0 MB (143959468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1184941834d52a0c641e3bd42d400008dde109883c44c1d9eb1e4be2cd3a024`  
		Last Modified: Fri, 27 Sep 2024 10:36:02 GMT  
		Size: 80.8 MB (80790345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff08372fbfa92a6dd1e5bfbed669aa45d9530333def3eee869f29be1191a1d61`  
		Last Modified: Fri, 27 Sep 2024 10:36:00 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e025ccc22a511ed8df3a95fdd04afaadf64536b89cb74afeaa20959ac8cb7f`  
		Last Modified: Fri, 27 Sep 2024 10:36:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c12eee6b1f249b759f174ff9492ae2664ef7a0f2b8f9b4427b3ea3d2cbc1cbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7177750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9c9b5f3388415441945aae9fa3d9009370e2860955af4371800916c05afb35`

```dockerfile
```

-	Layers:
	-	`sha256:0b8f83833073e381610dfbe1e533c1587744490f817ce355947ca93e4219ad16`  
		Last Modified: Fri, 27 Sep 2024 10:36:00 GMT  
		Size: 7.2 MB (7161774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6e4e2cb35f9055b7cd56e4c52ab02506808eef33d6aa3826d8980821a74bd6`  
		Last Modified: Fri, 27 Sep 2024 10:36:00 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
