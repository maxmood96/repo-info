## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a6234aea849518eaa300316e70aa32a097aa8d8cb0dcb7b968880ebfa9f60bc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2f96dbf2dfec1e60981062b99e51f71cd8e82875d1d701472951fbbc5342cc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.7 MB (282683019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb951f289078a74a61d425140e33b35be20678ff10a9a8eed3f99929312fdcd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbae5bb1acd2f3069b480560e78a1b25698b645f3474df25250a74a0eb8000`  
		Last Modified: Tue, 23 Jul 2024 02:01:28 GMT  
		Size: 158.6 MB (158579359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e08769b00fb94621f6a2b8db550ce649654a2c7130d35af1867bda2d87bf921`  
		Last Modified: Tue, 23 Jul 2024 02:01:26 GMT  
		Size: 69.0 MB (69021256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2bb0265c34a3b1a5e52edbe7b691eb22bd61983efcb0ccbd1f83b92d17533c`  
		Last Modified: Tue, 23 Jul 2024 02:01:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b570a5d16f905f8a15e12b35a739c1ca845af7d24bb9edb9cb6cbc2d4b5c1463`  
		Last Modified: Tue, 23 Jul 2024 02:01:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:81438c6e36d978b4c82f1ac85d8ac95d8f0329741c8cf339ae2dea09a3e29d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ba8908fb8a3598c0ca04618595c2e505fb9a14397d172eac043964a3b6517c`

```dockerfile
```

-	Layers:
	-	`sha256:128583edda1f173558cc2986bcc666e17d35caef03b8743ef21ef8b261d05114`  
		Last Modified: Tue, 23 Jul 2024 02:01:24 GMT  
		Size: 7.0 MB (7041030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363aec8d926fe424a3553d721992e82c16676039fe889efb2f453b20d1040823`  
		Last Modified: Tue, 23 Jul 2024 02:01:23 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:623cb578ff5fb1dcfabe616bb8e8b900b98cdb562f733ea7cc880700f83490b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279522234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f686001c5c00d0402761733a9db7ec44e4968eb97207ccd204bdd1a632ed8677`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecca8477e0397c040d15e67b7e57feb8812c304741394dbd74afe49b31a0365`  
		Last Modified: Tue, 02 Jul 2024 09:37:28 GMT  
		Size: 156.7 MB (156665627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d401c3fbd8be617206844e4b10a9a4e7dc3743ba28333b3b1509785466f7d`  
		Last Modified: Tue, 02 Jul 2024 09:41:11 GMT  
		Size: 69.1 MB (69133912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a166113cacf91ac9bff320a3790c92182730160eeade41964bf097f657bd957`  
		Last Modified: Tue, 02 Jul 2024 09:41:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aec5fe2c12a558a22bdead70eec566ecc360ae29a41226973c7c37600d84eb`  
		Last Modified: Tue, 02 Jul 2024 09:41:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2d517e4fb66f41ab57fffcbd83b9a4143ca6084e8852d2dd5f07741afbad10e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9612f04dbcc61507dbb2a8f2af63dd731af5d2d2720db56a4cfbdd838cd8197b`

```dockerfile
```

-	Layers:
	-	`sha256:c3abdef51398d53db546272290789b3670ffff1c7686ddc34b1dd925e94e0683`  
		Last Modified: Tue, 02 Jul 2024 09:41:10 GMT  
		Size: 7.0 MB (7006222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a107cebc70471620f7e0c871fcd65f27de0b19f6f171ae217a37ee98504defa9`  
		Last Modified: Tue, 02 Jul 2024 09:41:09 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json
