## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d5e0b44841b7f75dd20015f82aaaa522ef4e9da46b94ef64aea79e88c7d76556
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c6a52f5b83c96daec65a4da825ec233c891d3337c44def18521ee9d083f0a11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243713908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777dacf82d7f671c8d7306e0f8b348945390a224e327ca78e0ffc472d429fa45`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:02:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:57 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:03:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:03:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66be68264ca5d8a848f13ac7e616f9854156b11083f457fcdd397aca0d843f3a`  
		Last Modified: Thu, 05 Feb 2026 23:03:36 GMT  
		Size: 145.8 MB (145806880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df974489f8786c9153300edae85d49812732335f3b0383e5ddda06887dc39b11`  
		Last Modified: Thu, 05 Feb 2026 23:03:34 GMT  
		Size: 69.7 MB (69677894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab2171ef6e500de14bf93c331159d8f72e7ce22ecd3ea86c5373a8579ca8765`  
		Last Modified: Thu, 05 Feb 2026 23:03:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47e964a046125d68fd6dfd1ed1fd0e77de5e2af49a2513b8c6d53d41557f4353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a005f414a456680c2828b13f59083a9bf4f32d9c2999dd7d5c47e578cbd553a`

```dockerfile
```

-	Layers:
	-	`sha256:692f59f85a4c386a4f31aed3a666108c248ccfbf2f2dbe5b4bb1cc455c5c58b1`  
		Last Modified: Thu, 05 Feb 2026 23:03:32 GMT  
		Size: 5.1 MB (5134795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d216b01669823cb84c04f9c53246b8d0d4e1a367898a394ccd992f4ed960606`  
		Last Modified: Thu, 05 Feb 2026 23:03:31 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e821f317f2e12375f90f5157404d6eae0cf7ec188bb29c9d3fe8f6e85bd7ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240281963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81aa5d20cff0ee99da036e01f88ee89695ffdf931e6835a1157d8c839172dbae`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:03:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:03:49 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1314a189929ef3517dce02d806f4df5027c3480747d91899f7752f36509e271`  
		Last Modified: Thu, 05 Feb 2026 23:04:27 GMT  
		Size: 142.5 MB (142500849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc718cdc07cc14cb8d864d704732a3eb2af6b058c3c69faec6a3fec0e686581d`  
		Last Modified: Thu, 05 Feb 2026 23:04:25 GMT  
		Size: 69.7 MB (69672646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc92a92f9e51cf0e7b29459145cae62e9a3e094b8500b8d04b7d917a88759476`  
		Last Modified: Thu, 05 Feb 2026 23:04:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:737ddb04e4e97cedea78dc7fe5218307942fae29e7336e2dbe22f18c2f66b6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889709342aaca514782b0933ddb7866e4c906f112a39d6e0a50192b80d3d8d40`

```dockerfile
```

-	Layers:
	-	`sha256:453d0dd9a6de71ccff2f3cfcfa4a418e0abe6dc8780e688448257105bb066c7e`  
		Last Modified: Thu, 05 Feb 2026 23:04:23 GMT  
		Size: 5.1 MB (5141174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7cac358a55edde3f58491300d5e4190d6d2777e941b6caa4b7a5bea370c81ec`  
		Last Modified: Thu, 05 Feb 2026 23:04:22 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e33c8c747b70cc531f611981d48d0926eee628443d495ebeed406bc440c262e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240580194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c09b4601fa8d3989798eb2dd21768635ed61deb0438560b3095decf65e367d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:09:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:09:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:09:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:09:12 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:16:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:16:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:16:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607c79b3b3b1691eb3c0b474b5d2de20a327ef51c9164916b1b2a1abd13eb606`  
		Last Modified: Fri, 06 Feb 2026 00:10:51 GMT  
		Size: 133.0 MB (132996861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671839212a1ceb91e5a0e0cec79b7f5923f07fb1a38da2f5aba89a509c091b64`  
		Last Modified: Fri, 06 Feb 2026 00:17:07 GMT  
		Size: 75.5 MB (75513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87a8794d97879e47fbc4106d8e4d0ab23ab99be301db2c99848a46ee1f8d346`  
		Last Modified: Fri, 06 Feb 2026 00:17:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b0225e87511c13506a2f8ae7b5ad4e45c67919df145b2417e583a034a5430a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3df5656e86354d2cc17024460902b6da48879e15f1050b1b4adf1285c7046cb`

```dockerfile
```

-	Layers:
	-	`sha256:63bd02daa1beac8a88d3fe696f8e3439d426c877163db70ef434a7bd9968ce6c`  
		Last Modified: Fri, 06 Feb 2026 00:17:05 GMT  
		Size: 5.1 MB (5139338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba44f4ee4a0138433a4ece40eeedaab23cd1e89f35537ef57dae3a710fcb496`  
		Last Modified: Fri, 06 Feb 2026 00:17:05 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:84074f61317c40122d50f655b1fda20575c60d49448ec79a35ecfdf2925c0fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221937065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79b4b978c8f76f1e92aae8c6b120131921d94b4b08cc5dff8217455ba4128be`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 22:58:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:58:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:58:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:58:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 22:58:50 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:00:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:00:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:00:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181b24fc761df552e91d0d7f604b47fae5305a37ba74ddcb21468831ebbba7b9`  
		Last Modified: Thu, 05 Feb 2026 22:59:30 GMT  
		Size: 126.6 MB (126562187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9b3a63a30a65c7187dc425c83f6bb09456837e59eb4e7e32577e26cc0b7a81`  
		Last Modified: Thu, 05 Feb 2026 23:00:27 GMT  
		Size: 68.5 MB (68489851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef6688f84cc8b237fc479511cc741feceddf897a3eb3f54523ce4f6e3f13d3c`  
		Last Modified: Thu, 05 Feb 2026 23:00:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:253956fb7f92914b691e53d931c789aebf88335d90a6f21e5a214620a1aa6473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be250ed6b668c975f104876363cdec5b1a44e2af84305aed47f27de1092c587e`

```dockerfile
```

-	Layers:
	-	`sha256:2a4978f6e2e09fd1552bf2ce2d17dda4df3a07cb9f15eb0eb63beba8d1ed251a`  
		Last Modified: Thu, 05 Feb 2026 23:00:26 GMT  
		Size: 5.1 MB (5126120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3aecc701174cb39d6908f0cdbd93de8029b10b2e410ca475075298f8ebfe4c`  
		Last Modified: Thu, 05 Feb 2026 23:00:26 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json
