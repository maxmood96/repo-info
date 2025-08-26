## `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:0cd8454e23bb94a2f14ceee2c18d8ce945c2da50fd0578681f2b4dd6654cbb0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b6d1e6632ebbceccc0964101e6fd60e6f86f9a1251f56c74d320bdebaa19877b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184364765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54e3aff9b008e0ba292f89ecb887b42db03deae562d50a5332e695ee8ca0aa0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef10ccbb6d40081f550d2d19df0c994c6d9ad815b9c7c74f1f859646ba1b5b93`  
		Last Modified: Tue, 26 Aug 2025 17:28:08 GMT  
		Size: 54.7 MB (54731325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fe636473dbc172fd95cb150d63e4c0a6f5fc4e3e3885a55f3e468284acee72`  
		Last Modified: Tue, 26 Aug 2025 17:27:57 GMT  
		Size: 81.1 MB (81138282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037fdcab02ecedee5c173c1bb1413e0b2c25b0e5ab56ed2bba43b05b479c6c64`  
		Last Modified: Tue, 26 Aug 2025 17:27:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:457ada188b5d8c66d676c6b0a2a5299131c48654e9534395b280803d2f49ef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde8f3106c8ab47305c2156e93872e5a8c4e4585a6d766f5972fb487c4c85c35`

```dockerfile
```

-	Layers:
	-	`sha256:e3afa4adb0258426861041814cc6ada9c4ad5260d5f54f9b823a45ac6df94e30`  
		Last Modified: Tue, 26 Aug 2025 18:44:45 GMT  
		Size: 7.5 MB (7489907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff51072b1f8b830108493eb5ffd9227b24fefae94da605a33498f80f272fa22`  
		Last Modified: Tue, 26 Aug 2025 18:44:46 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c58db2214c3276191b9c8c521f140d95d937f4926469445e4b9bcb2b872cca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183188104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f40ceb73033d105cf8daa73d6cb05fc2fb94f9eb3e99ab6a78e13acb17c4c5e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab8e03733fa4cd230f3c654cf2c9de160d54ba2f0b7af6f920b3c8ffe594231`  
		Last Modified: Mon, 18 Aug 2025 16:52:49 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadc1236379723ba9f788497752f33352451f41715ee2b271f81d9794efd199`  
		Last Modified: Tue, 26 Aug 2025 17:28:11 GMT  
		Size: 81.0 MB (81009399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac1b35762c7b9b5d068ed016ff3d80968368b68f919f10d0964759651618af5`  
		Last Modified: Tue, 26 Aug 2025 17:28:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b8bd53ef3d4f28cd1c8bd04f43ab6ef5ebe3458ad708012e9f79ee13e1cefbe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5836083437c36ba440b11adec1239fd18e4338101ac26cd7e3bdf7b3f2fca86a`

```dockerfile
```

-	Layers:
	-	`sha256:47056a4f6b3abed98615415b4c92568e5227e477c2209c8e65c835764f677c62`  
		Last Modified: Tue, 26 Aug 2025 18:44:52 GMT  
		Size: 7.5 MB (7496368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a147991461f593fc9f05898b878bbfa5a14865ecd235761ae4049ca7f360dade`  
		Last Modified: Tue, 26 Aug 2025 18:44:53 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c016aaec93b05cb82f6bc699865b56cb051f0866d9418b15c078231ca16a25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191476813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ee32566e761f216223d056c867254bb4e58dabfc68d0ace4b367d65bee3b8f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47051cd5c75ec10709ec504d89b39f72c1348ec4054ca49be83a8093cd36b3e5`  
		Last Modified: Mon, 18 Aug 2025 16:58:10 GMT  
		Size: 52.2 MB (52165394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7680678465b4587df92250daf849f4b5686df684d75eecd6d9e39528d6b9dc5`  
		Last Modified: Tue, 26 Aug 2025 17:30:31 GMT  
		Size: 87.0 MB (86972695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c71b2780d0e7d4c66c185c57c432293866f55fa6356d664398d949cf9b3154`  
		Last Modified: Tue, 26 Aug 2025 17:30:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:88b39871024d63f82056ed76aabfd0f2e63675237baf97f6cd52921f45a7db87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed8de86c131cc606e5dcf4e770780f45ae178b3a7dcd3af3ff2f24b36309cb0`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b7dff2e2d6d781dcae88a57cce2524b06b5ecc542ba6caa8850055c8f3527`  
		Last Modified: Tue, 26 Aug 2025 18:45:00 GMT  
		Size: 7.5 MB (7495704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dbebdfe73740f5c0e3361fb576eeaadfdc18ec2f5a68284a1d8ef4a7dda755e`  
		Last Modified: Tue, 26 Aug 2025 18:45:01 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
