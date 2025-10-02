## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:eb6d6d21c276d8b3adb0484da9dddc60476f6997c5aa86eb927319b648587f61
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a02bcd749e97583ccb9d4691042e17fc4d4f5fc67ebb36c692cf8ff750b7f992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274322024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73924631d51effad3b04a778d69763a0150a7436f46e57c7b9aff4717a97063`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacf3e20fa0bba4039a3304ae47756b3deaeba4165f463b4d66842045625c02e`  
		Last Modified: Thu, 02 Oct 2025 13:01:19 GMT  
		Size: 144.7 MB (144693595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66862a79b60c48cd62e537b7e1df4359f255ec85c1a5ebde018ff2feb669dc6`  
		Last Modified: Thu, 02 Oct 2025 08:59:25 GMT  
		Size: 81.1 MB (81146832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7eadab9fa30055fda851add4895c3073129c3641e9037945f944483cf56f17`  
		Last Modified: Thu, 02 Oct 2025 08:59:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f4937ef1ec623c97123c8be9422c5a357d6df02f8ff1705e1d8f722ae2f77`  
		Last Modified: Thu, 02 Oct 2025 08:59:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b726dd54e73f54666551ff41432e77848af7220f02fec2ecb5dc87fe65c5d94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9840738bcd9c17c2a64c89206a5de8e9baf66c69618437e4bd3105bc87851789`

```dockerfile
```

-	Layers:
	-	`sha256:a4c156fd74445bb1122cc2b87dcae24da5692e64083c5c179cdc2d97dba9c62d`  
		Last Modified: Thu, 02 Oct 2025 12:38:01 GMT  
		Size: 7.4 MB (7374890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf39c9cdc62a9cdbe1aa488254b2ba8ba615a3a0a6eaf5253234902847046f1`  
		Last Modified: Thu, 02 Oct 2025 12:38:02 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:044a16b3868a17d6b52c59ff41320e3a77b46487e4bc928c82d41e726f3c4f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272932067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f698033d5fd082f0410eebc502b1761ba5edd989f2e5819a6f84d2b73a5e005c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501398b346a9e6fffb2d8d5b84d7f3aafab159e8a6ea65796789e82453d85bc`  
		Last Modified: Thu, 02 Oct 2025 05:25:25 GMT  
		Size: 143.5 MB (143542136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2072223065a543a70e19f0dfcbc5f5ad7fd870d751d05ead363204a021b8f5`  
		Last Modified: Thu, 02 Oct 2025 02:44:03 GMT  
		Size: 81.0 MB (81029974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2decb8db38833e8937c9b723b5c1d7638b33a42675475d482a350682f55b6c`  
		Last Modified: Thu, 02 Oct 2025 02:43:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7523312d417ea8939a0d5bd0ccc75197a0e00e79faba3ae25332453de7fdf8da`  
		Last Modified: Thu, 02 Oct 2025 02:43:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6d3942d4d406a509757d654dfe75b4872bd504cc7eaf78bc2e2816db788887ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53dc728710ca0665567ba63ca34da527245cb62ff73baeea225f64fceee168a`

```dockerfile
```

-	Layers:
	-	`sha256:983d841cf8e46ca8b4133f606ce8fe7828bd687a50bc019bd2b907541b3fb523`  
		Last Modified: Thu, 02 Oct 2025 03:35:10 GMT  
		Size: 7.4 MB (7380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4efda404a2e473490b3bc4d675688a4cf29bf5388488d4cfb8a86a534247c0b`  
		Last Modified: Thu, 02 Oct 2025 03:35:11 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:54f5304e03383b5a50a7b1813b179ce606dcce6fa2a1c9761d0366fd903d1fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283686245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9718848756bb514edd2494203111bee112c6f64d7ee94fe50c33f8facb8fe02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223e84b4dc89382f6b8accf640a8d431643b298572b9a72b40d35b2ed1caeaf0`  
		Last Modified: Thu, 02 Oct 2025 08:42:50 GMT  
		Size: 144.4 MB (144372613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2507d4002cad18377f77aaea75f14e36643e0f3e6ed731a31a44afd5465dc2`  
		Last Modified: Thu, 02 Oct 2025 08:54:40 GMT  
		Size: 87.0 MB (86985825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5130d109604a1995a66ce64f66371a8773f0d8e8ddb44d696a6f6e77bdc68697`  
		Last Modified: Thu, 02 Oct 2025 08:54:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f446c0c79214e29c1bd0d14e193312c5560a0eff5cd3053954c6635dd67b925f`  
		Last Modified: Thu, 02 Oct 2025 08:54:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cc01cdd7e52c907ab0e83698d824db01951f157ea29b2cbb33e29658d930a462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3726d5281371fb3dcb46b9ad4bfb43ee5ab63afe6dc2b5033c4d702a8d7b0dcf`

```dockerfile
```

-	Layers:
	-	`sha256:91f499e89426a10d1e1380aead73dff8c81fdb0f141f552edc154175ff9f6acf`  
		Last Modified: Thu, 02 Oct 2025 09:37:07 GMT  
		Size: 7.4 MB (7380104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d66001d93e1e9cafd658ece6aeaf85affdd4ab3668135691a9f131ef7950e95`  
		Last Modified: Thu, 02 Oct 2025 09:37:08 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:aa3a2cb4de8225ddad8c819bcf4e2e4acc1716897e24b55ebde5eefa107faad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261819228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c75f73c725acf00a50b8af36202754b6fe567241628d1f260368ca9f4d6612`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285debd5ad8d815f50f89f400d98a124283c4c9c7c892230e90cf233b263c9b8`  
		Last Modified: Thu, 02 Oct 2025 04:30:03 GMT  
		Size: 134.7 MB (134724316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c778702e9f2fa8313f7569ba7fb697414229720f613d588f271cd5132ada9676`  
		Last Modified: Thu, 02 Oct 2025 04:36:06 GMT  
		Size: 80.0 MB (79956425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5beb414406cab835dcb7727a9516300e33cd0576e4a06f0f1b28589ab6a6edbf`  
		Last Modified: Thu, 02 Oct 2025 04:35:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f653fd5b4a86f0410d894f2be2fa8c81d4157f38a79dadeeb11a2b59790ad9`  
		Last Modified: Thu, 02 Oct 2025 04:35:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1c1c1271255f0d605079b4ddf8c34ca9dd301998d52e95deefd9569b28182dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4670349a41aed858abac0acb3c79e1225f09d6b775938dd8281839493d446d7`

```dockerfile
```

-	Layers:
	-	`sha256:12a320eff2ae2025c608f5494c5a79d55ada0ecee4c85704bb63d5f697ec74d9`  
		Last Modified: Thu, 02 Oct 2025 06:39:04 GMT  
		Size: 7.4 MB (7366209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cebebf0873451f98bb76b9bf9e2d52e0f9bfb9c49e0c86ee7336789dd056a714`  
		Last Modified: Thu, 02 Oct 2025 06:39:05 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
