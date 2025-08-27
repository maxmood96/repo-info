## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:9d8bc8bfb47f3068b66b650443df2a02c33402c72fb3d6f81a2d5bb0072d8cf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3e54851f712ef60e4acfeeef20b0fff7aa12fe74a91e602d7ec0acecb2050f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246450141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3728ca6c00475ee5fd2d4696ce8ae4c07e86f013e636bac210b4e7237d7a9c6a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df5f9a37b869e6e5edb32c69390f77a97be2d72f920fc00fbaba6de99abcde`  
		Last Modified: Tue, 26 Aug 2025 22:18:05 GMT  
		Size: 144.7 MB (144693303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767402d4f717271999c4fedb4c5c51f93a3d8bc757488b35b4c323162225d50f`  
		Last Modified: Tue, 26 Aug 2025 22:18:15 GMT  
		Size: 72.0 MB (71982511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99203255d1c7fad72157991b1b615a0ab713005c924cad473c8855ea76d78b66`  
		Last Modified: Tue, 26 Aug 2025 22:17:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdb4738eab85301910b5ce61a854a04fdb45d621f006dded34cde4a22a130d0`  
		Last Modified: Tue, 26 Aug 2025 22:17:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a677a0d3f634162c04674b8c299dfb9ffe163fb337084b018f6c1437addcba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c17f40187b5855a6c74d50619161665dae7d5fede0e894d9d47f4d1fa7901a7`

```dockerfile
```

-	Layers:
	-	`sha256:ae7841c992714c56294e9dd1af43bf3502bdb0d321673837fed00ad6ba624861`  
		Last Modified: Tue, 26 Aug 2025 18:38:59 GMT  
		Size: 5.3 MB (5255237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472375d2a9f0b82c7ada4e4e3b7d81260ee71fb9aa7fdb1600bf1331a10dbc21`  
		Last Modified: Tue, 26 Aug 2025 18:39:00 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a59829d559a4f636449f4e66ea73e1fe70a00e2bc1f0658e0657cc63234a4de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245482928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a060c1b668752b758cf1279423fb79f4acae0b532083a1fba3a35b769a080d23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640cf07419cf2a2f084e2df121a60b637ba9a6a3bb5fff3ddc4f930742d38659`  
		Last Modified: Tue, 19 Aug 2025 03:40:32 GMT  
		Size: 143.5 MB (143542104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154bf5acc5b5e32718a1a4a8edb02f894d46893b447d7673827f35d4ef23cc19`  
		Last Modified: Tue, 26 Aug 2025 17:46:16 GMT  
		Size: 71.8 MB (71803736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a492875c4c7a425b11f3f053acb75c0a13be81dd176c90711d0bc95549f98c5b`  
		Last Modified: Tue, 26 Aug 2025 17:46:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649a51ead87f3f672dd390e4782c5165a01d3f2c35e31a247d608d4de1c53649`  
		Last Modified: Tue, 26 Aug 2025 17:46:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ed741e3e603ef3a95e0177529eb72c4dee912d9232e5f0e4ad68b0c2921104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7122bc1d92792953fd7af95f48216892bb0a89caf3b1d4910e3c9717943322d3`

```dockerfile
```

-	Layers:
	-	`sha256:7fc77373dd4b3df31ce48b57351fc205d6057bbfbe54116fb5ec9c1fee13ac71`  
		Last Modified: Tue, 26 Aug 2025 18:39:05 GMT  
		Size: 5.3 MB (5261006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70625ce087f230c2c9b6489adfa0c2df12d062c1a7b3f5cd83645cea3cea987a`  
		Last Modified: Tue, 26 Aug 2025 18:39:06 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:26fdff6f24e14b0b23fa183e08f375c87b16777dd526d1743e932ae8ae3fee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255356763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bf31a540950908f3c8f0123d190d43357752b44e993bd20c0b4f194f11fc02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a139213f46a9b4f3351f5b4b2cdb1bc223768bb802b0d7ecc6c23c9602d56ac`  
		Last Modified: Sun, 24 Aug 2025 02:05:59 GMT  
		Size: 144.4 MB (144372823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8721309013965a712cb423db217119593c15f3bbde7e9936c6a6e799decc415`  
		Last Modified: Tue, 26 Aug 2025 18:03:06 GMT  
		Size: 77.4 MB (77388682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ee7c83e7b659233b687376dcf8f71b743386cfbd7fdaa6c27b80ddd5b7d13d`  
		Last Modified: Tue, 26 Aug 2025 18:02:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e460837911da62fed567bcdad3647cbb455982f8c317644e58271fb967672af`  
		Last Modified: Tue, 26 Aug 2025 18:02:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae0effc731a634a324a840f3953d3eead202b2b00e0fafcfc51edd092c0d2417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c604bbbf0b6baf8cd538df876964130de0fdf41154d86cabda36630ae3095ebc`

```dockerfile
```

-	Layers:
	-	`sha256:076e686fafabf5a09ce87ddf5287b5e5a8ce8ee71a7819530be6e5f24f26f190`  
		Last Modified: Tue, 26 Aug 2025 18:39:12 GMT  
		Size: 5.3 MB (5259608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6265f105044cb338df9d1a887b97b746313e68a6dd8fa42f33311508f01eb2b`  
		Last Modified: Tue, 26 Aug 2025 18:39:13 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:497e19f9731e7ffc4b5683dba2a72c16403611c50226cbf9c52f4ef87653ac54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237724255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e4bd04d70263d6f6c6cc5234b1d92037d885639b6ea23ffca5028dfee4f9cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003c8df477a56c140d3903d6cff477740baf1dc3729dc456ec4837e6f283fe9`  
		Last Modified: Sun, 24 Aug 2025 02:06:17 GMT  
		Size: 138.6 MB (138575688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87158597cc3d80b4f2093dfa5a1e19d4cb29fd6c7fa2a8a264c59e8cc501cc3`  
		Last Modified: Wed, 27 Aug 2025 09:13:28 GMT  
		Size: 70.9 MB (70875898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9895235db1164df00eb1e382d6e29d5158336bd86705e5e83efbeac5b594f5c`  
		Last Modified: Wed, 27 Aug 2025 09:13:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e24d27fc290119c0e63edc8c3d4e81e59fc7370f9d5eb490250f13faf8d857`  
		Last Modified: Wed, 27 Aug 2025 09:13:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd792c2fbd1fde43ba3ad69f64be13ab0046aa3f1bae9abc319f05dcdad636f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ef738175a469794a21a725097bc4f7ded2a23ff9000bc060db426eedc20a6d`

```dockerfile
```

-	Layers:
	-	`sha256:bdc73ff082b2f693e38da22a5d2b6f43afb6c3c89fb682735e6803bade8e587b`  
		Last Modified: Wed, 27 Aug 2025 12:35:46 GMT  
		Size: 5.2 MB (5242782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d23b239548b3555a2b3196554f52c84fbdebe0f3ce07dae3d0209574840ee8`  
		Last Modified: Wed, 27 Aug 2025 12:35:47 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5c2927ce6752a536403995e9139446c49a63601f6b9e222b89a62bbefb3bb374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237508309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd4c19b7fe2396d31399d6835c9158cd5eb6a37d76dae8784231e52107fb535`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3144a0cc045b5340a2720cef30a5ac35fe54584715375680594646fdb9f1dd5`  
		Last Modified: Sun, 24 Aug 2025 02:06:37 GMT  
		Size: 134.7 MB (134724368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458a6d3170f07e643dff262a9d86289afaee6aa9bbde809a95dceb1b86d1b6d1`  
		Last Modified: Tue, 26 Aug 2025 22:19:11 GMT  
		Size: 72.9 MB (72949837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe23b75682c9b72ebae4c5ed01e73d5ecdb58bf380dbaff551a163950dbcd5d`  
		Last Modified: Tue, 26 Aug 2025 18:30:12 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e557eda19b6203462b2ab78f959432733804b94aa8ac81d5385cd96cf9bc0eb6`  
		Last Modified: Tue, 26 Aug 2025 18:30:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91ff8f4f62662e69a6224f4862a7403689ec9ee636f2560a2e428e9b7e3dca7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65bff4c45bc97e34568dfc9428279270f15464a7537b07bb387a0e473371b8a`

```dockerfile
```

-	Layers:
	-	`sha256:3c3451fdcbaeddc67f1017bdc349dbb0d3eea294611e40095adce6e7575fbe3d`  
		Last Modified: Tue, 26 Aug 2025 21:36:14 GMT  
		Size: 5.3 MB (5251161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4358a8b2ff5937e9fff9fb5c39f41193216952ad841e177aefdce46c3f0b2cd0`  
		Last Modified: Tue, 26 Aug 2025 21:36:15 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
