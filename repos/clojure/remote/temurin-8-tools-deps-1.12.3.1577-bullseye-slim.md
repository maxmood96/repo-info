## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:36f9193b040326489c463d98deac046b06e129e573981fa15be5fc9ead4255ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c758df52bfb96ae43b89b1b59906bcf9cea5f92117011048a7b78478579fc9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144142476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323f8e7470879bbd3a3e86ee7551541452fbf257334f9a8e6c74d0bfcdbade77`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:53:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:51 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f762b144e1cb5535fbf0b64b45cc5955b5d58bca82d042672538471a688982d3`  
		Last Modified: Tue, 04 Nov 2025 00:54:41 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba33a88466f3b62df5ba8a73edbe327a83c2138f46b7d75d351b439955133a6`  
		Last Modified: Tue, 04 Nov 2025 00:54:40 GMT  
		Size: 59.2 MB (59151945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38c9ceab75aceb3177cd45e58591fedc7354e80d91846c9bae80cbac23bad09`  
		Last Modified: Tue, 04 Nov 2025 00:54:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:615c71d1a0278cab3683201b7ba5be1af63cba826a1aa6a1029e91a7a435db21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e15e1b867cc8a5a46b5b93b4f991db1bd33e0355cb68d72b1d6ebd253273a4`

```dockerfile
```

-	Layers:
	-	`sha256:aba91d8c50ad40eed943a822436fc36bf3ec8849fa38c449954c638adea63343`  
		Last Modified: Tue, 04 Nov 2025 10:47:59 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f673c895f6593f0be97b8b64cf90704f5b12eb567ca218cf7198f679372031c4`  
		Last Modified: Tue, 04 Nov 2025 10:48:00 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f7cc6673b619a02aef0e87d6fb364124a6777c3e6cfee976af22b29972d38bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141872539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef33ea7a9ba06a3f10390c63fd5776fa340ef3bd0106bab0fc27bf4f4c171f34`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:14 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5322c0ead7f03196c6edd81f478a18f9edc12c090d2a20c187ff5f32553d1`  
		Last Modified: Tue, 04 Nov 2025 00:54:59 GMT  
		Size: 53.8 MB (53835605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed773eaaca734787fc5db22927018ef27d06de17f71794e17cd42464f6252317`  
		Last Modified: Tue, 04 Nov 2025 00:54:56 GMT  
		Size: 59.3 MB (59287737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b00ab9b94ddd2f2cce99797c76dbee2424ed5beded6be91eee78adf16c50dcf`  
		Last Modified: Tue, 04 Nov 2025 00:54:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb6b2a174ca91b319a0da68446f847dd65263600b283962f76ae08c6790732b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b067df298496a48a81371cc055d1e61247868470282622556eae57372098b4`

```dockerfile
```

-	Layers:
	-	`sha256:a9cf0b6af2db0c7b779617665837e1f9d041975806157341ecf9863a30411dd7`  
		Last Modified: Tue, 04 Nov 2025 10:49:22 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb81bcff8973c91e49974e4ccd2d43adb8f461498bec164af3ca3b070c4a55a4`  
		Last Modified: Tue, 04 Nov 2025 10:49:23 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
