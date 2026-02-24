## `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:f73026f522ba157182cb93de47a6c4f7b5dc3536e95cae984b5f557f4f2477c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5aee653647a5a046d59a76a08fd2ffc31bf2e8a308c6e0ff4c2c1f01fac6f674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153085182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d920a37c49c3b0f22d4c7a455db7de2152cb5657cb49dd5254768fa401288c2f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:52:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:56 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d78fce1206ac2fda2e1842a35a7b1064c5515f38ee0d94eb553d3ca345a7a42`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c693aa26e2c870ebf896baf6746d4de93e711c279a71a2aa06d849880bcbe90`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 69.7 MB (69678191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa74829ed0368a0571d329b3f8a17a82fa0fa88dc5578e2f3d927a46508ec1a`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:035f5e457f0adface6dcf8ccbc4dadaf6310f14bdd08b4b956ccd132147505ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6660c0140a97165b5d353abb2748816cf16e2a978b3b4c5a56eb218892584945`

```dockerfile
```

-	Layers:
	-	`sha256:f23e539434ad5b5d9607ea3b174b7031ad4d1573a8d8c15c051b109087fca73e`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 5.2 MB (5235641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cefd32fab7887b194b638f1325987ee62d00312ed708c4f0596d8c0ece8869b6`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 14.2 KB (14246 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6bf8943d008c5338b4bc6e1134b5553303c690225e2bcad1856d86542db38478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152041072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd90904883fdef2a55b087bf9cbe3a06721f22c7a89cd116d50f2536ae018a6a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:03:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:03:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:03:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:03:17 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efebc0063ab903aa1b94c2759f150e779c405e898766b5d7b6e979d09a1236`  
		Last Modified: Tue, 24 Feb 2026 20:03:48 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbae7c37dc254edce5f0e679ce13c4312542f11bb3ce3642e09e2ef3290ef54`  
		Last Modified: Tue, 24 Feb 2026 20:03:48 GMT  
		Size: 69.7 MB (69672729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429cb800c75186edb5560f39e05adf7c943bd26cf2d59724708b6d63864a642c`  
		Last Modified: Tue, 24 Feb 2026 20:03:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80323ed705dd702ad4ddf9639d935a3b5ecb4543064d27ad3dc3ab20a014d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5256467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7c39db9bb916be5650727ac0484cd08c7c68a105ef66ee3d3a53612394a07`

```dockerfile
```

-	Layers:
	-	`sha256:57523d2fd4f613e4fdba0ac8f7c385a15cfaec0770b332e5f804215da89effb2`  
		Last Modified: Tue, 24 Feb 2026 20:03:46 GMT  
		Size: 5.2 MB (5242102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a02ff498b1dd77dfe4d55c68e1f04c91c3d2fb3c95048adc730972f85d0fda0`  
		Last Modified: Tue, 24 Feb 2026 20:03:45 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2468db0ef0e4a17da5e91a1f15797054ccb0a46ed2254f528d4ee71a202f94af
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

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:63650798d52ff50d197fa8d9cb62a917002541c4a440bd8f1dcf10ab7acf9602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2175ebdea2cca59be034c39fa427a282c64a9a94508e673f1f9283834d7bd5a`

```dockerfile
```

-	Layers:
	-	`sha256:e8115f8f8ad8256b7641cd5b0ed9bcf5007423e2e79cf65fa1f25170178bd640`  
		Last Modified: Tue, 17 Feb 2026 23:29:50 GMT  
		Size: 5.2 MB (5241394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a9dc296b99c70a34b7c5ebe02006d5e142cfd3734c99cfe1dd2c5b5f2663e40`  
		Last Modified: Tue, 17 Feb 2026 23:29:50 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json
