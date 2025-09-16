## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:bb653be182d875a6cd40c694461964bce7e2a124f318867f129fd3427b42752c
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:875b8ea015a4da6043bfa22f95cf573c51dbbf23951f1034f056e93f810f2937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246450580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d0dc486f2e0bff3634f01ab8d10f145ba149f06ad745b50532ae15a24d0b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a443541641ab29489e7ce9216bea390b0a73347a436350c85a6eb1e504e7568`  
		Last Modified: Tue, 16 Sep 2025 19:34:42 GMT  
		Size: 144.7 MB (144693569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ed62d894e79c5e756fd16dd7e00adafcbb8b89c29282c656f634f581123670`  
		Last Modified: Mon, 15 Sep 2025 23:27:17 GMT  
		Size: 72.0 MB (71982475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e5213e2b2d489970b3ce46d6eb129ce900c1103ebbe971e0fb76dc7fd561b9`  
		Last Modified: Mon, 15 Sep 2025 23:27:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c9d046139f2dc702691d1b339c3776ef3a5a12a36b9ad3d6c6e386fe736219`  
		Last Modified: Mon, 15 Sep 2025 23:27:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d11b690548d9b7d3dfb61fb592d1d7ac22cf33779a1fac9329fa7cf923f50bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2bce28e47f8caa97d8ec5fc7f1eb72e81f0b134945fe2477a8227c136252dc`

```dockerfile
```

-	Layers:
	-	`sha256:b3ffd8fd492390c00b7eded0b5cc85bf2c1ea3579741c31acb0c881ae37463b2`  
		Last Modified: Tue, 16 Sep 2025 00:41:15 GMT  
		Size: 5.3 MB (5256113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d003257a3b0804504671f2c12dcc30be0e9664832ed9e472dafcb14354bea88`  
		Last Modified: Tue, 16 Sep 2025 00:41:15 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dce8c92d98d028058f25ebfdee9758d3d5ef4895ff2bbd5098ae3db2e5e43c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245483821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1ea253c25886fa632a243eb9e2b564d30fe0327a7c183cf08b68d79a8249a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3cc6750f5b8e0e444e9b04801dc21538ec361953ddc39c639b2a3f1b9f123d`  
		Last Modified: Mon, 15 Sep 2025 23:27:09 GMT  
		Size: 143.5 MB (143542107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360cdcbd6ea6c1691bba415c2dcab28679844060565ac3824e9483f727c7d079`  
		Last Modified: Mon, 15 Sep 2025 23:27:39 GMT  
		Size: 71.8 MB (71804044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44fe4e062f945e7836bf7bc665fedec214631b8a3777fda4fc081ed1e9cf6dc`  
		Last Modified: Mon, 15 Sep 2025 23:27:35 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995792a52e9a84e5b68c6babdbeea5a39a54a4d0a745fcd355c1251b37c5e4c4`  
		Last Modified: Mon, 15 Sep 2025 23:27:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46e384c64cde4a0415f9fbaef4e03f4e19a7bf76f844a80aa2ed9e874fdb98bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674382acc91df9950ff4742c40a5b9a601fd459530b34c1fe88c310a193b56ee`

```dockerfile
```

-	Layers:
	-	`sha256:73eaec2db35e919e5475c04773f49f5a9414e53508c3f8df07bd3c906cae0266`  
		Last Modified: Tue, 16 Sep 2025 00:41:25 GMT  
		Size: 5.3 MB (5261882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701a44f9c8351c56cf0d79cad3fc81b37cf06a12debfc17a0eeb9a5ab5efa110`  
		Last Modified: Tue, 16 Sep 2025 00:41:26 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:66b79c28233f494aaf4e80860a5132a6d19249862542ee6c60d33ac7260575ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255366179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ad2f14de8e02d39782453e3375f359cc8845936ed1e6b6b7386c591f781785`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4102e9af22f540530aa6b82a785d589839b94b2e74e6eccd0c458a8fbf8109e`  
		Last Modified: Tue, 16 Sep 2025 01:03:59 GMT  
		Size: 144.4 MB (144372824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14230b59b9a2a611a91c2b24df5bfde1dda366ebfc2a2ef59d4123a1ab393541`  
		Last Modified: Tue, 16 Sep 2025 01:12:57 GMT  
		Size: 77.4 MB (77397960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d457dd2757fb82d7ea14822a4247d73349323b64cfd5b51c6cdfb1288f222159`  
		Last Modified: Tue, 16 Sep 2025 01:23:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995469ae68df5b2050d92397dae79e14c0530106826383c4a1d974b907de2e7d`  
		Last Modified: Tue, 16 Sep 2025 01:23:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99c81bc713f1637a249a4a2d5e062f25e37b3908afc660168c3240caad588e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a1b76339d44ee28605feb6e1ad60fc6b2f5a0671a8074c912e4aba98713f5d`

```dockerfile
```

-	Layers:
	-	`sha256:8aa03c8e8f00447ecac2e3d5f1f06b834060618b3ece917136151e1a9321155a`  
		Last Modified: Tue, 16 Sep 2025 03:39:47 GMT  
		Size: 5.3 MB (5260484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ad9baea682b41dac4768efdec1c712bdc7a8cad37d23fb954c8e31b7de353b`  
		Last Modified: Tue, 16 Sep 2025 03:39:48 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e27c8cc431acdf268732ff3a42ec5cec36a409b5ca39099e125531e5224388a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237727884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27634b27721fc179bb2fae08aeba20b4cfb506c1e9f659fe35fdbfb95278e926`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e1d5e296080adcb97b55846e6f82f77ab692c109d2a4971bc1bbc3770f4f85`  
		Last Modified: Sun, 14 Sep 2025 00:09:17 GMT  
		Size: 138.6 MB (138575716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be9c03992cf3a105f3599fa9d4a1d9a55ef1cc6e5d09437bdf32ccce9d3835`  
		Last Modified: Sun, 14 Sep 2025 00:04:32 GMT  
		Size: 70.9 MB (70879755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb77b836f64d58375d4e0c296e7557cd1a4c22e9d914d76de976f966aeb0dc0`  
		Last Modified: Sun, 14 Sep 2025 00:04:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca0ff13f9f7f2b97c443b50010995259a1677c9b0a0aa14235ee72375649e79`  
		Last Modified: Sun, 14 Sep 2025 00:04:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:200500d7b1652c425d1b367f72bf1f926976922a96158ba951edeaa4901e776a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a1917804615a975e326c5a59562b9841d448f88220430497c37909020da929`

```dockerfile
```

-	Layers:
	-	`sha256:a2f990921b23e9a51832f26a811646b5681c0c79ab05c4023f9f260656e2941b`  
		Last Modified: Sun, 14 Sep 2025 00:35:39 GMT  
		Size: 5.2 MB (5243658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b3bb815e9d8be00fcfce5d605da6eca1663a779570553bf7e67330d9e53cf3`  
		Last Modified: Sun, 14 Sep 2025 00:35:40 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:84d406699cb58ee6d20d3f56d7f723fe47f6b57f7f699e72d1f9fe845e9707d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237509898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bda6f51e1de1e9dbfa300ca516f7556cb2ea92ae5bb72e9c81d4573f72ff0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1a307b856fc8879483d389d861a1ed2b557f8cb9f87c8bc5d01ebb87df5cd`  
		Last Modified: Tue, 16 Sep 2025 03:39:36 GMT  
		Size: 134.7 MB (134724367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539cb2953b2d2d4bfd8ac155493eea3a7118c21efab319112888ba15e3e907e7`  
		Last Modified: Tue, 16 Sep 2025 00:47:01 GMT  
		Size: 73.0 MB (72951584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06add408fc6b4606e50895c8c6a12c0566f12f884a5800a7a262cc5c65b0552`  
		Last Modified: Tue, 16 Sep 2025 00:46:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5a1e0d57ff863962fc3cc568ceead2e21d3476a30cd56b872bad5217759319`  
		Last Modified: Tue, 16 Sep 2025 00:46:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5500cbd083c8107eca60fdcbe9dacc188706c89ceea4f0b96be2198f44a13062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395a2b3498a61c5e20a5b74ed4069507bdd22c2a12344371cb9d2f0c2e58c7e0`

```dockerfile
```

-	Layers:
	-	`sha256:efeafc84ba78ba9ad440e83679c863313e12cd9179d04173bab93ee8ea300823`  
		Last Modified: Tue, 16 Sep 2025 03:39:56 GMT  
		Size: 5.3 MB (5252037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa26e4ff8020d511cd7fe90b26f83180be3e513de1c89ad338fee64ae12fbf8`  
		Last Modified: Tue, 16 Sep 2025 03:39:56 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
