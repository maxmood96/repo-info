## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:3e2ae5d2cda7c465e899a08f38ae5b1759769671c3f0d4ca28b71af201a3b101
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:eba499eae5f0bacba4399db4f533cd58590f2c401c2acc74eb39e77b0d3a12e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292705921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c6874eba6374fed4580a0f1878d0e46f0c90f0d269deb9b8d85af25f9ffbd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:47:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:50 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:50 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:07 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759c5af7cd09aa775ee3dcf5cad452afeb0d6d664db887adaf8d1ab2e5569bf8`  
		Last Modified: Mon, 02 Mar 2026 19:48:31 GMT  
		Size: 157.9 MB (157857068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1879c7a8d8cd033e3e8cafebe482873ccca03adc69462edb2c33c927015a91d5`  
		Last Modified: Mon, 02 Mar 2026 19:48:30 GMT  
		Size: 85.6 MB (85554687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e9bde9141dbc604d046c8291c5e4960af5c75752a50655ad4e7f3ad271d4f5`  
		Last Modified: Mon, 02 Mar 2026 19:48:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e09eca37eeabdccea8dc5e37d0e9fa6a6cc1441e15d82c273902dc1335928`  
		Last Modified: Mon, 02 Mar 2026 19:48:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:446d2da01205f6bf189e8d37288fbefe96765dda65574975953c04897727df8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b105ba583579516e984ef24d69101bb01aeedcaab700ea5a79d2c5604b4a1bb`

```dockerfile
```

-	Layers:
	-	`sha256:42d3f8cf8aded334d8de2120364f8f259a05850d5a59dfaeb39b740c7c6dc424`  
		Last Modified: Mon, 02 Mar 2026 19:48:27 GMT  
		Size: 7.5 MB (7472445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0675f42c5b8c948aae9c99a2ba10ae3004811c6b5b785bab2d0b5a5650fa7fdc`  
		Last Modified: Mon, 02 Mar 2026 19:48:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ed67f5b72726178901aebf82faf745233baecd8954582e09ee6168a2417103c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291164687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c8a7367a130d6df67c59644c285aa6e8acce373da6bee223096a08f98fee7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:47:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:41 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:41 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:00 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036960f838f6b1c542c22cf95d7306b16bce102c9a9ef7c37043868733c1ec4a`  
		Last Modified: Mon, 02 Mar 2026 19:48:26 GMT  
		Size: 156.1 MB (156133016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a8c180e0bbe93b18f0e18f1e7e40ae08e733f536a40c13558c2b6629f5b81`  
		Last Modified: Mon, 02 Mar 2026 19:48:24 GMT  
		Size: 85.4 MB (85378460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13d0aaf6ff1123ce04f1470685642c57d166ca71564a86d262471968ae3b620`  
		Last Modified: Mon, 02 Mar 2026 19:48:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa047b2498642951b7b7eeb5120ea73fe568b3e29dc6a06635649d6e2e997d6`  
		Last Modified: Mon, 02 Mar 2026 19:48:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:18f1bd35b2a168f2134abbea294d64d1b9745882b6a8ed7a430f0c5322cb4599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f6ab9a5792c7a03cbd77845675ea9132da43c1a3055fb420e04609014c7b57`

```dockerfile
```

-	Layers:
	-	`sha256:47c7c373bfb58bce0d1c375ad0bf5599eb37bc3d3975e9f12281d2b5b6f08ddd`  
		Last Modified: Mon, 02 Mar 2026 19:48:20 GMT  
		Size: 7.5 MB (7479475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf7cea660e0e6c1f88d79d12a8f0c1e4a0ee3386f5fbeb22b34a5106df12ce1`  
		Last Modified: Mon, 02 Mar 2026 19:48:20 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:14b101529edfd34d56239262bfacb259645feae8df2ab679bf4ae990363741f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302065044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a305ddae6d218221a0672871f0f5730bff77477b76ced48fb372fdf1bcca83e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 20:05:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 20:05:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 20:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 20:05:27 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 20:05:27 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 20:06:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 20:06:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 20:06:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 20:06:34 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 20:06:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a40052fd07e1a3800ffdda0981fe2bc6858a3163f7d39a8a091c4933eabf99`  
		Last Modified: Mon, 02 Mar 2026 20:07:21 GMT  
		Size: 158.0 MB (157977535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14acd2dd3f5f0ef4d3bffd78320efbeb575a4f7364bae22827743abae6dafb73`  
		Last Modified: Mon, 02 Mar 2026 20:07:20 GMT  
		Size: 91.0 MB (90974205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a9b357bd08cf593fb5b98a6cd38ad9af89226775a767317067f97a7a903a99`  
		Last Modified: Mon, 02 Mar 2026 20:07:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2559158ff14677a9050fc72afe26227a31d011979963b69e00247a80e9beef3`  
		Last Modified: Mon, 02 Mar 2026 20:07:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c3191833eba33f6efdccea0c4de19f1beda2f5574681e595c239791b4c5d82db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2064605b47af2738be8821604bed66681297f29ce0c9b33cba82eb53ab5b4c`

```dockerfile
```

-	Layers:
	-	`sha256:4d89f931aae9b3879fedf09db21c77ff93abf346ee9dd0a3a803d00b66129c90`  
		Last Modified: Mon, 02 Mar 2026 20:07:16 GMT  
		Size: 7.5 MB (7476866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff5c5fab137809f837fa819b0a3e976f8764033e55d730dff289602e9f9ef9d6`  
		Last Modified: Mon, 02 Mar 2026 20:07:16 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d0052c664fbf97f07169285e77fe21a9530c75c9af44b5e3ffd9597062a12143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289434722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb58029fefb2c062eb59ed1033a854a4c6d947146fb3ccbd939f0913e49f58a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:14:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:14:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:14:59 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Wed, 04 Mar 2026 11:14:59 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 11:17:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 11:17:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 11:17:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 11:17:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 11:17:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb9c79161005e6b84d0763b0f118c07cedf15f1b6ee06d958a2a83ad03907d3`  
		Last Modified: Wed, 04 Mar 2026 11:23:14 GMT  
		Size: 157.2 MB (157216889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7307b3b20b3a55db8c7968b6249873f1aca5efd60334695ed2038110c7b3e27`  
		Last Modified: Wed, 04 Mar 2026 11:23:03 GMT  
		Size: 84.4 MB (84439852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d4ab3872fc67dbe43a18163a381cf3091428c74ecfa20bd2da64a8675a38b`  
		Last Modified: Wed, 04 Mar 2026 11:22:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458576d305a181e20e622df93b231769264166d82bf3d3f6c824a81c14299e03`  
		Last Modified: Wed, 04 Mar 2026 11:22:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f9956efd0c40a16f65d6c9790e9c9c908f2d5093b3b04ff525c14f4d2670720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941da767d2e3b6ff8a6b4ea4a54bdc41de7d2e706364bcc902c3ea05913a045b`

```dockerfile
```

-	Layers:
	-	`sha256:17338121e0697a258f04a7ecd17e33f1f8541c148f3e7794584d5fc6a79a5e12`  
		Last Modified: Wed, 04 Mar 2026 11:22:41 GMT  
		Size: 7.5 MB (7460360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a00d93dde3e1e5d1368c625c2c17854850c68409e1e3720890ffa093f60e604`  
		Last Modified: Wed, 04 Mar 2026 11:22:38 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f2f6b2c05d1b5096b58971fff0221f850e6cf4940849001dedc936c0a7ccf472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282991800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290010eb02edca15537d1fd160c4ab1c0587c335faea18d13efd74f5a3888449`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:48:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:16 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:16 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:34 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65684af661d610863cd20ad8456569899b56cd9313c24997ad023fabf39d39e5`  
		Last Modified: Mon, 02 Mar 2026 19:49:11 GMT  
		Size: 147.1 MB (147105304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348d2ff66b3ed8b98dc544226dd412450d2bc40e3958339bf91c527cb6bad740`  
		Last Modified: Mon, 02 Mar 2026 19:49:10 GMT  
		Size: 86.5 MB (86530918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5680421ac61ea28957f18aa4cea37e01654e498eba76574a546e152153b2c341`  
		Last Modified: Mon, 02 Mar 2026 19:49:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516a1cd8e90fd5c00e73efa136c585633cf3b908916b135bb27ac18b06068045`  
		Last Modified: Mon, 02 Mar 2026 19:49:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:da0570e1c243f8b2d3c21579e79e74ec940292cb838a8adf75667eefa2d10c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39d1f8111f0892151d53da311ebe0d9739a5b85aafba3e8992286004f7e662b`

```dockerfile
```

-	Layers:
	-	`sha256:4a56adcfc2c5e1f4466f2acc2211822b95d29503a718a5cd3aee2ea1634008fb`  
		Last Modified: Mon, 02 Mar 2026 19:49:06 GMT  
		Size: 7.5 MB (7468367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108e0b3efdf41ec2d65b652cc9a73a281b2019ecde41b63aa66505fcf7c97763`  
		Last Modified: Mon, 02 Mar 2026 19:49:05 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
