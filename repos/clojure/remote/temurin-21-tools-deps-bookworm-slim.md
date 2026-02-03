## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:ca1c2c5042757ff144c59fe2f9d20a6d872371f99ba34512030c42a538d8d7f3
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7abee3bc13615f4defcee7ad024c93886d4aae23aa1c694058edfab4b4e764dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255733302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfdcdfefa044993ac95e4fc62763d9a7e1d4cf44b79d439a4150499a8d5c6bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:21:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:21:51 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05ce29ff1b60ba86fd0bf48eef8ba80140ffd4cae32aef820ddc1a20d214fe5`  
		Last Modified: Tue, 03 Feb 2026 03:22:30 GMT  
		Size: 157.8 MB (157826000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09025af192d23a0132b3f2b8c37453e961dcfa4eb9806e916ee5ae29d06f436e`  
		Last Modified: Tue, 03 Feb 2026 03:22:29 GMT  
		Size: 69.7 MB (69677773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ceb7c1c5a53b8cc0d4a8bbb946a70b9ba0b4374ebe953a2cd932dcb6901a8f`  
		Last Modified: Tue, 03 Feb 2026 03:22:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e43dba80abb068a072a4183a4d68f0925a306da0ab8e216a475e4e16a036a31`  
		Last Modified: Tue, 03 Feb 2026 03:22:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b75f7e82834b48f4a50a48bff05877db574edebb8ab926be5e9df53f33bc348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e04e3ecee7022ab275946e111256a74a6de0feed17cf56d657b8132e5fd11c`

```dockerfile
```

-	Layers:
	-	`sha256:c6149d8eb594c390607c18692ee0cebc298a289902970ac1d6b93fa016d74cee`  
		Last Modified: Tue, 03 Feb 2026 03:22:26 GMT  
		Size: 5.1 MB (5116504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0775303bc3dfb7462a15a18500d4a6da433063a727b7fcd44ac3244cd39fe8`  
		Last Modified: Tue, 03 Feb 2026 03:22:26 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a62d7fd4faf67311fc7504cd676d2397a94f37bf6f8fa0d9098c412e099ad846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253889158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cdf154910744779ed3d887f291c0593ef43f3a8877a46830a8ce6294a390b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:10 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9ab2f92e0555fb23dfe1cdc081e138c41514d5eaac47cedf37ad0c452b420d`  
		Last Modified: Tue, 03 Feb 2026 03:24:49 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ee12e8aa0e2fa7b61e4a0831a168befe2f27027ab65ebfbce309b3aa3073c2`  
		Last Modified: Tue, 03 Feb 2026 03:24:47 GMT  
		Size: 69.7 MB (69672711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079971f7eabc5e098d5a8c09f049ed4e6b3dce2b4877614b3d80c94702d68ae6`  
		Last Modified: Tue, 03 Feb 2026 03:24:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1062d4fc668bf294608ea62394af13bc86fde4e5494d21c8efeeeb91add0b17b`  
		Last Modified: Tue, 03 Feb 2026 03:24:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d7b5fee9a111ceb678f127cb710ee1f96dadf4d71d2051af05757fc4fe8e79fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf19ca53a8855b01451e22ecdd41b13aa90b7b449b3a3672b889dd918a3302d6`

```dockerfile
```

-	Layers:
	-	`sha256:9b54c876b1453f91bb1d2f90e451c51f3bd7f97daad451731f48674e1567fbc5`  
		Last Modified: Tue, 03 Feb 2026 03:24:45 GMT  
		Size: 5.1 MB (5122265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f0dc327e8fc83516b5604cee28ef2573e409708310e5b082a7c8126bd7c8fa`  
		Last Modified: Tue, 03 Feb 2026 03:24:45 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:737b757aa1b778515c1ab4bcf0214056df6a5904c787c11d479c6be49f74c928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265526532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69fdae0224f3a542082df839e1b9144f44ad71cfd994dcfab4ca102ec4f6f1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:47:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:47:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:47:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:47:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:47:26 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:51:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:51:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:51:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:51:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:51:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f1af9e8db4ce29cc7e415b10645fed4f03a07bd5d15711fe08be12e893108f`  
		Last Modified: Tue, 03 Feb 2026 09:48:42 GMT  
		Size: 157.9 MB (157942896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aace4ddd7f127e01a7e43fe2cfafe7f00a9d590a2a4add8e52efed33532b012`  
		Last Modified: Tue, 03 Feb 2026 09:51:54 GMT  
		Size: 75.5 MB (75513878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96301cafea6040bb7d6df7d86c0c6808b717034323c2dcba822df8dd2b85a2ab`  
		Last Modified: Tue, 03 Feb 2026 09:51:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6c0d056429e6ee2f713adfffc6a07bd3bed33ded97af0c162264f19b28a772`  
		Last Modified: Tue, 03 Feb 2026 09:51:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:10f56824dfcd5fe0d9e2210ac6246784b099a6236d367e2cf31e1c83c878d7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e94bcad77a1fda221f284cba85353818e887fe83fdf510a8d97d40c15dbc09a`

```dockerfile
```

-	Layers:
	-	`sha256:adea54d0cf343064361b0772ce7fa3d8de7f142a4eca93cbecc4e6788de5e3c2`  
		Last Modified: Tue, 03 Feb 2026 09:51:52 GMT  
		Size: 5.1 MB (5121662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98790d5e366554fe6131ec28840fe994d6f5011366feeeecf154001d8cc8cc2`  
		Last Modified: Tue, 03 Feb 2026 09:51:52 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:998b178718db248e7bf4d5a6bdf83f2982cc353728a077fbe51b9577787245fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242445386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528a2839329409a38eb1de74e96acdd97d60ccfa86104f1a5cb67ce3f6fb0d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:03:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:03:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:03:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:03:53 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:03:53 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:05:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:05:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:05:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:05:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:05:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ae753e080cc50ca20884f34f16a7a103d8cdee0bb115b2a6163947581cac7`  
		Last Modified: Tue, 03 Feb 2026 05:04:33 GMT  
		Size: 147.1 MB (147069863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5966125a6b6ee7a6303264a2198953985ff56292e3b26a0c2a06b53c3ba61dad`  
		Last Modified: Tue, 03 Feb 2026 05:05:33 GMT  
		Size: 68.5 MB (68490096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e709e838e004daadafaa75066124304c18deea21bdb32dcf23b13e47805c549`  
		Last Modified: Tue, 03 Feb 2026 05:05:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149d1aa320fafe222a7c935a4bfb2f57966048221ebc5c544d3e9b823830963`  
		Last Modified: Tue, 03 Feb 2026 05:05:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cae9c023edbb8298245fbbc616a5eb24a20ff4ef8e6ac6d8f44dba10d51bc639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c802ad502fe3e5bb3d72c10823ec043594fa16f22fc375c860791bb2a59179ea`

```dockerfile
```

-	Layers:
	-	`sha256:038fcad0a989a861c7635eac92f5d13882bdda2911d107340863b1ab79ebf740`  
		Last Modified: Tue, 03 Feb 2026 05:05:32 GMT  
		Size: 5.1 MB (5107825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ae0be19cf2a0cb6c219ccc8b8260903265eeb2a83e1611a27274083e68555c`  
		Last Modified: Tue, 03 Feb 2026 05:05:32 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
