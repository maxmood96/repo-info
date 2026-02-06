## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b4d490cd7f31ac9c5ed89e768c87c6cd9f0280ed4f5c0d74f08b25dc8f1afb49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1b89c80f3523e2bc43da7c2d80c98f3506da0e883476c6a4a4af0f1d4d86b15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153077585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3bc75d5bb9d9729052a6acd77a3d3c8343591ca8a3ba385dd692969d2736c26`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:01:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:16 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:01:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:01:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9fcc0093592aac9aa46ed9c7c776557e6612d683e6475faa9d7b2f27d8bd3`  
		Last Modified: Thu, 05 Feb 2026 23:01:48 GMT  
		Size: 55.2 MB (55170168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee56b5f3caed7f490fe60eb94bff96452ceb038150a0b7d202813b7eb6d5672c`  
		Last Modified: Thu, 05 Feb 2026 23:01:48 GMT  
		Size: 69.7 MB (69678285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffe960e621ca1f934907d7f51cd243774daaa049a4208a092944f84c6d2668f`  
		Last Modified: Thu, 05 Feb 2026 23:01:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:310148c171dfb0c480a72f7413b6c6cf8cc4e9cc0b2509704ab93d9aa3200b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9de4216cd041c75a3ac541336a9f4cb580d37d42c85e0d88e24618f529256f6`

```dockerfile
```

-	Layers:
	-	`sha256:f99d4d5a8de41e5fa68e46d5d08dc9dd35c5bf57ed6d84bdbd387cb36715eb69`  
		Last Modified: Thu, 05 Feb 2026 23:01:46 GMT  
		Size: 5.2 MB (5235641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009db3f766b5000cad2d6e71192a97f7d50013c222c5e0a473b732d8f91d6ce4`  
		Last Modified: Thu, 05 Feb 2026 23:01:45 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc1b320a4ae889bbd03154787239421fc44a7313ea1af2441b122c05fa2f6fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152032727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9feacfd9ae4d9f1ae7901352f1c44169201e6a9f7c6e891bf925512394be8e3b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:01:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:21 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:02:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:02:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:02:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bde5efcb33d27d06e84e3f23cc59a1f3fbc32b08ab1888d46dc1293f22731ad`  
		Last Modified: Thu, 05 Feb 2026 23:01:51 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f884d9f59fd4d4b6c18140e46db21e02371079bc5ab1d5f60bb59efd24befaa0`  
		Last Modified: Thu, 05 Feb 2026 23:02:41 GMT  
		Size: 69.7 MB (69672628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f344bae861c63fb2fdc4aa36e979df890882ef724450fde3c776c28ffdf27e`  
		Last Modified: Thu, 05 Feb 2026 23:02:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:999f36e89f4c3856d17acaf8bea2da88bc41dbf2b1dcf819cc7b8227cd0e3454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659b63ec1f5405ccf56adc4ef023d0d3f9ce2e2aba68d4f9716e684bc6d206c5`

```dockerfile
```

-	Layers:
	-	`sha256:eb279e7d234843a73df3ebcc174d81fb14eeddd217095f717cde0cbac7a1f9c5`  
		Last Modified: Thu, 05 Feb 2026 23:02:39 GMT  
		Size: 5.2 MB (5242102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ee86db2f08c35f039434612d0a9498e05bb07f77b97312a5af1d7134aaa354`  
		Last Modified: Thu, 05 Feb 2026 23:02:39 GMT  
		Size: 13.6 KB (13565 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2a6289b2828a7520a9bf6c485235fb27562b2d3165449ef82a9371fe93630f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160233858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720f71bb14575c2b07a6f244cb34a91308fcd07c959ba918dcd240847b44a1b9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:57:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:57:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:57:26 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:03:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:03:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:03:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fdf83ffd1238f33e1fa3f93bce20dfbfd9ae745a5f61042a0bc95827efbd6d`  
		Last Modified: Thu, 05 Feb 2026 23:59:00 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a3dc37174143c3e49846ed024e124c88f9671c47fd5d699f75ca97b876fc4c`  
		Last Modified: Fri, 06 Feb 2026 00:04:36 GMT  
		Size: 75.5 MB (75514106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373f1f68513648509379b8064b9669cd2c188bdfd8d4157a589dd8ba8ff5d800`  
		Last Modified: Fri, 06 Feb 2026 00:04:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72e9ff8d1390b22f029d2ce2de0cc272a103049cf9df383524f61db07fd8c6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23cb8417544cce2ea3b17592ab355cabe0ab5937e95f90e102ea51980ca0c52`

```dockerfile
```

-	Layers:
	-	`sha256:9adb58dd3edfa54976be8253c25b53230fdc6a9d9d10041c2782566e934f2e60`  
		Last Modified: Fri, 06 Feb 2026 00:04:34 GMT  
		Size: 5.2 MB (5241394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0716f85215c2867097dd0185cdf3cd29b72cd0a66dacfd6293d6c55c978ce88a`  
		Last Modified: Fri, 06 Feb 2026 00:04:34 GMT  
		Size: 14.3 KB (14293 bytes)  
		MIME: application/vnd.in-toto+json
