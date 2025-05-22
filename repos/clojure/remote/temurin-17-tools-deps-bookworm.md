## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:30c4728c19fe9c64330b87aff0a3d5a24eeaa28c6cd2ab47eb43c33088fb28c6
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3eb4a55f38783b1e706f8cf25cdc20b2bb2d3f4339f6f41342357a80d1ed3ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274119502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3c94799da4d30efa7bb0d31f70596a080f044571a42105e0488038ee110f64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b5a3c25542e0d88809ba04c06354f605617015d471bc60c8bc0084925084a9`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 144.6 MB (144634954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc6d0f46340222fb1f03d0033cd3e5b49275ea5e815876c126460e8c5a56620`  
		Last Modified: Wed, 21 May 2025 23:33:05 GMT  
		Size: 81.0 MB (80995262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe129bdb259639e11493b8217f0399cb0f10bc7038f5dc0c531eff363347dfd7`  
		Last Modified: Wed, 21 May 2025 23:33:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9721aa43dad86c03b65eaee10b5e9f6318a2feda8b86e816fbb57bcbaefa44`  
		Last Modified: Wed, 21 May 2025 23:33:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b814b6613dbbc129d0bafccd392619edbb66d5c0199eed5e9777e050870c36a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acd6454cd84750d5fbd54a2b65af822783b395cdea5679024c260da15913051`

```dockerfile
```

-	Layers:
	-	`sha256:24a00c32494f08bbad62c780ac9013859ec79df5af0ff22765ff49487f527d40`  
		Last Modified: Wed, 21 May 2025 23:33:04 GMT  
		Size: 7.2 MB (7218522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f26ec7d50bb902601975aca3b3505bfcb424366e7c8a1cee870d952e324576b2`  
		Last Modified: Wed, 21 May 2025 23:33:03 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a83366ff27db3150c169c0982b8bcb0ca4e9889fe406d452776bf17e57bf1265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261608743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d8dd420f55a66fda1e0cd6cb127e237b2de95c2cc3deec45e03afed0c3ed0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9c813a7e65d2034deaf8d72553c6f77f9d06392049a6e567e512b1efb6e191`  
		Last Modified: Thu, 22 May 2025 03:49:42 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02bb9a89c9e3e9abc9c0fe1327dd52b37a7ddb8d4516484bf7851576e8768d`  
		Last Modified: Thu, 22 May 2025 03:53:35 GMT  
		Size: 79.8 MB (79790300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9766fe771a9d34f88be1dc6ca7c1bfca000fdb29adbc5e4c95f7fce647fb5f`  
		Last Modified: Thu, 22 May 2025 03:53:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072c17388bba2c6f43263e0946a08a40ed5a367b51bd33d579d58de251a4cc7`  
		Last Modified: Thu, 22 May 2025 03:53:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d2ea50ec47c267969407a4157859bd51af217fb29e9a88fafd94a0c81b455319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1366308761a894b59d1ce5ab3cbb1e0be80e90de0b189328e93303ac656a0cf`

```dockerfile
```

-	Layers:
	-	`sha256:aba409aa8d5f0e2d1b06c69fc6a0850119b369ca65008fddbdf4c621731843da`  
		Last Modified: Thu, 22 May 2025 03:53:34 GMT  
		Size: 7.2 MB (7212733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088e24e0f1ccc0196b91f06a6552b0c4f64e77c9c21bffa48c6a7de2962ec0a7`  
		Last Modified: Thu, 22 May 2025 03:53:33 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
