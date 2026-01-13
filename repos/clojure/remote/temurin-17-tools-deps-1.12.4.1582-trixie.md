## `clojure:temurin-17-tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:de8a387c345ba47a2f156d312aaa473d6ee55719eadb8afaa14a8d0659174d22
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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; amd64

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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:86f8146d2e01ee383bd6b377c29ce9a6ab4c9458cc80d61b7237bbf0d0856e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274085747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d966d9c09d600be3ca31b96547dcc51fa639b079b6a1578d256e51af28846a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:28:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:28:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:28:31 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 06:28:31 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:43:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 06:43:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 06:43:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:43:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:43:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84137287e78b3f369929e5abc1e6ea708f5c823ab4a3f6ddfafc4335289f5a85`  
		Last Modified: Thu, 01 Jan 2026 07:09:39 GMT  
		Size: 141.9 MB (141889568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2608f484a88cf2b41c5ac45bcdf6d3677bfddbcb2c786c407abb3c6da4ccc1a4`  
		Last Modified: Thu, 01 Jan 2026 06:48:38 GMT  
		Size: 84.4 MB (84423985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2330be42cc0e1c84411574e5559c5ee864268f7c2803ed41a11e074c5724cc23`  
		Last Modified: Thu, 01 Jan 2026 06:48:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95763ecb571a2d2b763c2dc2ee12d735f043cd1b1e0cbe4e9d5183e31f9708be`  
		Last Modified: Thu, 01 Jan 2026 06:48:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d419860cf53d3e4528a964baef45da3426d53496110e5810315062bb9e0ed518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c692e0b6e75397e81446a2aaa3ca7ca8b52a6ee172f5bf9f0554a41c4d6787e`

```dockerfile
```

-	Layers:
	-	`sha256:1b353703cbf097c86bda64ee499a2fe02033a987eb2416ccac7550d1449d1829`  
		Last Modified: Thu, 01 Jan 2026 07:36:02 GMT  
		Size: 7.5 MB (7452925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3785a0050307df368a9cd3ac290758867a3092c4844e242566f8c18fbc2ee4fa`  
		Last Modified: Thu, 01 Jan 2026 07:36:03 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:9637f8b25aef38fdd5eacf19cb842e87d7f2c2d38a61585657d88d9f7ebf3ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270717824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6325d6d8b27ad414f04b86a363d84a80f61f84ad51d8a73930de0943e0265c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:04:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:04:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:57 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:04:57 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:05:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:05:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:05:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:05:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:05:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fe2535727ccf04bb30c79a01756c8f1503b4d27d2088b08fbc95a336d9c0bd`  
		Last Modified: Tue, 13 Jan 2026 03:06:14 GMT  
		Size: 134.9 MB (134859046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3173a43af7ec9a36750e75a4febf98a667d2c1af831256b710cfed222683a9`  
		Last Modified: Tue, 13 Jan 2026 03:05:55 GMT  
		Size: 86.5 MB (86509037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abd1278745a51ada6d12c722fbca44415ac3fb270de50ee49b53b81b2ead725`  
		Last Modified: Tue, 13 Jan 2026 03:05:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed84d5480f32a12abbe0639fa5966c4a9f9db6f184ad35606c35713996bd6050`  
		Last Modified: Tue, 13 Jan 2026 03:05:49 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9dc95c060322e4d082b0e9117d7efba81851e6bdd316a65663520e1db4ea53a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35e9304f139f2e230f9b182e5f842c2f8983e661057d1aa13228c53d61f4813`

```dockerfile
```

-	Layers:
	-	`sha256:f035f41d55e45a3b6814500910a989463b27f33fa5439bd0d4e765ac7a3b3f46`  
		Last Modified: Tue, 13 Jan 2026 04:38:24 GMT  
		Size: 7.5 MB (7463748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108ae01f2f505a561172c6a0ceb5364851552d8e07ba3a45a3ed2a3150da479a`  
		Last Modified: Tue, 13 Jan 2026 04:38:25 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
