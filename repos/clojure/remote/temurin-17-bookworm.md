## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:d3c686eace2706a7917d9d718768b0283ccf253024368c42a90e6c43f82a8153
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:952f2f6f05af13f757a95d029f595d9aae9d3488807c866fa346131acab614f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274476100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a029f3c0bff882817cff876e2588bd19704a0308468f183067862f4337b8b7fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:52:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:52:54 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec673831a72559be1cd0fe46da8925268bbcf6231edde409c156b2e5bd92b8b`  
		Last Modified: Fri, 14 Nov 2025 03:33:46 GMT  
		Size: 144.8 MB (144847978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad4057d53ad8425cd829eb80ce6989922c6e7ebc484fcc99dc7fa1b1cc61493`  
		Last Modified: Fri, 14 Nov 2025 00:53:45 GMT  
		Size: 81.1 MB (81146024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37889a50d7dd9d2d8619064f9c62700dd63b51ceb280f6695d89c36812be7b6`  
		Last Modified: Fri, 14 Nov 2025 00:53:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f24b51067260dcbabc42f0f066b504dec66b270db97dbe506e7c126faaab736`  
		Last Modified: Fri, 14 Nov 2025 00:53:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:efef910d92d889190b68f24d1b0952ae74bf1289c5d1564bd85adf06b5bae553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac258bf568d5f3be6eeebccbfb45e481a98674fec68de7e4801593645f21177`

```dockerfile
```

-	Layers:
	-	`sha256:1b8747ad9970e240770d457246dcd6d24eaaddd76a163d92dd6f8f900e518c77`  
		Last Modified: Fri, 14 Nov 2025 01:38:43 GMT  
		Size: 7.4 MB (7374892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee5c128523741581902ac3d79fa06b09021c7a0df470471336db5e8d78f1188`  
		Last Modified: Fri, 14 Nov 2025 01:38:44 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf18417c781c7a16aa0460c9eb58e90232c705b2845706e0d818e543c940b547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273071357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694c29d35820fe77201000ad2fd69549d49ef55b7b572af68f2783946a2e143b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e195eb9037696e35b762178279590e9ef0ce585a82b8e9ba9b644b507e0e624`  
		Last Modified: Fri, 14 Nov 2025 11:07:21 GMT  
		Size: 143.7 MB (143679914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e037d726f64f571c3fb08b27d28a6dfe1d3c02f5ef43047685f2885d089abcc9`  
		Last Modified: Fri, 14 Nov 2025 00:55:58 GMT  
		Size: 81.0 MB (81030921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eadcd2308b2f0c5935e86fcc12443483ce37840f99340aa04267560ea67d216`  
		Last Modified: Fri, 14 Nov 2025 00:55:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0bce7f1e247ba611ff96e379c7ec206fee4fad9cd9084afde676060622550`  
		Last Modified: Fri, 14 Nov 2025 00:55:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f31bddc617aebc045113e090a64bdf1e72886f1a460b3d8505d018e9829a2998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d4034863c1db4a54cd8b5233b4c26928345adec67cf73f23d931ae42b0060a`

```dockerfile
```

-	Layers:
	-	`sha256:1c068b8f9aa3fa62a861ae55af79882226580ebda345b3862440974916a26847`  
		Last Modified: Fri, 14 Nov 2025 04:38:02 GMT  
		Size: 7.4 MB (7380655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:132a5f20dccb75306aff0d9b0d0f069052f489333a8ac60faf91521cf4779723`  
		Last Modified: Fri, 14 Nov 2025 04:38:03 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8883700b920225b2e3ddfb5e968a1f10f6f21bb0d08e92f651e02b9e9a9a0a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283839725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e640901313c5928bd593a1f27a12df198c2b5b1d49c20b721587742463a3b5bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 06:59:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:59:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:59:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:59:12 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 06:59:12 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:08:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:08:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:08:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:08:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:08:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03721825e92ed5d3670f8aaad934e33c62dc316ab4d6db4103a5f455b6275fca`  
		Last Modified: Fri, 14 Nov 2025 07:00:25 GMT  
		Size: 144.5 MB (144525224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a86a45f3d5a014f12f1c26293e290eb6064a9ea375c803acdfafcdf39700ad7`  
		Last Modified: Fri, 14 Nov 2025 07:09:31 GMT  
		Size: 87.0 MB (86986176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2812767d077489bf5bd2cc05d945619fca07e7981bf0a784bdf5aa8971a699`  
		Last Modified: Fri, 14 Nov 2025 07:09:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4573f4e14551639aaa2c432cbbec0334d157a962bd632d0cf881e32cad20f7ad`  
		Last Modified: Fri, 14 Nov 2025 07:09:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b293d43dd2cab059b7d2e031fc3e73230eb4217009e944ee189c82ccfb92c712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f35e50933ce679d85e824c6c72c1428477b7efb3baa44977e7c372f2c59ffef`

```dockerfile
```

-	Layers:
	-	`sha256:6e7d04db3c1cb1f3970bc5baeab46decd13fbba4c9d5f20d4a23eef793955eb5`  
		Last Modified: Fri, 14 Nov 2025 10:35:46 GMT  
		Size: 7.4 MB (7380106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6675228e1e6f736ca66accf59996ba5d7ade92bf8f9befe2178a1538313997f9`  
		Last Modified: Fri, 14 Nov 2025 10:35:46 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a198495dd1631d1a77c91cc4ffe421c43803e82b3018a4fd318eb0b3874595b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261954781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3110c2ee371c63966043135da3591dc5b3bf2de8b3332ce48563064415e3fe77`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:00 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9faef0ec95b30e3730f96a131ace05d8a92e63ac3db86dfbb78893f35b3e87e`  
		Last Modified: Fri, 14 Nov 2025 00:55:36 GMT  
		Size: 134.9 MB (134859061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab3f440e65207662d8398572ea01ab8c218e9ab7ed70802d0a103d4b26867d2`  
		Last Modified: Fri, 14 Nov 2025 00:57:44 GMT  
		Size: 80.0 MB (79956585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc5dd52a1956a9f747c4e4f8eb20bb01cf1bee1a708dac362a06c32bfded017`  
		Last Modified: Fri, 14 Nov 2025 00:57:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b209d4ee997f21ed44678466d6dd70befcfad12d3b3369fd661e0270d18f4e`  
		Last Modified: Fri, 14 Nov 2025 00:57:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a26da3601d2453469d88f4df7dd44258260ef52dee3875aebc413ab6b9976533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585722c01ac10eb120f2835b1faea29a21679fcdbafb44f6c4b22ad392450e1f`

```dockerfile
```

-	Layers:
	-	`sha256:398a9c6ddcbab4b56ebc6fe9fcc136a13762682e49efe05ce867d379a5175174`  
		Last Modified: Fri, 14 Nov 2025 01:39:00 GMT  
		Size: 7.4 MB (7366211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e25f2e1c1304306a49b402020ea2c3783b6dc83049dae152c035137fe41f12`  
		Last Modified: Fri, 14 Nov 2025 01:39:01 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
