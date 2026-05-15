## `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm`

```console
$ docker pull clojure@sha256:c2a66984bacb92c9ae818f5890b0510cf3f2535c5722dcb1550d8f5d1e39fb03
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

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3a7129b67fcd3b1183f6fe50945d0d6e81490b8811ca6a0284395aa4f0b387af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287870210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322c97c44fe63244adbe81be3535f971f4ed9f87883d40244e9460bc1ae483a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:15:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:09 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:09 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0702506bdf11b73dc83a5507ad016c2b34a46248cea22bec0955347e344b780`  
		Last Modified: Fri, 15 May 2026 20:15:48 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e314191ad330eb23be42ad029ad87fba0a6c2679be44f1ee0b6c9a0157db232b`  
		Last Modified: Fri, 15 May 2026 20:15:46 GMT  
		Size: 81.2 MB (81213552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b240e91b0004aa38375d05647026b1ac0fa7cc8bbf494eab998389ae5eeb25`  
		Last Modified: Fri, 15 May 2026 20:15:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2c227ad67500972f9e259abb8dc02c3cd593e82b9c5f862bd0227917db881d`  
		Last Modified: Fri, 15 May 2026 20:15:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:93d6dfb02cc9a9fbaaed2eaffdfb8974d0ae7166df53b2f0e077211543de2b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cce164abf149e337f1d3d548e5ff603fa6f0c5c6fa43dc32073225abde05889`

```dockerfile
```

-	Layers:
	-	`sha256:81f129dec0b91556a0885502980a7e2540f2b593cd83f2243e4959e1a93de39c`  
		Last Modified: Fri, 15 May 2026 20:15:43 GMT  
		Size: 7.4 MB (7381463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3dbd8c0d98cbe65f2ef7c9543d9c37587e246f5afd84c98ef7551dfdbe2b449`  
		Last Modified: Fri, 15 May 2026 20:15:42 GMT  
		Size: 16.6 KB (16614 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ea4476efb998d127be1016f31141caa4c5058fbf184c894678adddaffcdd364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286030752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84336c796afd1896f55af45346bed5378ebcc644c748b06643734849c47e816a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:15:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:11 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:11 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fef9626ca16f252488cf423e384845a5b476c93a9156695c6a6ab77f6a7421`  
		Last Modified: Fri, 15 May 2026 20:15:51 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5b5d41559acc99a6d14d13e2677bc3283b9b81f4f9c370a605d47ad2f07091`  
		Last Modified: Fri, 15 May 2026 20:15:49 GMT  
		Size: 81.2 MB (81195237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00feb7747621077635e29f60e55595c64d5198ead0da9f6e58496e63934cbe1`  
		Last Modified: Fri, 15 May 2026 20:15:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362f04847cfa79a74802be3007f006f79e3dd41b9401580e8603f65ecb85163e`  
		Last Modified: Fri, 15 May 2026 20:15:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:57b4eb70d9092e48fbb62e5543964222e53f611b0cc1d4af21db6ede27cea75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3fbb7831f1ce37f4fe301951746c3503fad0689be9a69280aa8c6d250a3d54`

```dockerfile
```

-	Layers:
	-	`sha256:1bcd68aa1e636324cdd4be8c90b417249639d9bf709f2b9ddcc2427b1d8e6e20`  
		Last Modified: Fri, 15 May 2026 20:15:47 GMT  
		Size: 7.4 MB (7387250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f355a6ea1f7aba0fa9b9557277019c0241f1bf393a20849fe0f199bcbc87a5d8`  
		Last Modified: Fri, 15 May 2026 20:15:46 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d2bf091370e2fd1ec6911e6b4ea679b9b1bf67777e70416af6d546ee0da438c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297714514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2887f350bc821ab6d899fbb294c28c4462b65e92a8b5facdd348c0d840b90d46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:36:33 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:36:33 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:27:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:27:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:27:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:27:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:27:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7fc9485b4fb59cd58fcb71fcd4db3dba936648eb297bdcd72a79d669b2338`  
		Last Modified: Sat, 09 May 2026 02:37:42 GMT  
		Size: 158.3 MB (158343237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34a3dcfec2dfdeec3cc5ad2825e4a2aa93bacc18c75e68e8e04456b26114405`  
		Last Modified: Fri, 15 May 2026 20:27:46 GMT  
		Size: 87.0 MB (87033444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3402343b535b8aa394bae97057d2e04c1b9bac5f4b49b3b47cba2a6be9e95dbd`  
		Last Modified: Fri, 15 May 2026 20:27:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc6a0c58701ef05d491f4fa08dbed84fb6bf57d93e4eb22ff0046609f2342ae`  
		Last Modified: Fri, 15 May 2026 20:27:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68b001025036b8563c1cb68b35f1d12ab308abf3c288fc79f2ce54361a958a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dab3d5faa76fb05dec3a193bfdf227393df1a45bafbff014213282aa0ff139`

```dockerfile
```

-	Layers:
	-	`sha256:a22320cbbc099379fc2423672d575946286f23c1598c6707a302bbc4b6236f87`  
		Last Modified: Fri, 15 May 2026 20:27:44 GMT  
		Size: 7.4 MB (7386691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b8036864f734d5cbe7650a3d2e098a1e3a2a87f9d85cafa3ea489cff595681`  
		Last Modified: Fri, 15 May 2026 20:27:43 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:ff01d35e5c8aafb975366ead96bac7965f5cedd296246ff4c80aff8766768758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274562982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4650c4310215d91bd994716932fe56840967071101e1c0a8817c4fb5663701ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:42 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:35:42 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:26:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:26:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:26:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:26:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:26:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25cec1d73807144f8a4fcd73c3f56fbd2782d89baf163adc3be7c86ee3ad419`  
		Last Modified: Thu, 14 May 2026 23:36:27 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec735c1c2f57f8940935c18a88a9d79a16baa9eb337259458045d418c1d25d7`  
		Last Modified: Fri, 15 May 2026 20:28:09 GMT  
		Size: 80.0 MB (80025564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e16938ba93c25ef947706ea204187270a7bb45b9e9442a3353d494fabe05f2`  
		Last Modified: Fri, 15 May 2026 20:28:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4fdb597d936cea92812fe6c91d17b3e42e89ad7ac3b366b07537ccd68342d1`  
		Last Modified: Fri, 15 May 2026 20:28:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c8daf752152fd2f7f222e2192f0b07732197b66fec4e0711c4c2924d60ff657e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1182a1b779fb7c3a4cadc48300eb53e399fde1b5c3f9b27048c21f371f5c4159`

```dockerfile
```

-	Layers:
	-	`sha256:c90bab72924ad3c7e50983d9eb858c875c43848a8d063ee021f4713ffcbb8f68`  
		Last Modified: Fri, 15 May 2026 20:28:06 GMT  
		Size: 7.4 MB (7372782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6086425699f27a5474a527c0a21a17c4f8fe5a555c4874a4ce9012d39d1d6929`  
		Last Modified: Fri, 15 May 2026 20:28:05 GMT  
		Size: 15.7 KB (15661 bytes)  
		MIME: application/vnd.in-toto+json
