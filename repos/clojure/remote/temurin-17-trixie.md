## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:1fe4c7f9eea9d36c8873517ebe4143b0d7a6796f0d48298f36a4574082e83b51
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

### `clojure:temurin-17-trixie` - linux; amd64

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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

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
		Last Modified: Tue, 30 Dec 2025 01:00:41 GMT  
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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce0a2b1d6c5595026848879ecbcf880c447235da88fb9da8398c745e64891991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288579883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a9dd7baf11793247d6a81efd878edafba93ab6e13800b54d271e5da7dde37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:27:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:27:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:27:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:27:14 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:57:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:57:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:57:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:57:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:57:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a185af1bf60cf57d1da0f13bf5f3a56964ffa7635cc2b99d41cd3ba11696aff`  
		Last Modified: Mon, 08 Dec 2025 23:28:59 GMT  
		Size: 144.5 MB (144525284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1be896c74e771b2d6e11daa36577f763d9e8743e8188a1d49579ce0c567d48b`  
		Last Modified: Thu, 11 Dec 2025 22:58:20 GMT  
		Size: 90.9 MB (90945080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b38e733a4223bbc092fbe4a158ba79b0c5322e3c17530e7733674a12f8dda6`  
		Last Modified: Thu, 11 Dec 2025 22:58:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6240fe52ae5f8041763e20d264295cd49aa7ced7e1f47d85e0c31793807cedb5`  
		Last Modified: Thu, 11 Dec 2025 22:58:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8f4f4143c7705f673460e5f20a9228ad377a7fb2b7066847d2f9c6f0eb15a85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5179f3390ad00573f52da2fe8940ac26242f159f29040f559c490d6dec7abc13`

```dockerfile
```

-	Layers:
	-	`sha256:f6a123c1f551884fe7de83b2e938cbbe1f5b54327ac99a1505313aba4f230863`  
		Last Modified: Fri, 12 Dec 2025 01:39:55 GMT  
		Size: 7.5 MB (7471350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5338e97e2c2f9ed7cea7e088a3d9d7121fc5be124ec0c9de29fe564027e3a9b9`  
		Last Modified: Fri, 12 Dec 2025 01:39:55 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:bab7c49da34a444079bd11caeb5e73669660ef6d05087e89ac4ab24076e3d707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270714644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb25736120f15515122ae6320b95b3c62464ca2b823114e6eddbb3c8321faa55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:34:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:34:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:34:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:34:17 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:34:17 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:34:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:34:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:34:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:34:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:34:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe4efd6cb1fe9f9256fb5ec095ce9fd2d8216620ccdc50d88e73bed4e27035`  
		Last Modified: Thu, 11 Dec 2025 22:35:26 GMT  
		Size: 134.9 MB (134859034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a4ff9d77bf8924b21c9a591115ea837713dbba4a08edec60f1b40f378b59d`  
		Last Modified: Thu, 11 Dec 2025 22:35:18 GMT  
		Size: 86.5 MB (86508661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5778a17fd6c86e638caa41030020e6597141050f99b38d0f914a8c72871e427`  
		Last Modified: Thu, 11 Dec 2025 22:35:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1422c6868f24b82f6fffd167c838082bb7ac075c202ca1cc31ab923ccd101f5`  
		Last Modified: Thu, 11 Dec 2025 22:35:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4ee0a5d90e0385de7d636771e94093702e76eabb621f3cc60eff74411119a72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446d19384d1473cdcabde95ad46cc0fbef2a3f4106f4363518bda6f36e184e48`

```dockerfile
```

-	Layers:
	-	`sha256:d86ecb351b99075f30ed7f7674d291c8a5fcd4899b7c1b70c8d0a31742521e32`  
		Last Modified: Fri, 12 Dec 2025 01:40:02 GMT  
		Size: 7.5 MB (7462853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53cc89ee5cd93c08a1442d041cc5326d08ee36259ceac41cd8b625e19ae998a2`  
		Last Modified: Fri, 12 Dec 2025 01:40:03 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
