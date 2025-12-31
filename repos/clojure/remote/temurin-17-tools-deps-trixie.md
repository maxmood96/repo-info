## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4fc7f84896321db700a3ac04b79f5e1b831b37487b8bfd4e03a0bbaf542abe3a
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:67b8df85ac6b8ead3a8bc1e1c7ad41c80d3fe2205e69de49209ec5be774fa36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279682754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aac64b3385ddf0f54c3802cc58614151b050ab814509bb955e7c68636928d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:00:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:00:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:00:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:00:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:00:43 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:01:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:01:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:01:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:01:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:01:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4192c6c2ea86fac78a9d5a737e5c8912682d2cf5252fd3fe8472c26c0062386c`  
		Last Modified: Tue, 30 Dec 2025 01:01:47 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2200cc1624e056f09463d92666690c5011261f90b05e1d4582d2dff86de32ec`  
		Last Modified: Tue, 30 Dec 2025 01:01:39 GMT  
		Size: 85.5 MB (85544204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1fe4af70885cbab5be23a1b4a68e25c5176def410fa70ac9a58f7ef3375a95`  
		Last Modified: Tue, 30 Dec 2025 01:01:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033ea5f46c30e37e50605deba602ba5e1c76b06f68f2214bcbda35d1fc3cb43e`  
		Last Modified: Tue, 30 Dec 2025 01:01:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:645fc8ba9ed91e3f7de5e6d45d1b03ae2949db7adf1e03ee161e99411a37c878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f3887ff961ae983e634362bfcc32505fb8a9fbc0ef6903e557bb8e4c2cc55e`

```dockerfile
```

-	Layers:
	-	`sha256:68e15012e6b23df83fb60eaa4ea76b0ba483e998af7a705e7e0b5c6bf0e3b614`  
		Last Modified: Tue, 30 Dec 2025 04:41:53 GMT  
		Size: 7.5 MB (7466931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e575b7f9804174eb8e1915b781384f526d06272bdc3ceb308f46ac92a51711d`  
		Last Modified: Tue, 30 Dec 2025 04:41:54 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:072b77626824eebf42c1de4cdc8969f7143f448f1d54afa01dbafc1aaea65e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278692582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91ab5057e40e1285557440ef7495b182787ca54a588f69f04184b5c69bfab4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:59:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:59:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:59:56 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:01:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:01:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:01:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:01:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:01:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe7737574531ce47a995a8039d085e29478f2b3e5a7403262cc2034e2d7a7e5`  
		Last Modified: Wed, 31 Dec 2025 02:46:14 GMT  
		Size: 143.7 MB (143679885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1160f0f3d3a7668dd50d83760be68de6a913d8a18e639a4c29b5ef64dda94331`  
		Last Modified: Tue, 30 Dec 2025 01:02:26 GMT  
		Size: 85.4 MB (85361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1087ea48a689897ade94d61db69be8595e630c729fbc4c1aa0f04554a2cbc8e1`  
		Last Modified: Tue, 30 Dec 2025 01:02:19 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f277f2b1068c5ccd66e2e463bd27eacfc122a431403ab3472d53506fc99cf1`  
		Last Modified: Tue, 30 Dec 2025 01:02:19 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1a5d0b3e023fd2e1f580a1ec4eab6a42b1955ccbe24c46e218a87eff4986d9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c6551d20f3758b1e2a9f69a170d3cee11dae7f4a2d63ae9da2244ad1638531`

```dockerfile
```

-	Layers:
	-	`sha256:c2bed94612644ce69a8c10fe7251355cb237f68d229899dbebce7a472618627b`  
		Last Modified: Tue, 30 Dec 2025 04:42:01 GMT  
		Size: 7.5 MB (7473961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f0f5ccccc80224582656aef60a8cd6818b4db18730c629636e2e0b51153c38`  
		Last Modified: Tue, 30 Dec 2025 04:42:02 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:cffe9a081f0523a8652eabbf0b81de602cb64efe89705b0ce818418f7e62d3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288579469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0e0a5d0245005fb306deb4d2a741107bd47964321fe44e4f33aaf9e335964f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:19:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:19:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:19:32 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:19:33 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:22:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:22:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:22:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:22:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:22:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec9bbe5a1b4841d627859808d06aee03b4bc59e675f245c14fd66a059d46e3`  
		Last Modified: Tue, 30 Dec 2025 05:31:37 GMT  
		Size: 144.5 MB (144525256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51a7f14ef8c990f5ee76e5ee80528a2ad03a62a56789548b475e4de86eec9b6`  
		Last Modified: Tue, 30 Dec 2025 05:23:06 GMT  
		Size: 90.9 MB (90944687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea0eef3e237a4c4ce7261ad6f2d3ff877de8abfccf889d7ab4d643126610590`  
		Last Modified: Tue, 30 Dec 2025 05:23:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938da9b512a7cc92610b106ca0f0648b489f9f25957e6ac946a83322df419193`  
		Last Modified: Tue, 30 Dec 2025 05:23:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4442d521ef18d91a3e81a9dcf6c9c6df3ed0cd8a1ee5b584ede9c130e7a2de19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd80efd26ec7453d964a22807b78bb32986b506f4307b65c6f704ed957b17138`

```dockerfile
```

-	Layers:
	-	`sha256:2ad4398babf6f1ea4fec4796e1810733da232a64ce22ab88841a89a7d7831c6d`  
		Last Modified: Tue, 30 Dec 2025 07:37:08 GMT  
		Size: 7.5 MB (7471350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c378ea6dde35a77f61d59d3f6be60d91e531048a1fcee80ca34a6e5a6b6d5585`  
		Last Modified: Tue, 30 Dec 2025 07:37:09 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:de88d63c37444407d5de0c492a954b55c93c7fcb450a603df6ad08903fd91b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274085801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e467a013c8c29fc6fbce12bf5d215d9fbf02e0f92052e862e5e6e7b1d9ddd97e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 18:39:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 18:39:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 18:39:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 18:39:46 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Sat, 13 Dec 2025 18:39:46 GMT
WORKDIR /tmp
# Sun, 14 Dec 2025 16:00:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 14 Dec 2025 16:00:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 14 Dec 2025 16:00:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 14 Dec 2025 16:00:50 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 14 Dec 2025 16:00:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed11f364842f3868a4bd6a1452b0de55321419b5214a37e282efa4a365d37af`  
		Last Modified: Mon, 15 Dec 2025 01:28:47 GMT  
		Size: 141.9 MB (141889568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234071e256c923bb99a049a992ebf3deccf1f5edf89dfbf60474e24e094c014a`  
		Last Modified: Sun, 14 Dec 2025 16:05:36 GMT  
		Size: 84.4 MB (84424056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c66502c9ab26c54a5ee1feddf21023d364b23ae9055a4551eecd019c0c7e78`  
		Last Modified: Sun, 14 Dec 2025 16:05:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c6bcc00834713556958989d53335cc9683bdd1e028656ee332484d2131d85e`  
		Last Modified: Sun, 14 Dec 2025 16:05:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:aa27dee380c5f4b44a8e0f83f29be5bc35b7528e9e417cd8170ecd588f0d3043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1116566b23eb75db510ed6f01c845dbe2b7e25d408a8cf0ec65101bb5c81ad`

```dockerfile
```

-	Layers:
	-	`sha256:4dcd5dcb3c6e0e5da0472aa9ac8619355db7874466c5af8ae8284af9208917ce`  
		Last Modified: Sun, 14 Dec 2025 16:35:52 GMT  
		Size: 7.5 MB (7452925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:774564b8a452554a552be3fccab8cd39b43590cc68737ec7ebe3937fabd3656d`  
		Last Modified: Sun, 14 Dec 2025 16:35:53 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e03bbe631d4a5b57438e6169f008fc9561a66fcd3520cc99b7331c14970666e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270714416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3629e0ececd31f298877c05b466360a07b559dd801c60695e9801ce1c1dd165`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:48:21 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:48:22 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:48:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:48:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:48:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:48:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:48:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dd69fb8ffec385e69f65bc0686e48ac1175a83475af590f110a3af664d78e1`  
		Last Modified: Tue, 30 Dec 2025 05:53:54 GMT  
		Size: 134.9 MB (134859034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b773cd33163c54bb6ef4681d6d664417a2054cec987cda675911c2692a7d54e`  
		Last Modified: Tue, 30 Dec 2025 05:49:29 GMT  
		Size: 86.5 MB (86508381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5537f731c3a9cbd13e0af3f31870fef8228813ca18e8b5b64d59af2793a42`  
		Last Modified: Tue, 30 Dec 2025 05:49:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b360f44123b30eef024bfefde5a503c41e79fe1a45fab8fac27c32b210fc67e0`  
		Last Modified: Tue, 30 Dec 2025 05:49:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fbe9099a5a260288b1f45888ef6d12891cf3453d7634308ca66ac6a9900a686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0822b798af4b201983c82481a6786f6e0e3b60bb469f38bce94d911c6a74f256`

```dockerfile
```

-	Layers:
	-	`sha256:738b5b13b6fde70b2cbdddf6f83e2fb139a9dc60ab97b2f635ef761c5a5da51d`  
		Last Modified: Tue, 30 Dec 2025 07:37:19 GMT  
		Size: 7.5 MB (7462853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8340c2e436aa0f3b9e7f26b64b1270a06930dbe89a70236a335744b2edda4ec2`  
		Last Modified: Tue, 30 Dec 2025 07:37:19 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
