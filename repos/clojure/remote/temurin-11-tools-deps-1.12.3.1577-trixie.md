## `clojure:temurin-11-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:39b6bb535cc95a6192c785deaf3f531e0043c69c6b36c82db15df58007d4b95b
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e98c8bc343755e2822d9b488f9af5bf9aa5e5de2e73d042dcb4c42a2e0f9bb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279793563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cced8205e11ad767818d700a0719141f96a9f73261b6a27fff819e6e3437bd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:51:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:51:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:51:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:51:47 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:51:47 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:52:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:52:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e3cf7e2bfd34b2adbb15760a43abc77c427118e4276dd983ad00e04b8a46ee`  
		Last Modified: Fri, 14 Nov 2025 00:52:25 GMT  
		Size: 145.0 MB (144966611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8842a114aaedeb327ea2d9a47648807cf63d387791019b7022c07ba4379300fc`  
		Last Modified: Fri, 14 Nov 2025 00:52:36 GMT  
		Size: 85.5 MB (85540678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5257c21118b81f11cc9fcf69452426ed3698cc84385866721c11ca57a54b8a`  
		Last Modified: Fri, 14 Nov 2025 00:52:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2ea416c9d6c8b428e5b75baa6b5d8e4d2d03c99018c9c46937d09f53af260980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44016aaf9cf1e22a5a3969bee039b83a494ad7c87b266b2a8989b355fa8872a2`

```dockerfile
```

-	Layers:
	-	`sha256:5a145d4b8c2cb07e6d61739d1d80dffdc1beea56a373ad3295520bf7d191a18a`  
		Last Modified: Fri, 14 Nov 2025 01:38:00 GMT  
		Size: 7.5 MB (7487040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abd9d8fce9163a159f2e7fd0574ed2b35f74f4a76510a125f8c2be38f834afc`  
		Last Modified: Fri, 14 Nov 2025 01:38:01 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:82cb26b71599138fc2ae772cab489530becde0d03a5bfd1e456bdc0f95fa0bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276745919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2584955a53df06c657506d5c4dfbe52d24ff41938ee77f9eb9ade062d1307fc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:48 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852b3702d15fa65362d783c6a2787fc6ffdbbb89c813654557604b6faec2ac7b`  
		Last Modified: Fri, 14 Nov 2025 00:54:33 GMT  
		Size: 141.7 MB (141731550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b92274c4ede4dd410d79ffed00c57e0b52fc5f11dbfe5e047280cf6bb47ef06`  
		Last Modified: Fri, 14 Nov 2025 00:54:46 GMT  
		Size: 85.4 MB (85363292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84963c4e05ad8f1e24b3fe24f91672c7512d44e2b90dd3655bc575a1aab11820`  
		Last Modified: Fri, 14 Nov 2025 00:54:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4fea64d294f35c855212b73256a5830312ba27ccd6e12c1b0459751f325770f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376ee30e63b003481ce2388fa55484b1406874c0d16370eca49f72cbba2ea976`

```dockerfile
```

-	Layers:
	-	`sha256:a818f51bf660993f709a508d6232a086285d2311ebfb9da3b3ff3fac83c12ea7`  
		Last Modified: Fri, 14 Nov 2025 01:38:08 GMT  
		Size: 7.5 MB (7494688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9a88c70d023a92dc125b0fe10f1a6a63869360930a99647c717e7ec31f0123`  
		Last Modified: Fri, 14 Nov 2025 01:38:09 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b5e9130f0e1309e6658284e42cf1535cb8ce34ba0adb74fc65d155f244c571e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276140624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2b8ddba60a83b1b1f0f7d78570cdd11d15c75701009d1107b03640a944c1ba`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:28:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:28:28 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:36:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:36:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:36:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8e3e02a4f5bce482ee6878197966e1ab6c51d874ce72ba1d61ebbe633711f`  
		Last Modified: Sat, 08 Nov 2025 19:29:39 GMT  
		Size: 132.1 MB (132079844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1ffd42d12a415e2c9e359d008400ae32ddf72824b7f12df8637cfdaa195810`  
		Last Modified: Sat, 08 Nov 2025 19:37:41 GMT  
		Size: 91.0 MB (90950008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145fe4c69a08adffa317c99a2cd50d85e89ef750a87a78f4e164bd55e8f264b5`  
		Last Modified: Sat, 08 Nov 2025 19:37:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e529feff6780aeaf039d1cb92d870998b8b8afa8b8cb0f19d2d2390293cd6d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5234a9d293e1b95284fd5e5093d8a4320e314caefdabf990e657011dad0bd1ef`

```dockerfile
```

-	Layers:
	-	`sha256:d843b3e8b5c364eaf573e485744e50a581e0f23df1df900c581b8c074b253693`  
		Last Modified: Sat, 08 Nov 2025 22:40:10 GMT  
		Size: 7.5 MB (7490844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b893afc4e1533672ed333784a60ad8f95599f253a074ad67ad5095dadc015d06`  
		Last Modified: Sat, 08 Nov 2025 22:40:10 GMT  
		Size: 14.2 KB (14232 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a8117a05a9ef040e2d1f6aa6ffdec0e275e401ec1aaa8019dd5e0e93cb857532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261556002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cd811046844dfe0e942be430e487209b7dbaa8f4de7e7cdc6cb94cf077a64e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:13 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:52:13 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a213f18554008fe4500d07244be8d9e9a685b476789161282afef051ba3355e0`  
		Last Modified: Fri, 14 Nov 2025 00:53:15 GMT  
		Size: 125.7 MB (125694467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18df3bd115188ffe982fffcbe9da98cbc625de5a63943d14799ed9f8809b6d06`  
		Last Modified: Fri, 14 Nov 2025 00:55:08 GMT  
		Size: 86.5 MB (86508590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54801f047191e67fcc4d8608ccc33f6fb026cefdee1a767967b2b06ed40fadf`  
		Last Modified: Fri, 14 Nov 2025 00:55:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fcc65a99d3de9f8836601b86122c5ce880a4c35ab1e3932d392714ccd25c2122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee7ac758d5abd1da45fe740e24a83ffb4b4435f06917da8081b8a06b8a2c92c`

```dockerfile
```

-	Layers:
	-	`sha256:ed733d5b0c61e7e647a304ab1385851b07d6b8c70a39caa992b17d5e01838a3b`  
		Last Modified: Fri, 14 Nov 2025 01:38:21 GMT  
		Size: 7.5 MB (7482966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1d5e645d8dd422f0f2e19f564615eade0409066562168aa009e73be3a82f800`  
		Last Modified: Fri, 14 Nov 2025 01:38:22 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
