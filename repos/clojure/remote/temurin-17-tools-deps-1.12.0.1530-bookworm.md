## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:05917a3d0628af646cf675e9b2ad3cac15e393a27d522659a60c44a29cbc8964
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

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:25f26f6235494593c940cc3e7695892681d27eb35d8f4c683a9d24a1ec51ad87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274118895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a007ceb562ef8a14c6bc5861cbf8c489cb839e123e134de6d5e7ee81c08d177`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811142764e4bd248dcb91193058d25b9278e8999f35cf511e3d3c2c20698faea`  
		Last Modified: Mon, 05 May 2025 17:07:32 GMT  
		Size: 144.6 MB (144635028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2c1defc4b0e23204341791be94a4b38a4dc8160e02b8444dd244d1ed7fb998`  
		Last Modified: Mon, 05 May 2025 17:07:31 GMT  
		Size: 81.0 MB (80991630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f981e63eadae807769b591d0fce420d8c1f5d5f21839a55544e89d74b754b769`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a54d1c8d92f6f2129d25c5d43433496ef8506963be38c2aa49f76c2e066698`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7857262a36751343dc525c1eea7bfd267791c6eb79ab233a4ab378092bc4d5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7188297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247785eeb212ae6a6cbe36e8cae45263676e7aabf59d9e30844dfc3fe6cffabb`

```dockerfile
```

-	Layers:
	-	`sha256:8f5ac1290cc1473579050be0ea47a5b321c4299c3307dfba12cf0607bdf9f38e`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 7.2 MB (7172476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e43d8c851ed532da4e3cf3314a4367c3bef167669a90f06c8f23d4343b3c02`  
		Last Modified: Mon, 05 May 2025 17:07:29 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9f3935ecfba078c84a9742ac06a734d8170f1c50b89114dc8dc7c5b598cd794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272684515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b0a5965d1c1d0a6e57c2a654c4d667d66251e7a39530b429da22a19efbbec6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0272c641cc0d4e591dfd5633964da759830a3aa31bb840abf370589a98c0a9d`  
		Last Modified: Tue, 06 May 2025 00:32:18 GMT  
		Size: 143.5 MB (143512646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2dc604bdc4541046ca02edd98dfc74c7675dd0312b0110ecf6f0ac25f5e446`  
		Last Modified: Tue, 06 May 2025 00:36:52 GMT  
		Size: 80.8 MB (80843180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8523e8a2ca745028325b9597ed694775a5898e8279b352ab8c1022a409eb0b`  
		Last Modified: Tue, 06 May 2025 00:36:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745f3f2632dddf5dfd0e505f486c4255b814f94dbabb7530b89a0058eb74cf89`  
		Last Modified: Tue, 06 May 2025 00:36:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0fb2eb9b5b74641ee8bb77e1890183196c1710ea8fe72587df1e13981c45fe25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211ea21354c76c99e7140ff1ed5a1d09afebc529db914f4fc80e43001e03c682`

```dockerfile
```

-	Layers:
	-	`sha256:5e44cfd0e0f5ce5f92c944bf7764cbcd495b5f4433ba66fb47a55286e097b2d4`  
		Last Modified: Tue, 06 May 2025 00:36:50 GMT  
		Size: 7.2 MB (7178239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4979877395ef3ec1f220a70e1411687c881808768c257e7757faf6d458bdc186`  
		Last Modified: Tue, 06 May 2025 00:36:50 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d831d7cd24867b3cb7059611e06211a1261ea69fb3e9aedde056052cb9d734e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283413783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6409a4b63bf5448754a08edc01c2279e6b7dcbff301955e3390e52b9df86aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b3d490ea25347d534362b7269da337ce2723a0c555c440f6211ca588075dac`  
		Last Modified: Tue, 13 May 2025 18:48:05 GMT  
		Size: 144.3 MB (144280506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9c85f0ec6adebdc360eb709c621a2417cf8487fda32011de77636a510fe65`  
		Last Modified: Tue, 13 May 2025 19:01:28 GMT  
		Size: 86.8 MB (86800106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01781bf942a47dde10a6c7b485994ea0b7ca2e7c027cc2824fb64fe3dfd9d7c8`  
		Last Modified: Tue, 13 May 2025 19:01:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6355ec8ca83d2d19e304f4083c03f2362e7e5525602ffe0075f09aa02f3f20`  
		Last Modified: Tue, 13 May 2025 19:01:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9532a7e7c64318cfd82f94e35785bbd775b299a1b292c71ce965868f06f85a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176d394531f1f423c2fd019e3c788fcf051888607ac465090e54d0cf48024820`

```dockerfile
```

-	Layers:
	-	`sha256:0b1c8fe73e493b9393178981937b84467b5fea8e7df33dd552c5e16d1b9b0ca4`  
		Last Modified: Tue, 13 May 2025 19:01:26 GMT  
		Size: 7.2 MB (7177518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a867042e7d152e58a49a50dabfabba1dd15a390cc243043cbcc1bd7eb28fee0`  
		Last Modified: Tue, 13 May 2025 19:01:26 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:057cc6fb3949aa559c443c6476d8ce0d2d29ffa956afa1d13df5c7e1a5c71879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261622626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7c39d8b0c0e6fb673ce2d486b55659808cc01946536c94a51ab2afa9cdaa8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6625b6191194fba26629853d9de4080fe3fcd48a079cf660370c1797f2747fed`  
		Last Modified: Tue, 13 May 2025 18:09:09 GMT  
		Size: 134.7 MB (134673599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c2b2a03ac8d5ec818c2f62213d13dcaf5a296e18dd3c370fe5b16ef8d24778`  
		Last Modified: Tue, 13 May 2025 18:15:27 GMT  
		Size: 79.8 MB (79796655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a30b7e158bd4dcdd8cb0e75395e21c981dffce976045c7d46f1ac38b5bd673c`  
		Last Modified: Tue, 13 May 2025 18:15:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797fb586205874f784a67ab9d26743c35bd01220e261e052a1ae58c1e32264fa`  
		Last Modified: Tue, 13 May 2025 18:15:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:16e44501b42e8ad673d273fdf644bcdb141030c9f8db2c834715225038484458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7182507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9bffa3251e80c189fb9e50056d8805b6cfada09b69166bdf9805850e390ac2`

```dockerfile
```

-	Layers:
	-	`sha256:6e95793fcaf97be42f9d6ce37a4e181878e6a4476de8efeb09953928b9bc5e4e`  
		Last Modified: Tue, 13 May 2025 18:15:26 GMT  
		Size: 7.2 MB (7166687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600a455c313768b9332e471037df0168e3e4015e337d53b1edbb892ba091e60d`  
		Last Modified: Tue, 13 May 2025 18:15:26 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json
