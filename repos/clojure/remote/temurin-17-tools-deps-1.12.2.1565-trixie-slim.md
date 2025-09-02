## `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:ee597e5cab27fb32c0c13db5558b03823139d72562ac52551c79a04a5a923789
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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8ee2feb43209af6b9f35d512f4d766eb196820736355a66c9bd80bf7b4f94497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246450718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d171c2524c45c7cde28b3a5f02fef0b3d90338d12bb233fa781d0e55d9a6439a`
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
	-	`sha256:7f29d863292760475f74c5948ae02914a5a959de6ef99285f09875341a7f75b3`  
		Last Modified: Tue, 02 Sep 2025 00:17:12 GMT  
		Size: 144.7 MB (144693356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e1c2a99fae520737558a491488040f2e0c0553829ec0ca38435b1e046ff382`  
		Last Modified: Tue, 02 Sep 2025 00:17:59 GMT  
		Size: 72.0 MB (71983033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d53b8608fc174f751c78eee4250a00bdc610266991b7c497945977a8c47723`  
		Last Modified: Tue, 02 Sep 2025 00:17:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174b356b59f40982b6f43db0de8577456d21dc02b4862546c004240c3c1428e`  
		Last Modified: Tue, 02 Sep 2025 00:17:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b24d281bad163c0eacad86ab9195f5d3d7dd0554c8d029255300e9a49714d63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2d630172b16a40fbaa865d38d3822aafa2a4fb8fb2bc872880a2c41f6ce20c`

```dockerfile
```

-	Layers:
	-	`sha256:8ca7c23b52d59ea16a42423e1f815453bde3b926fa308a050bf176bf75f33cbf`  
		Last Modified: Tue, 02 Sep 2025 03:40:21 GMT  
		Size: 5.3 MB (5255237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d035cf627bf41b1a5de626ce56ecaf7d8ed4ac0e50388cab744b63e06073ff2f`  
		Last Modified: Tue, 02 Sep 2025 03:40:22 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - linux; riscv64

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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:be2186aa751b9a00925e99850a236c970ee6b95817928caa581828d0d02913b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30881328e6227a46a74d41d9e4d541fc27602274a78588bbd3af3775016cc602`
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
	-	`sha256:a5a1e9e470b7c88bd21688fbc518ea5bdf98b1d2fab1ef9fc4455855387c7eae`  
		Last Modified: Tue, 02 Sep 2025 02:01:48 GMT  
		Size: 134.7 MB (134724306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd9c40373aef1f01b7679f0a307a4d51e88dca4638c77791d3733c7709fa66`  
		Last Modified: Tue, 02 Sep 2025 02:08:44 GMT  
		Size: 72.9 MB (72949443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d059112eb820eb91b568592afadf6769ab48c854df04cf5d6ce27f42ac5b96e2`  
		Last Modified: Tue, 02 Sep 2025 02:08:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7edd659a911a3da9d638710d7f6c89b84c6f0651696f7844536432926ff2423`  
		Last Modified: Tue, 02 Sep 2025 02:08:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce54678c787db9e1418398a1203cf03b2c86241bad9b2b1d47b423e318f68816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fa85f436f2654ed94f1d35d6163afd49515b7842bc572063811cb6e9e52076`

```dockerfile
```

-	Layers:
	-	`sha256:a2750e1cd266f093ff0aee03ef951803c9a244c236db306a8a96be9d0b093b32`  
		Last Modified: Tue, 02 Sep 2025 03:40:47 GMT  
		Size: 5.3 MB (5251161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1ab089ac12b1d8b8a259f6a9f9f8ca986c120865fdcea43a4ff895e25aa02d2`  
		Last Modified: Tue, 02 Sep 2025 03:40:48 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
