## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:4ad870ce3cf70aaa6265bd771e057775867e552348dae39de7619ddac52d41e0
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

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
		Last Modified: Fri, 14 Nov 2025 00:53:26 GMT  
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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78a967c1bd6ebb76a968fbd70a428d0634feba8f0f4115f72b969184fdd40442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273071610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc28f23c2dae3a763bbc5c80e419fe5e25d3566f5dc920f07eaf9464a68eb396`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:42:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02779de92cbe40f2440c934503688b46946311c4ce317a946f5c5d4caa912112`  
		Last Modified: Sun, 09 Nov 2025 00:37:46 GMT  
		Size: 143.7 MB (143680053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807c5c469af39c2ee9f4d6e172ad346430e29b8199ef5fb5a14108577bac164`  
		Last Modified: Sat, 08 Nov 2025 18:43:46 GMT  
		Size: 81.0 MB (81031036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85585b35d915eefe49f0947ce9d9cce13ed4fe305de08cdb0e816f63b6125bf`  
		Last Modified: Sat, 08 Nov 2025 18:43:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2efdf678cd7734f43f15c7556ad0fc554964f5b626ac75c30c78f0efdb6b8`  
		Last Modified: Sat, 08 Nov 2025 18:43:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b095ac87804fc043d76dde5dfb4ee9cfe31ddd04a1bfa6fd692cfe988087ba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16905c494c92dd02ad1559e611bb6642ba7f4d13226dc0d5f671e9af2862443c`

```dockerfile
```

-	Layers:
	-	`sha256:5b946ec71a99474c84fd33bef0f4e53173833a5c0dacedce8a724d9df2501a84`  
		Last Modified: Sat, 08 Nov 2025 22:41:06 GMT  
		Size: 7.4 MB (7380655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf294dd512766e3a8bad2e88c77496cd214b08bb3a3f191a9789bf742247b67`  
		Last Modified: Sat, 08 Nov 2025 22:41:06 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:964f6887d642cf3aa390292de0e39b47a5a5616cbd5998049d8404851121c8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283839481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f88884e39a16eea0bb0d17510de6adc831deb86cbc50e822551f5493643bf1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:13:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:13:32 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:22:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:22:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:22:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:22:02 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:22:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b991744392cdb392b2eb2934ca9a948480035c261ce99f62fad6bd622bfcaaf0`  
		Last Modified: Sat, 08 Nov 2025 21:14:39 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d38c6f617e0c6c8d09cdde56fce237a7770d47e8c84745692bdcaaa3ca7fb38`  
		Last Modified: Sat, 08 Nov 2025 21:22:55 GMT  
		Size: 87.0 MB (86986024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11b7fde61805b5a0f91d90569c4ff1d2941fb9a48e95c756e5795d7857a6e36`  
		Last Modified: Sat, 08 Nov 2025 21:22:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a0bf506f738194304e84a4124d9e125f1f7ee59f251e94193f46511112764f`  
		Last Modified: Sat, 08 Nov 2025 21:22:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:769b5ed7bd4d11b143fc7854b5405ba98ffcdfed3a377c3fab63e6eaf04a234b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee6d44425207466815a8ae7a7e63e6ffeb93b7b8ba025d8814837f4c6017110`

```dockerfile
```

-	Layers:
	-	`sha256:f6a67c71ef950509a41a1ec29761162ff442cf32b5d0a0d2b39c1d2ad1818505`  
		Last Modified: Sat, 08 Nov 2025 22:41:12 GMT  
		Size: 7.4 MB (7380106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795b2011fcf39d6268643521d6721af27beb0d57ded8bbbf4ba0a78191849d36`  
		Last Modified: Sat, 08 Nov 2025 22:41:13 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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
