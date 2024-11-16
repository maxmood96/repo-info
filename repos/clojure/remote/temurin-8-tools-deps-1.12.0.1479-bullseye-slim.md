## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:6b8f0cb8a9ea4c944dfbba5f862fc203f6fcaa1d2bf828a244c2ca41a38d036f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0f95c8ad575385db0febf67526e20af53f19c6e3848b375b7bcb90f470d570d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193826400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8034b7e352bec45fbe2fffb72d0f81ae5cabcd488ff38fe5d5240fbbf94895`
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
	-	`sha256:429abd4f30024e4371eb02522a6578e5896ba3c148cb7f63a40285031c62315d`  
		Last Modified: Sat, 16 Nov 2024 03:51:48 GMT  
		Size: 103.6 MB (103633964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0757388aacc022f7326fc536922ce9fd7f8f5a61bebf2f311f96edcf294a9ab`  
		Last Modified: Sat, 16 Nov 2024 03:51:47 GMT  
		Size: 58.7 MB (58740232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d651790794b57c14c9756a4413fa7092c8b1c93e213f1e020470166765e392d3`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b6132bff2cb53906b2479859549f2ea2720aa6e11b9e08bd5902b3282c1a2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4421e4c33f8f3725794388425a9e3f6b4c7de79ea4d258f1d1fe0cd391e5607c`

```dockerfile
```

-	Layers:
	-	`sha256:50d29d4fbeba62fbb5e9166161a217e7554a19e7b21b0dd8252c499de73f4029`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 5.2 MB (5247522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11378cc7a45c13ce66c57c31b4a12f4f49f752bcd118476266128415b793eb57`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 14.3 KB (14293 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:348bfb0a7ff68b6dac7bdc22a7c1dad83afbe74250324b270f4461d6137ed9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191716076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae509aeb0c290246d71bc6a98874874adf89988e9804bb2adbd94d04fb8e7095`
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
	-	`sha256:90545bb27805e104123f01b3e16835ce4f6e45b25a39ba2f670aad5c259ca992`  
		Last Modified: Sat, 16 Nov 2024 05:14:02 GMT  
		Size: 102.7 MB (102747710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f2f108b24a554ddc836ebfd65f70a3e9943c041f64d50d671409d48d5b99d`  
		Last Modified: Sat, 16 Nov 2024 05:18:14 GMT  
		Size: 58.9 MB (58876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67b6507464b438a14f5097f7225cd37a11d047a6f0c1c193bb2b57203ca3422`  
		Last Modified: Sat, 16 Nov 2024 05:18:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:37a19328b9fc1444623ba3571f53e2125db9c8b78b585ae23042862771bad68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2c1fbb9694ab664016402ea708d3ce79e46902cb321d0ed9228ad44e52c97c`

```dockerfile
```

-	Layers:
	-	`sha256:e3160d75d6407930453a806451bb503dbf58ef14b881882ecedac2242cf2467f`  
		Last Modified: Sat, 16 Nov 2024 05:18:12 GMT  
		Size: 5.3 MB (5253958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd47001902560f19bd37dd3a186eceb03b53d2a6b67b92fc245d7e083136a51`  
		Last Modified: Sat, 16 Nov 2024 05:18:12 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
