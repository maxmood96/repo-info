## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:be035b9c0267a4856696fcdc0f99424031a3ab69593e6fa180b2d882b8beb438
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff60f5f5fc11bb6a3a02108ead5652c35748f89c748c10fdcc87c35363716b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193826347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35d10e944afbfe16b4098c032788cbf790634519938b9e1a0c458cd32c49504`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ca0e90c0313dc6bffe0393dd5d7dcf7f141c9ea48f075560d1ffbcf1f5d75`  
		Last Modified: Tue, 12 Nov 2024 02:23:02 GMT  
		Size: 103.6 MB (103633935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692235f4903bf3f9ef690319dd8534fc464b55e4471852f958a5ee975995fe4`  
		Last Modified: Tue, 12 Nov 2024 02:23:01 GMT  
		Size: 58.7 MB (58740207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f102d4f3dece76a981be22cc4efa814ed7ef680fb9bad9e4a6ea1478fe64d76`  
		Last Modified: Tue, 12 Nov 2024 02:23:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34a16eef4d7b729ea3b742a93f34221a9739a2dbd1f69e8a6c0aae611214f291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1baadd3c20f952e55593062f07f9d3230d2c2330a3e035059140ecaa3a30d6`

```dockerfile
```

-	Layers:
	-	`sha256:5eaa3e64d6caf8e0e4c88df957d7dc3d2054acc2906ceab1fc4532eb32976ee2`  
		Last Modified: Tue, 12 Nov 2024 02:23:00 GMT  
		Size: 5.2 MB (5247522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99eb0e7ba12e845969584bd65e92e5bd90d87cab09066a6731db344d49181d9c`  
		Last Modified: Tue, 12 Nov 2024 02:23:00 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5eee53aba6c766d49ccd5693c274a9eb03b2af5a6134b33aeacbc13572c5bfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191717602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab28b6b38e02a9ce79e30383dd5e5a6f938db7f51eca051d63484678602dd19f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ef2468ca2121e8498cc091dcad7224da7e6127b4e7bda1c762c0574ef68d1b`  
		Last Modified: Wed, 13 Nov 2024 01:04:23 GMT  
		Size: 102.7 MB (102747730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920cabfc94ff6b7ec8e737c4bd1790a135b8f0af9471982fcef6bbae17d20acc`  
		Last Modified: Wed, 13 Nov 2024 01:08:14 GMT  
		Size: 58.9 MB (58877629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff8bd7066cfdec8f9c0d2c70fbe994cde0d0dee6132821dc483726483ae761`  
		Last Modified: Wed, 13 Nov 2024 01:08:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9816ff5603bce435e35aa6fdeb524146cac2af96c543fcfe3fc2f1a210db06c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1776b11f7caa758a937387f9c2549a5a33b98c93bff69a05bd4d4a2f9d6ad7`

```dockerfile
```

-	Layers:
	-	`sha256:fbe6a528f697dc7c47eb5a69e25f49914b692c3f6126d22149a23ad036686433`  
		Last Modified: Wed, 13 Nov 2024 01:08:12 GMT  
		Size: 5.3 MB (5253958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85bb21b6ca42e9fce9b3c32409d454737277e1e6e9b5a00d6ac22e59c5791183`  
		Last Modified: Wed, 13 Nov 2024 01:08:12 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
