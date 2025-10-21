## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:d9dabd169071be8f1b5e7130f17a51e6050b22c5abc17d0aa267da6675d47bcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:56d6f061b4149f3d7c69d5155ea041c1b46e20cdb9a71a2427f5e6e8a4ecf936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156504176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03509f3f397e964d644940e0ebc61502ffb8387d59cb22650f02f5ffd14e599f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07714ac29952818337dc242adf8da94b6919a2cb37d259e79cdf56455b6dc2f4`  
		Last Modified: Tue, 21 Oct 2025 02:19:59 GMT  
		Size: 54.7 MB (54731352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbced3b99a418ec2a0e8213792aed567ad0e3dc01f1f5a89eefd4d045076cfe0`  
		Last Modified: Tue, 21 Oct 2025 02:19:59 GMT  
		Size: 72.0 MB (71994256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffecd2ecedfe9b823f9faa21a9ea7a43628ab74e91ad7bd632307915cc24b68`  
		Last Modified: Tue, 21 Oct 2025 02:19:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2cc47f1ad79c44d796db5e90ca38a74fff31dbd009fcb58ba3d559f51afb7e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b5492e73f3a20f3a4a7432fb61b27b430eeb06fdb404faa80982e64e7e5d62`

```dockerfile
```

-	Layers:
	-	`sha256:8da33c22cc55eb113ca1b5a7b34c0ad597f9cb84a6e969f5e60d7241306c1a0a`  
		Last Modified: Tue, 21 Oct 2025 09:48:05 GMT  
		Size: 5.4 MB (5377777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e29a04d2f1bb6e5108975fa38f53e48a1e72ee4d63e40e105911a175ccc851`  
		Last Modified: Tue, 21 Oct 2025 09:48:06 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f393b618cd3245cc50338cb2c4d670a29ed4baef91a27c951f83b712ede9aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155786866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62c3f8c08c87ca0a25178465b2f599e78a43d8c6dbadbb4888ffc3252aa80de`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bca21515bd3733244cca6de7a301d65b5d5851e980d67367c85aa74b1bdb309`  
		Last Modified: Tue, 21 Oct 2025 02:25:06 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc927b022ea0ff069d33f9fe788d597729b233a1626294696010c64013d0bc6d`  
		Last Modified: Tue, 21 Oct 2025 02:25:49 GMT  
		Size: 71.8 MB (71808487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f137299f5991b5cd287d0642ac8e8a807a5d1d423f7154a729cb30d7e3e1c570`  
		Last Modified: Tue, 21 Oct 2025 02:25:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ed04cf049ab80e630b9777b7ec927e72c89d9beb19bcf6988e47f5d57e0999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa4d5362e9f1b2b29122aef2c8657630d2a4b50e34a920023f9ab11fd8d436a`

```dockerfile
```

-	Layers:
	-	`sha256:60055fa787f261ef6cfe441c27f6951427da617c7a9fd3289b10662f93b7376f`  
		Last Modified: Tue, 21 Oct 2025 09:48:11 GMT  
		Size: 5.4 MB (5384244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da2e540f3dfe788c70a63594f1d06185f48e33c09ae9aa5e2b9a0ee9b20bbf1`  
		Last Modified: Tue, 21 Oct 2025 09:48:12 GMT  
		Size: 13.6 KB (13589 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dd3a87d7d487c5e3b9ca97a330f354fc9d18b5ea3829c493a1faae5c751d14d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f24df693d9924351410c23fa04a02a19013e2263bf42067d9925430a5b95b77`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850f6bfd7c5a8dd3875f0dbd8746815ac97b4f412c114102fd1d99799526a2c`  
		Last Modified: Fri, 10 Oct 2025 04:47:10 GMT  
		Size: 52.2 MB (52165392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0950612e1044930e7226f77d156aa1393b290600cd86d9f9aca2131b70b7b1`  
		Last Modified: Fri, 10 Oct 2025 04:56:17 GMT  
		Size: 80.6 MB (80588281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2b2c0fb131309dcb24978b0d381d0ddd0cb338198996a52811f651e0d8090e`  
		Last Modified: Fri, 10 Oct 2025 04:56:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b970338235720b1a6a8db4a6288670b25fd1645f6a3850d2cffb829fbebf620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6875e71136e24efa7e82101bbcc7957fc9d00af953f968f8838418c27e5e1c`

```dockerfile
```

-	Layers:
	-	`sha256:5dc1bfabea2d19ca1c2a309fed9b845dd0e295e46a2c539df79bb59343a6192e`  
		Last Modified: Fri, 10 Oct 2025 06:53:08 GMT  
		Size: 5.4 MB (5382741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b11973620c6267bba6216dc24a86e42a2337beecbd0d51d65b66967f46a4a14`  
		Last Modified: Fri, 10 Oct 2025 06:53:09 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
