## `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:8b24600ddfaaada15a4d30817816e37c0615526aa172ee10decfbd2fd7afbaa2
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; amd64

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

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
		Last Modified: Sun, 05 Oct 2025 10:40:01 GMT  
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fa892e42e8101d9f9961b6a8681a89aa325ec7f15adffc8439dfd49109e2e6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261818655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acede584f06e6ce66a23a3f53001c78d92df1db6e1d7d5261e351293e6ef3dc9`
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
	-	`sha256:1f3afa8bb81ce30bcf13eb0db5dbd6d2b5add61080756bc490e8e5412b5d8260`  
		Last Modified: Thu, 09 Oct 2025 23:08:30 GMT  
		Size: 134.7 MB (134723624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa8c44b70e05464954399a13069cc93c9310bd31a40a0e50376ea20db89174`  
		Last Modified: Thu, 09 Oct 2025 23:14:21 GMT  
		Size: 80.0 MB (79956545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54a9b659d7b6b86fb1a86d7a709880f72dc18d00a87406a7ad8ccc05f087491`  
		Last Modified: Thu, 09 Oct 2025 23:14:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668704c839bb49aa0df365047ddef5c2467945903c874806c774cf0f41c15244`  
		Last Modified: Thu, 09 Oct 2025 23:14:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1ce04a443e15874923b448dde2edbec12cacc9d4ea00258799262767e0d10efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea6a3f8492569151287ec59a26407862e08d4607a6ade807be5ba7f3f88e070`

```dockerfile
```

-	Layers:
	-	`sha256:97de74b909dbc06e400809c6cd0bb4e6c6a4f4f80981d2ede6f9b948b6c9e005`  
		Last Modified: Fri, 10 Oct 2025 00:37:11 GMT  
		Size: 7.4 MB (7366209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ad56b4b0ae2c5847eb87da3652ce00182701e6e185400b2295ba38f52f6217`  
		Last Modified: Fri, 10 Oct 2025 00:37:12 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
