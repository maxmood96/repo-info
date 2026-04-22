## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:69819adba51ca7069ad7b961cf75d0051551f2b34c6a4e51c01866ade7977fbe
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f99ec8dea70d36243133debdf0811df4674970136a8de6984c0b1316016eec09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247421013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f362002255d6634afd9b421896e3e9a000c984ada9b89dfb600a9c08616f3555`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:18:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ff1afcbafc953e75a5e4564936c1e0f61a3fae4f3bba2db4a79d483d9184d`  
		Last Modified: Wed, 22 Apr 2026 02:19:30 GMT  
		Size: 145.6 MB (145628775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a6ec1a70c7816d699cf6089674b421f36bc8f03dfd9971184e829cc47d36b`  
		Last Modified: Wed, 22 Apr 2026 02:19:28 GMT  
		Size: 72.0 MB (72011029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc35c694370f9469e256a54d24e1c5fc91c5198e6daa59100c4b08b15c5bbfd`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c2b11c3e31e6f2ddc149d36ec39d617c7991da482257612a607caee4b7899`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5efca7b1c8626aa2486bb11470748f11dbdc4992da3c5616033182db69dd57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81993397e5c342d79b88d18ecc015b777309024fde58b56820c25a1329b5aa70`

```dockerfile
```

-	Layers:
	-	`sha256:9a38a4c9e446356eca65716cf2eababdc2ebac9165c072921f00048e086a0d73`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 5.3 MB (5259192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ad6707b27451be2e14f6de0d2c0b253248c701c7462239bc31b62380d7d0b5`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2051d6cb85acf35e69cd1acb438a48b701e44de9ea4120e81bc61fb9657182cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246411822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de45cfd09cf4dbf3aa671973985c4eb45b131799d61edc213f74e114761619a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:02 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4465b23c6e58d5a1a05042311f4685ead7d9047e0131e81387bf48019dd8045b`  
		Last Modified: Wed, 22 Apr 2026 02:22:42 GMT  
		Size: 144.4 MB (144436188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a472be38af607ae6be4edb01a1c70f52a53b3319458d77a3a89ea9c5c3bf7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 71.8 MB (71830991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ffb346ea9c4a2fb56f7bc49cee9a53d7b29316404d3e0b173c8d8d14f58bd6`  
		Last Modified: Wed, 22 Apr 2026 02:22:37 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f717d86f6e89cad1393481616e3cffb1593a9e6d54c1b928ead75cb124993e4`  
		Last Modified: Wed, 22 Apr 2026 02:22:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc4a273a1f38a83e1ff870c67096e7d35357be63d7d6078c4ed902bf03d689db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67e0eeb4cbe39650f1a45f8f9e67999fb920efc0364f19b28c1f521d88bb3e5`

```dockerfile
```

-	Layers:
	-	`sha256:420e9d7d693ac18bc52ddce585f67358d8573f98eaee92335d761399f4d6acfd`  
		Last Modified: Wed, 22 Apr 2026 02:22:38 GMT  
		Size: 5.3 MB (5264961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3058b0a5f9a21c5eb0d67efe11d6d4cc17857844f9bf7e0bc05aee694cba5dc4`  
		Last Modified: Wed, 22 Apr 2026 02:22:37 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f9b293f014000708d0a8e7c84c3946c223026339f639e24754b9ec370f79a133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259643381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1111f1d7a9b1f3fe748a3f843d0f9443c3786a5c0cab04abeeffe4d7b0414b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:51:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:51:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:51:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:57:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:57:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d63fa71f8a08634b0312e1df11dd8fc3363471d8c3e45af52999c7c3ba56e4`  
		Last Modified: Thu, 16 Apr 2026 02:53:12 GMT  
		Size: 145.4 MB (145438287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee785cb4b2f981419a2dc622c9210cf5d41863a25b7f000daf150541ee234e`  
		Last Modified: Thu, 16 Apr 2026 02:58:10 GMT  
		Size: 80.6 MB (80611032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8766f31590bd4c37b119e329c2b4ccd9e3e9ee28d44129e81ecb1e27a93620dc`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd6d6404d14177e8aa7f0522f485449cdc21d9bedff44ac99d5197ddbf9aa2a`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47c6df4b9a68cf4b75748dba7fc51f83d6b91322c0dd6ba96cce25610ff2168d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ba3975072071fc5548e5d3f50176c13866cfcb9c9b4062f9832cf3701a197`

```dockerfile
```

-	Layers:
	-	`sha256:3b68a706401f501cc21fa4953582689cdc77df726389bd79cc5adb4c72a0d328`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 5.3 MB (5263509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd455d244808a5cd9943caf786693e3474765118f81a27cab4e985fff4ef6d4`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:9a9848c18c42d80a9a73c3e6433a794c62014ea9109341e6422410ee7518d046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244458615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb198cd1fe435b3d51475d82bc48d39c3c9b1e6fbd0f5dbc6298d0722fc6a71b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 18 Apr 2026 04:12:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 18 Apr 2026 04:12:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 18 Apr 2026 04:12:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 04:12:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 04:12:57 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 04:35:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 04:35:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 04:35:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 04:35:59 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 04:35:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6098747780e1520a3d6d899270f72a03303fffbfe05521aef71b5a82c3ec10`  
		Last Modified: Sat, 18 Apr 2026 04:18:43 GMT  
		Size: 142.7 MB (142662942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41795faab70d4d7af4e407edbd10d392f571b6d67a3c5f9d57c50171ec8f38da`  
		Last Modified: Sat, 18 Apr 2026 04:39:43 GMT  
		Size: 73.5 MB (73518848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a84a8546c9694ca98f7dc0fb4fae5a8cf06461f0ea5b044c1560cc68b119157`  
		Last Modified: Sat, 18 Apr 2026 04:39:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e518160d2dbefb6dc86914af152cd3ddecf138184549b9c687c0c6ea274275a8`  
		Last Modified: Sat, 18 Apr 2026 04:39:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0dcfa53595fe13616e65a197062ecb3c74bc4d4d1120ed8427ec19a12c7dd6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1594937b20c8066571d4a21435fa6ca46808bcf1e70bc618acda2bec76a4436`

```dockerfile
```

-	Layers:
	-	`sha256:50a1591a9553f2c23dd47caa992d3e2dacc9c31179780c3cc61f6a4a812a42b2`  
		Last Modified: Sat, 18 Apr 2026 04:39:33 GMT  
		Size: 5.2 MB (5246683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be32f87a783c1c33791d13c8a40d91960f9ed28789c12817c9bbfeae95ceba82`  
		Last Modified: Sat, 18 Apr 2026 04:39:32 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:52b5e17a373a04d89d7beee3805b9c9fb6aead449086bc5a769a7c2e5548df53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238455422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cb4472130ba3d5f63dcfdc4585e5a8dbc3e073f9577c688f6df2f3b65c3bdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:01:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:01:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:01:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:01:03 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:02:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:02:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150332b9769a3e50f47d036c734faa3f383f8ddacfb44d5dcc29fa64b02ecdae`  
		Last Modified: Wed, 22 Apr 2026 04:01:47 GMT  
		Size: 135.6 MB (135627000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07a87de185171280320c8bb7216ba61fd3e71db135ce5537da4a19f2bbea67`  
		Last Modified: Wed, 22 Apr 2026 04:02:51 GMT  
		Size: 73.0 MB (72987082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873213f0ba4721a51f43092b62ecb6315412a423d5ec7151cc2a1d9320057d9f`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8967983ac424ebaa33dfb9ae561201e64c011368a583177a19fab59b3e3c5e1a`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0db0673300dd5f4eca88f1a355610596a691391d214a357f7f894d2d93a54486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ada69889849da62564b6d52e611d161cb0dbc64b492a4d94a39756291526c1`

```dockerfile
```

-	Layers:
	-	`sha256:4f86e969552116e6bf82f6e1846a21a4c5d611a715bc0851182151c013df02be`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 5.3 MB (5255116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e742f00a8496439e92785f33745bf8f4a1e2a072f0f0ca211338c981d07711`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
