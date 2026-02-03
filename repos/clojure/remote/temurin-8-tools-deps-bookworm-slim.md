## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:bb46090fcc86feb6fb092f535b5ece32836d997f5808514a398f9666d634a122
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
$ docker pull clojure@sha256:338a64b57eb51217cbbcd7e20be7ba38d0c2e2462db846f37aeb0712efd34bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152640429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40736399a22f1b4ea998f8c4ebeee14c507a7f246924e92167d073a1d96550a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:18:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:18:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:18:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:18:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:18:24 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:18:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:18:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bc60d68863fcb1134976b565154fbeec83e6b182ca53e9e9a87d0d6ca422fb`  
		Last Modified: Tue, 03 Feb 2026 03:18:58 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83b7c4e6f15ecaf00635037572252439d794ee7b45485b59d002dc0b2fc3e01`  
		Last Modified: Tue, 03 Feb 2026 03:18:59 GMT  
		Size: 69.7 MB (69677924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ce227557b16dc79c20a485921a3a2450f78100edef17afa388adf58ffd1701`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df92a140454c6e45bb5abe4572db04cc1424c20ac3a2bb7f4ac55a66de5315a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac9bbba8d5898d30c7fbb9dea0a9f07d5edc4260ae8739b03cd764b6067a4e0`

```dockerfile
```

-	Layers:
	-	`sha256:f04d83cf2fe7c2489680009ecdbc35d067de1d11c4005fd5f9e4476859497834`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 5.2 MB (5235010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6620cb48972994e3e9d88cbb4ace934754210d966ca9b188cfd8a2cb6182dc6c`  
		Last Modified: Tue, 03 Feb 2026 03:18:56 GMT  
		Size: 14.2 KB (14246 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f5678fc76b4d720e8ee148d1e3c6a8a43fca796c9521cae51ecd41453767b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151596136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9907bd128b759374d997bd39513d1c121813d05310feed6fb7e9034c29bb30f7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:58 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f588ba761977132d2ecf6506e1a07635b1a4ce296a2020cbae117c592719d3dd`  
		Last Modified: Tue, 03 Feb 2026 03:21:29 GMT  
		Size: 53.8 MB (53814976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e718d6ba54b0c9ef8e7ef362b88f8cafb8d5ee38c92f4378a391ca9d905afa`  
		Last Modified: Tue, 03 Feb 2026 03:21:29 GMT  
		Size: 69.7 MB (69672690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe848fcf6579abc3fa184af8460be3fa77e34bbcb6997bafa08273bb2640f7b5`  
		Last Modified: Tue, 03 Feb 2026 03:21:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8e5902c36b6df7e97d9f69faccb78b72aff56b9abfa2f68b664a12edb04f28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a062d6789d6228619c08a374399e79e74d5f9708fa54ae3b1c545d2b804fa2c8`

```dockerfile
```

-	Layers:
	-	`sha256:cae48220d3ec0b2d96809879cd3ef38e58d6b3f17b25e2157420b7105b2a818f`  
		Last Modified: Tue, 03 Feb 2026 03:21:27 GMT  
		Size: 5.2 MB (5241469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129c5dd027835d6712c4a0f365135b11e826b9ff821d87506c2ad44448d2121c`  
		Last Modified: Tue, 03 Feb 2026 03:21:26 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:54e88f5ecef71ab09301fed4adca0462ceedf52790904d1008a24d7cbb98df07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159758522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329fd23f91cc7ec37756886eedf502df508fb9bce018acd9423ed39585ce914f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:28:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:28:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:28:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:28:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:28:56 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:32:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:32:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:32:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce017c8a49cb1ae866b2be346445f9e98394b0ee0a4cef0a2924bd7c8c7eb34`  
		Last Modified: Tue, 03 Feb 2026 09:30:02 GMT  
		Size: 52.2 MB (52175144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95964b7433a262cf84be753fe3d7f4fe417c190a0e16817a64b66576d1717193`  
		Last Modified: Tue, 03 Feb 2026 09:32:59 GMT  
		Size: 75.5 MB (75514020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647cc7c42aaa74d1034393be838dce00a43710ba7922ad0c1e41e99e430b5110`  
		Last Modified: Tue, 03 Feb 2026 09:32:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff1d740eb5d7a39d3c0d739270d1a0a5b2f858b84334dfe78bcac0a27484d3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839d237b667805599de5c90fecfc362cac6d60488492dcc127ed444555679191`

```dockerfile
```

-	Layers:
	-	`sha256:650ffb1cae6bcc0fad6ec7e5ca05159ea0144dc505f1ac2c0189b1f281649a4c`  
		Last Modified: Tue, 03 Feb 2026 09:32:57 GMT  
		Size: 5.2 MB (5240761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143ef073bf27d7633ebcec4df870d61e2c045f0b5c78e789eec48d7e450cd74d`  
		Last Modified: Tue, 03 Feb 2026 09:32:56 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json
