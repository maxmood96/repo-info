## `clojure:tools-deps-1.12.5.1645-bookworm-slim`

```console
$ docker pull clojure@sha256:a5b45bb4f02f129367b8f05b7de1b50ad8a0e2d72d14bb6b786b036daee99217
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

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e2d0a61db6e21902cd3524fc78f4cdf24ee6373fa7762a31c08b6acf25d7436e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190546467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b715a440fabc49963c9753ac68f8b29e5e0d946962140303add3b2a561530127`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:01:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:10 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:01:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d7c003a9799fd0b5028602ab76b4ce46b51602570aca46308f1fce1585208`  
		Last Modified: Wed, 20 May 2026 00:01:43 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e558c5ccb5de6557cec344352c3fa49d54df9e199d14a5088ffe1e77ce186b4c`  
		Last Modified: Wed, 20 May 2026 00:01:43 GMT  
		Size: 69.7 MB (69737317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e4dccf0c4b54615b6ad93d26f3c7a047cc443357a3eef08857a3a5933c9d94`  
		Last Modified: Wed, 20 May 2026 00:01:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a206d379db06431efd1be868204df703b4b5bdb2e9f8c11949797ef0ffefad09`  
		Last Modified: Wed, 20 May 2026 00:01:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed19bdb0e35773baa2a1dd8775a577b26d267b58e25d223360085de06dd8dfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4b11a0909956ffc494f516b3867da2bf8ef2ca74d955ec09c55e56a2e4bd8a`

```dockerfile
```

-	Layers:
	-	`sha256:7db71eeef87ba70a27df3d327504b16f4ffd1479610a37b2c462d50aa2660b89`  
		Last Modified: Wed, 20 May 2026 00:01:40 GMT  
		Size: 5.1 MB (5084904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1b52450a89dc2c75509428842d38cb06cfe50e56ce0584c299ca953596bea0`  
		Last Modified: Wed, 20 May 2026 00:01:39 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce4f50cc5d8d37b7acf6e360a947d86279444ec444f82c42bff1e6998ed2ecbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189390030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7534c8805c4e0018f8e2959ed80b49f24e839b2e50f9212d3bd75ddce99d5774`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:08:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:17 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:08:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875ad743d27c0f25150dbd995e073e4adf3ede0b75c5dc5f062fe2bed108b50e`  
		Last Modified: Wed, 20 May 2026 00:08:56 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0edd6e2c77a6a5d0cc9f6319208341354015d2ca8204dc944848088f6c196f`  
		Last Modified: Wed, 20 May 2026 00:08:55 GMT  
		Size: 69.7 MB (69731683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04fd25fae068190d197971a506859ddce1cc7cd4efdeec19c4f6c447aba6fc2`  
		Last Modified: Wed, 20 May 2026 00:08:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa82fb8ee0de74cb33b714114f0d7a6601203e8c06f26fb6edc21f8c80940d2`  
		Last Modified: Wed, 20 May 2026 00:08:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb3cd745fe379d5c4fa2e7811161e1bb0ddc67fc7192d88e751894c864d7ef81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe602550ea7af57a5986956b88d7af75160b18b564c09e51374ddb5b404183c`

```dockerfile
```

-	Layers:
	-	`sha256:7f70bf3415ec3c909242f7e3e3e2b60a21103ca416af55082c5780b4e874cbfd`  
		Last Modified: Wed, 20 May 2026 00:08:50 GMT  
		Size: 5.1 MB (5090686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51767ff1cb356b831170e4d6eeae38c55cb79e96f95129fb050930f97da8ef8e`  
		Last Modified: Wed, 20 May 2026 00:08:49 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cbb4b7daadfa0c462fc14cba0ddbfba5ecba6b1e8b66e09fd4669db3d629c44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 MB (199558906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa012dfd5fc8edcbaa198dfc20e83569c578525208d34e02e65cc766f96d54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:42:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:17 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:42:17 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:32:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:32:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:32:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:32:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:32:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d1c7548cf004fea430b1528d91b72c7b0058d926919d1835a7b351081faec`  
		Last Modified: Sat, 09 May 2026 02:43:20 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef322e3a9c290183413fea60e33cc4a1da4745a950e58c8a325c55ec7434a724`  
		Last Modified: Fri, 15 May 2026 20:32:49 GMT  
		Size: 75.6 MB (75565378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ef33cbb31e1ac133c3fc1d1df7262907e43b66870dc2b1a74b77ef1c451547`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cad7a6a304705352e1e244d6f39b14759681c631d122931f2129abc462ccd1`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a89e656e9989aff1486b9f0081931662820da9385a6177cafed0509a2c6871b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36914c959b1e9b82efcb5629bc62d1b6999cc9e78d3c4a86cef88429280216d8`

```dockerfile
```

-	Layers:
	-	`sha256:0e30984ac041721ba8ce2b83e257233426909dcd9d83f48d16838ae84d6d878f`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 5.1 MB (5073364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8616656158ad103b09e9b3a8246aeba60f470c0953f3b5fbbefb1a8805e1034f`  
		Last Modified: Fri, 15 May 2026 20:32:47 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:16136689c5dec65906a1586c47e155f0f3206bee93165a6338e68b52b5334f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183856969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3ea26f9e69615fcb5b64331000900f12386397dad4049594d3343d4dbb3fb6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:37:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:49 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:37:49 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:33:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:33:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:33:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:33:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:33:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ff53ca1f92c2f307e0a9048298a9fcf9270e8898d762120f6bd32811caf21f`  
		Last Modified: Thu, 14 May 2026 23:38:29 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5359b6ac08205bc70e307c47c18feecc111b364925cbed2f2e5d1552026d7e5d`  
		Last Modified: Fri, 15 May 2026 20:34:23 GMT  
		Size: 68.5 MB (68543987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596436a62c1df02781027a1fe7dad36ea675d63c02d35e745d762b23fa17f17d`  
		Last Modified: Fri, 15 May 2026 20:34:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959d09306752ed004dd43257c4dead6cc70e27111afb731d5515cec76015bbf2`  
		Last Modified: Fri, 15 May 2026 20:34:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1645-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e51879f296762deda6ae827f09885b6851ec04e17173ece9600d7df79361226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81206a213de784537a2e211ae784c8cd465b660972bf5f80d6c04c2191b0cae7`

```dockerfile
```

-	Layers:
	-	`sha256:27198c953db56da300d1447379b131cecf8925616ab48e3bd53ca959099b9e23`  
		Last Modified: Fri, 15 May 2026 20:34:21 GMT  
		Size: 5.1 MB (5060765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1f4a61da3d5c1fecf99d6ac59bf12841f1f1f860f2d96197df39e744f3cdca`  
		Last Modified: Fri, 15 May 2026 20:34:21 GMT  
		Size: 15.7 KB (15725 bytes)  
		MIME: application/vnd.in-toto+json
