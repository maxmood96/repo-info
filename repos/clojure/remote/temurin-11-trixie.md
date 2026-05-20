## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:2871d5b63add7efac0c1e5a47e7f2b0ce24bf48f98bb7db42f970bc3bb6b2ae8
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a1be2e6d7c4b599685807f9dfa5abed58ec52f190a0b4f8d96b4fe42e593e9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280804920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f907bca55c58dff0906dcb2d8adf1f2426de8bd1f7dbfdcd2f37503c513d7b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:58:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:13 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:58:13 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:58:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:58:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4efafb668a2750e069f47336bd6671b79f6e1cf314ab29af76a0f2e60f2d9`  
		Last Modified: Tue, 19 May 2026 23:58:56 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b796c6c2bfd6a375c2eadf9c90fc096f7d88109a7f139cac7d973e406f40a2`  
		Last Modified: Tue, 19 May 2026 23:58:55 GMT  
		Size: 85.6 MB (85607390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2567a44c370b28676d41e647224f98d87837f1cb8853240fa72b3bd7c5fba9a0`  
		Last Modified: Tue, 19 May 2026 23:58:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6d7ae174c291bde21a620f5fdbac27b111608c9f9252252efbf2ea6da1043a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f16e0a9b50351f63695168f6a37e48b0beb99588158a7be08f8ce3bbea8af2`

```dockerfile
```

-	Layers:
	-	`sha256:ead58a1ce17333b43c5c004877af6edd60dc6da49080a75484ebdd2fce43035b`  
		Last Modified: Tue, 19 May 2026 23:58:52 GMT  
		Size: 7.5 MB (7491012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9a081f71db06e8cc316d6cc1398681cbce78b674b794b3cd4b7848788f76bb`  
		Last Modified: Tue, 19 May 2026 23:58:52 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dce17c95a5336e8dc289115ad9a9fa1ae106590c3718ed6ca62e68638f6ccfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277686593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d79476d7c38d76dedd8f1115baf68ff5a791841873f475f5c8699f94f6be8ba`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:05:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:12 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:05:12 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:05:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:05:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219861c11c57f50fe8e376337efed53a48b754c9df99db788c9a4f77c3791de7`  
		Last Modified: Wed, 20 May 2026 00:05:57 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8993921d0cddb622bcba966a78fab57f5a0eeb1348e4ca6c695ed42e458b5bb`  
		Last Modified: Wed, 20 May 2026 00:05:55 GMT  
		Size: 85.4 MB (85431498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e700f1ae052b27a1f39cd745030ec9f5ecb2991dba5c231977b5c5d7adf410`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9afe79619dc7eb1a1a2bb0defd9af4c71b55c3cd13843f9a9425e47a5a44aa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8be95ee52c1546b5c6642494f528495dd3f25b9c6ff58395e9f96e4d45a567`

```dockerfile
```

-	Layers:
	-	`sha256:cc257c2f2672469403b264e6a75af5e2c66d99945b2bd075318612ed14b50394`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 7.5 MB (7498023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4770603daea335d76535163286eef2bafa7a7b9e548e92f002e086c4b62d61`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:05fabc46c897817ff30aff8e3a232ae83158b06edcd03b3b6cc0cef2eae10593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277240935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f47f7c5082ddb6263e5aa4cf3edafe2c535ddcd4c0badb9262c5ce886f13078`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:20 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:26:20 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:21:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:21:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:21:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6819a6f95dd2e4192ab6b7dae90a40976321dcde2fda4665eb71bbac73d5122`  
		Last Modified: Sat, 09 May 2026 02:27:27 GMT  
		Size: 133.1 MB (133110167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff49e822af717e234b91bbaed5ed00ee4f47ac07108b9190afd63c350d995ba`  
		Last Modified: Fri, 15 May 2026 20:21:41 GMT  
		Size: 91.0 MB (91006955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce615e65115be1342d8648c2db9beeaf4a12533b06b89e5f7b336a70a73bd2e`  
		Last Modified: Fri, 15 May 2026 20:21:38 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8862e75fd74c43724cfa30e7058c52e16bd0605a6e7689e60b9b1d420c62d4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516cec7e6287bf8624cfa8ad7a7fa51933b7f9d12e111a4e1fc9e2b254285beb`

```dockerfile
```

-	Layers:
	-	`sha256:d02bc1d7c0abeb09d62f436dea4c689d337d7b44911fc88529cd54e379cd68fe`  
		Last Modified: Fri, 15 May 2026 20:21:38 GMT  
		Size: 7.5 MB (7494704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2f0cdda3731d6f7c1b54e43189dbdfc07c28cf24a0d9e2d609de6ca994dac1`  
		Last Modified: Fri, 15 May 2026 20:21:38 GMT  
		Size: 13.4 KB (13432 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c68d7eea7c4068d0ce2b8236dcd7b1afdcff62f588dae9c75819a44e46898e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262591672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190725cdccd7f07c3e7727df38959e6884e86c7dca227f6efb9ed60896d7b13a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:45 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:46 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c8c6065ad7c76b091e258045d75213f8970d8f170ffa27f4de19b1ea27fcd3`  
		Last Modified: Fri, 15 May 2026 20:18:00 GMT  
		Size: 126.7 MB (126651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4806b5bcdc73821d904db580ff8784fed05c8be4a5d48d3b5fac557ce5419ecb`  
		Last Modified: Fri, 15 May 2026 20:17:58 GMT  
		Size: 86.6 MB (86567004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd669a44e4030ec81df4ca1fe60a87f3d58e114872870b6243e717312cd94601`  
		Last Modified: Fri, 15 May 2026 20:17:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:46ea7e79fdbdbb9794484cec4b33350b020fe021d636a05d4af3f4869d0efacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3811aa3a20ba673c635b4dbf229315f59cb751cd9861b3f6e5b1c204fa9a560b`

```dockerfile
```

-	Layers:
	-	`sha256:f89e86bf944d4312844ede4bf35d26c93065bfbb4a58b2eef30b2ae8272dd4c9`  
		Last Modified: Fri, 15 May 2026 20:17:55 GMT  
		Size: 7.5 MB (7486824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11e00a87410cef9d0c98d5b6056767c9f53bf9513f51021dea7d9da9bb013e2`  
		Last Modified: Fri, 15 May 2026 20:17:54 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
