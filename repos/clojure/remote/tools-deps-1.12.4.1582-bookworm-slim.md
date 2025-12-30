## `clojure:tools-deps-1.12.4.1582-bookworm-slim`

```console
$ docker pull clojure@sha256:bc0b0251e60ab2de9f1faf3a6b1c298ff490bed63dc415bfaa2a044f308057c9
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

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0c04ede195bb181a541883b2108a3e93c36d7c32663f49df558fb7525b76bd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189952035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fda3579f215ceb8a8251cf1d8f1cf17bf8aad9f4790a292de60e027500bf99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:06:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:06:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:06:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:06:23 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:06:23 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:08:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:08:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:08:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:08:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:08:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cadd1d04c25c1af3140f14a1cdfc3b2540614c4abc9e48a10b252684db2565f`  
		Last Modified: Tue, 30 Dec 2025 01:07:12 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7562097f5d4f8fd0b8a457f2c3a8b2ed7bd1cc5495578fb9f85210013f538c6`  
		Last Modified: Tue, 30 Dec 2025 01:08:40 GMT  
		Size: 69.7 MB (69677275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d03e72009bb0b4df533f28cb59ef884c64b4e557ab98f98d54c075f338755`  
		Last Modified: Tue, 30 Dec 2025 01:08:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806f8f8ca3f6d0f5f32651534f996c9e2dd7b1693159cd1e94b4b6d4d5762de0`  
		Last Modified: Tue, 30 Dec 2025 01:08:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c42da7d6e9717541d0c3430dea0d80c382cf5e703a5d1c4e602e5fdfa80e8d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5080474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fe302dceb16789aa48564a3cdba4803e11ff1be58a41303b8b4a56b382afe5`

```dockerfile
```

-	Layers:
	-	`sha256:18baacfa1c89cf6b1ebeaf0f4ea9d2d71a5672376fd9ab9514a52ac7dfb29fe2`  
		Last Modified: Tue, 30 Dec 2025 04:46:06 GMT  
		Size: 5.1 MB (5064748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66397cbb344cb59b28dec0313c7ed2a6005edc936a63f0059b55442152bda337`  
		Last Modified: Tue, 30 Dec 2025 04:46:07 GMT  
		Size: 15.7 KB (15726 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edd91b4aeddf65193ce033f6b60a1bc40e63265759ff47db10ee2fb1f272365e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188714450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b79dd5314ef633e6fb0f415d58f127d61addcfbfedce44333f0153695811004`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:09:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:09:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:09:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:09:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:09:22 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:09:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:09:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09bb079260f4d2b176b04fe8b5f3cde9a368b6541c1f34cf666fe66c2d9f10`  
		Last Modified: Tue, 30 Dec 2025 01:10:15 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68774afc34a000b273ee3b97012223bb8a8456b898d0907abbcc2c40f2406753`  
		Last Modified: Tue, 30 Dec 2025 01:10:15 GMT  
		Size: 69.6 MB (69558688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005c0f752c4bc96dd5afef0bf3a1792c8c20c614903b42ed65a97bde900ba3e6`  
		Last Modified: Tue, 30 Dec 2025 01:10:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4922df82b0468dbaeb805adf79d38db8e754816eeeecbd0ee228739229bd5b`  
		Last Modified: Tue, 30 Dec 2025 01:10:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b4527ef3fc09971b1bb331e5a2d6f2ed7313a3dac8bbc6cccca0fe256eefc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed7960d3997665aedae683e4f7821a725d633d87f088f0b52e75b9a22cbae0`

```dockerfile
```

-	Layers:
	-	`sha256:03f9c5ad86ac7aa9bcf53192c72ff0de069b0fe7ef689ac86fb48f135ec8e336`  
		Last Modified: Tue, 30 Dec 2025 01:37:25 GMT  
		Size: 5.1 MB (5070530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:869383de83db43ac06e81eabf95baeb6f3923c086b2ba7ef59ae2f4a6994256d`  
		Last Modified: Tue, 30 Dec 2025 01:37:26 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:21fc4ccedeb4ce310e878ed54d4e93370b1ba0e4d8fc0b9b6053c1116b6cf7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199190741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24093edbe8c4e98f35ebd14ad685d7116a9157c09531f5d9a58e6c547182cbd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:24:10 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:24:11 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:05:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:05:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:05:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:05:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:05:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34f3bc4e2e28ed95aba8ec4d91b1f2ea595dcea02126d32ce2f47b884268f0`  
		Last Modified: Tue, 09 Dec 2025 16:25:49 GMT  
		Size: 91.6 MB (91610770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124559ba349c73d2192f3a5269593fe3cbabed4d5c8b8b4570ae22c0788a607e`  
		Last Modified: Thu, 11 Dec 2025 23:06:36 GMT  
		Size: 75.5 MB (75510084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88719ed04b07676fdd490ba81bc669189bd339f35b5862fccf01c1307e37d2b6`  
		Last Modified: Thu, 11 Dec 2025 23:06:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415d426b5e137dc995e3662948282829bf0e64fee38ab6333b6a2f060da6526e`  
		Last Modified: Thu, 11 Dec 2025 23:06:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:001a6392c23f83e713751dd6b2c9fefae1ba789986eb25178976a515ad180e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27637350a240f7b44f4e35ea41b264ced3cb84c829c812a4c63b2880ce379744`

```dockerfile
```

-	Layers:
	-	`sha256:46da68e6487af437ec45d4571cd74d93e14f583052c46eed50a0c23cf4cbe1a4`  
		Last Modified: Fri, 12 Dec 2025 01:44:17 GMT  
		Size: 5.1 MB (5071216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528df463bbf72ecec11118d1c2754442d595712733f1a96e4b948295bee2239e`  
		Last Modified: Fri, 12 Dec 2025 01:44:18 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4f0edc6d748ae208f03f930f936b6f097a1518f74f6f58cd28dc510c02f3c9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183583986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23ecd879dff128370e67d7781428d125092eb2ad20d631e4454e82d715e7e04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:06:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:06:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:06:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:06:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:06:36 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:08:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:08:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:08:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:08:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:08:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206a49bac65bd4add6dab33ac10d239d5efb1670d78480bf889aa12ab7137521`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 88.2 MB (88210732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3941ee89ca5c6270a47a079ba00fc6175cdfa80407822c530811808131740738`  
		Last Modified: Tue, 30 Dec 2025 02:08:41 GMT  
		Size: 68.5 MB (68487816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ad6b1e11c6b04f1e50c9f7dcdc1e1a64c723bd1cf2c47b004ce1b4a4015cb`  
		Last Modified: Tue, 30 Dec 2025 02:08:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e5767147aa06df82abafe615563eaa2306b64acc12fdd9abb5a698a8ad18a`  
		Last Modified: Tue, 30 Dec 2025 02:08:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b3815eb70183f9f226d6dbb683d2000c0fd353b03c8466af29bab8c011ba927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bbb7eab8033d0f2e150858f93b803d6896451c27bff4a8c2d739cfb0c40ef5`

```dockerfile
```

-	Layers:
	-	`sha256:cbf9c48b4f0aa7703a68d40803a72a027698bc208ef06674e4e7e39207f98cfe`  
		Last Modified: Tue, 30 Dec 2025 04:46:19 GMT  
		Size: 5.1 MB (5058617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbae1a90cd63d586107b6167ddcd524989466c796c83b5e6ef9db45d0f3ab19b`  
		Last Modified: Tue, 30 Dec 2025 04:46:24 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
