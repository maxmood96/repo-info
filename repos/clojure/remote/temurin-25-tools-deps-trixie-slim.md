## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:238d88cfb58cc75dc908e45beefd98b53cc1877529bf36783ef9a7682fd0f70c
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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:306b4783409ca2500a64cc96824f4fbea4fd15b949d047b6e466fa8be5b607c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193805545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718530500b921b51321603884ec88fafad587bfd46dd6c1513fd92cd996df964`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a8677d0d94f687060f7ef369f37a2ad8ed92020138745a8be4b0c01b89bca0`  
		Last Modified: Fri, 26 Sep 2025 17:59:42 GMT  
		Size: 92.0 MB (92036038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857ebbcebc4a5fbe755d9706526981da96c5b7c6da1bd6bfd6b15c1b94328949`  
		Last Modified: Fri, 26 Sep 2025 17:59:31 GMT  
		Size: 72.0 MB (71994972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb3d7bf3b4eed96307cfe8616b892ca6757eb3b0ccf38611782862a8c71a190`  
		Last Modified: Fri, 26 Sep 2025 17:59:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a188e59017697f74e34eeb7d9020dc3920767222b2cb0171a1a21ef12631ed5`  
		Last Modified: Fri, 26 Sep 2025 17:59:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d546ef8b33eaf501700d7fb6b5b348e135f268eff4b6b108379dd1e3111c6000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f193cad6c8d41229961a89c116349212389a944a9b03468b300156d69b656f`

```dockerfile
```

-	Layers:
	-	`sha256:855d586e9ad527ab4b4e257f28aa11faa9a42b9c9facccb488e7742861303a45`  
		Last Modified: Fri, 26 Sep 2025 18:45:43 GMT  
		Size: 5.2 MB (5207451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30e61a3c93eaa6b54ab06b032edba47fc5847fdcd5fc4c0916e42f3df1565783`  
		Last Modified: Fri, 26 Sep 2025 18:45:44 GMT  
		Size: 16.5 KB (16535 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e4276a2cd6e38982aaab41a462720da84c0a1018cf29d61cbbe6f5e7aa2b0909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192991323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e280598e044306cb152416f7d01c8b9f3263909e6e8ad1d6e4d2bf6dd31e52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3d1921eb8bb8ae28670d43eadeb2eaa7bcb7a1dc1a01aa7e36b67ed50fb8bc`  
		Last Modified: Fri, 26 Sep 2025 20:04:13 GMT  
		Size: 91.0 MB (91045231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e8b4847d81055e998e82c7c456e039a7120a37f1f856a4494ba853b3da7956`  
		Last Modified: Fri, 26 Sep 2025 17:57:20 GMT  
		Size: 71.8 MB (71808420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e97faf0c84d3755ca8e190bfa210c21bde7843f36d9450d1dd98abffdff3945`  
		Last Modified: Fri, 26 Sep 2025 17:57:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bf229c9f7c328cedf7c5057b0714122ff4456cb4a1ed497801885a43febcfe`  
		Last Modified: Fri, 26 Sep 2025 17:57:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d53afda88159215c371b68253a1d728e488e873c031e18286c31e0a4b387929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d92589337b388b73c05ef2c57ef7662791b78b022d5b997e8ffec4ae3694ec`

```dockerfile
```

-	Layers:
	-	`sha256:5c8191e11e68097beb927ddf46f5b09f78cd5ae135cbce8b2af2a7e5c0afb872`  
		Last Modified: Fri, 26 Sep 2025 18:45:48 GMT  
		Size: 5.2 MB (5213241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d84c61484d049f8c75c42ae92dcb906d9396fcd4c7c285b67e887813ae0ef5d`  
		Last Modified: Fri, 26 Sep 2025 18:45:49 GMT  
		Size: 16.7 KB (16678 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:101f4c3f98b0d6a99894482d7d1d2b0c2456759f5bc34e040fea7f7365ee5176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202592046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345fcbc3d9205ce3dd5c2ddedb3d27187de51f1a3e7a3319cb552f95bc2872f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ad67c343d5231e272ec612fd96b09c7e9b774f451f836f7c87a590c3029c9`  
		Last Modified: Fri, 26 Sep 2025 18:37:23 GMT  
		Size: 91.6 MB (91601770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b458d864dba7099b13471af39b762d606ba2c99fe24f133986c73ce1ae47eff`  
		Last Modified: Fri, 26 Sep 2025 18:44:16 GMT  
		Size: 77.4 MB (77394882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a6ce86624e9b5797311b107df14d8b99d79e53b182ebdc88c8ae60f527af31`  
		Last Modified: Fri, 26 Sep 2025 18:43:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdb53f7bf20551a3aee0c718fac92948cda0e3cbddf9b2588569464aa237082`  
		Last Modified: Fri, 26 Sep 2025 18:43:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87c13e2874d171e38aa5cc635c322b8d180791edd9693b07050154dbddacf442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e1563e31f339af57ef1ccf343c682089c90a17f48c70a03cd9cb8b8a1cad24`

```dockerfile
```

-	Layers:
	-	`sha256:5a1acf7766a756e0182aab7135671caeecab2b6e02160ca1238b00b4d5ffb66b`  
		Last Modified: Fri, 26 Sep 2025 21:42:25 GMT  
		Size: 5.2 MB (5213132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbca571025a366cbd607648642a7492851ef1971abd9646b61f7555e287b9b5f`  
		Last Modified: Fri, 26 Sep 2025 21:42:26 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0e2dffb54af2178ce5613621b4747e39ef3bb4de7ca77feb7f4885b8884dd1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190994348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7208ec972999d7f00ecc9bfb185df2a66ffe74bf4711a3f2d668fccee740c85d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c330f9293bcb88de9ff4c589e69ff241f08b3844536781fc13cee42ceaa7c8`  
		Last Modified: Fri, 26 Sep 2025 19:35:09 GMT  
		Size: 88.2 MB (88206464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abd3ab0eb7a9fd1209d50e6868bfc2721fbde8d396c60138aecf59c7d4f646f`  
		Last Modified: Fri, 26 Sep 2025 19:45:26 GMT  
		Size: 73.0 MB (72953935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecbffa5ec28f90d048947fcf12f47dfe9a3e760d492a932579ee95056210661`  
		Last Modified: Fri, 26 Sep 2025 19:45:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d645f83eb8670787e94a09b5638d22b2d119d4bc6f99e81f7b4dbc9e88da88`  
		Last Modified: Fri, 26 Sep 2025 19:45:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8504f478086c3a85bfa06008ae681c675d42fcac29c4cafda111f6b78c991441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637abc591e476702bbef1678eb793cb11f9e9462c0141e02577bd19f73546b6`

```dockerfile
```

-	Layers:
	-	`sha256:5827c4c93bcc5b888b00a7c09ed8ff0f5eaa4671878d9fe2c9e0fcf81fd09be7`  
		Last Modified: Fri, 26 Sep 2025 21:42:30 GMT  
		Size: 5.2 MB (5205923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f5967069ec90477de8c90eec13be7309edcaa3915f8eb8db6e9cdcb888fcc82`  
		Last Modified: Fri, 26 Sep 2025 21:42:31 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json
