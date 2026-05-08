## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:a8a18e56752694736d53bce1c4f9af14e14932efe4d9329df846a18ed4108a88
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dd8fe726c59d548f6d2e7ea6fbac4901cdcfd500eb1e6c409b9261f5e925719d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275541816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e26d4dbd105a8505e31cadb2aff70555a09a979ee911ee9bec8486e7f1e2b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:06:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:06:19 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:06:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:06:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:06:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428edb2b2b05a42673fbd4a0a37f45c3d9ba60f5f782ba0c3c41013fc3a9566e`  
		Last Modified: Fri, 08 May 2026 00:06:56 GMT  
		Size: 145.9 MB (145886194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04769d910efe37e92f44a2d681c85aaa1aa71aa219d6d872e93ced608468ad8`  
		Last Modified: Fri, 08 May 2026 00:06:57 GMT  
		Size: 81.2 MB (81166349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51194bc42de6f5b78a99e80df6be9f9e50c438a9903c8ca51612a2cd5e385308`  
		Last Modified: Fri, 08 May 2026 00:06:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:93f952c30d439ed353a636b0a45b5b7f92e57780b2df302bbe74614b09069d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43add15e17837d55fb90bc316da6a6e2619ebc43df15753b434a48ece3f60493`

```dockerfile
```

-	Layers:
	-	`sha256:eb785e5273c4aad623e31ada89813dd94d5da26c869dfe61e0f4bfe719fcfa04`  
		Last Modified: Fri, 08 May 2026 00:06:54 GMT  
		Size: 7.4 MB (7398445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8cb42f09b2d7718f91e5d951edf757150779781648b5de83bb483c2ea41422`  
		Last Modified: Fri, 08 May 2026 00:06:54 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:55301b4a7f6391f76b77fb06c370af2aa38dc82d7c968aad036cfc30d33d4812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272130370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85cd7dafe8439e69b85ecc474a2d3d2728e4eeb935bf292dae4a68f38b40a97`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:08:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:26 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aee3f00cb77b6b5a117e42dd3c428dd1cd5c346bfeec65b98228688fcb21ce7`  
		Last Modified: Fri, 08 May 2026 00:09:07 GMT  
		Size: 142.6 MB (142582244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaf8585ac082ab1903f479886ea7758f4607ed3a801b542575a1fb8a94f2e61`  
		Last Modified: Fri, 08 May 2026 00:09:04 GMT  
		Size: 81.2 MB (81174411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96795f6dd31012ceb1b933714b8218d5dfe71d656144d38e951b240685c8adb`  
		Last Modified: Fri, 08 May 2026 00:09:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:452329703dc85592c9504fcef97b5f390ef1df96a709e8781c50d887862a12ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce10ef6211810793f0695944f37e0e9a7e4a946c596257592224294477914c16`

```dockerfile
```

-	Layers:
	-	`sha256:bf6db37dc7fdf3dbc500970e9182ae050c99b2a327f6fb58ca63bf4508b9322f`  
		Last Modified: Fri, 08 May 2026 00:09:01 GMT  
		Size: 7.4 MB (7404826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e672c5c79541a7b2d3201ad6fc1818f85617a1c519fcb6ea4a7aada0cf2537`  
		Last Modified: Fri, 08 May 2026 00:09:00 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cf47a4d8d34baad02921deac9200567b4fdcc51b08ec7fa0ca2695480ad10f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272451618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6bde78b52cca274f0a9bf85f81b574c501bff5ee04852fe470af7326be33ce`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:32:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:32:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:40:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:40:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:40:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ccb486cd38d4bc6e81d6a758dc0756e8388df36970ae898570b04b2565a95`  
		Last Modified: Fri, 08 May 2026 00:38:30 GMT  
		Size: 133.1 MB (133110145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f069442f2da4efd04df94d85f3cd53cc799cb029d7b16984c8e999364425f4f`  
		Last Modified: Fri, 08 May 2026 00:41:36 GMT  
		Size: 87.0 MB (87004093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26258ca5b18a373e77774f7a4c735d81a332d6a071fd7342ab6e8cbd7892b77`  
		Last Modified: Fri, 08 May 2026 00:41:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a04acbb95d9468aebaa11afb42e79415e6aa569f32c670dbf371ec27da01181c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99cf3d555dce03940f4703da19ccf5fbb26cd11f030599d4017cd6f41cc237da`

```dockerfile
```

-	Layers:
	-	`sha256:303512ff4807255878dbe78770cf6b9187f63bdcedad74b13b96465da149feea`  
		Last Modified: Fri, 08 May 2026 00:41:34 GMT  
		Size: 7.4 MB (7403046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df8443efad10bc84779a1094e44810e089a58f3449596fc18368f168f311cbc`  
		Last Modified: Fri, 08 May 2026 00:41:33 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7ddb6f07fe0b77a262cd1fb8f22290cbf8db7de4751139ed1e223b6268d3b322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253781172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0e700f74691b815b342eaebfbb427b7c704b7f05be12652e3b3ec2d88fc904`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:12:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:12:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:12:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:12:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:12:54 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9877cfa317cb3a147f3af298dc6f97e96426f3a35ab1d50968ae58d675a805f9`  
		Last Modified: Wed, 29 Apr 2026 23:13:35 GMT  
		Size: 126.7 MB (126652695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a80cc25dba2d73816d107005dd02248bbef7e6dca0678b6d4d07fc1ea2cc70`  
		Last Modified: Wed, 29 Apr 2026 23:15:02 GMT  
		Size: 80.0 MB (79979863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071d09ba97e0f5b47722d7f2dd5989084fa9404dc6013a5b97d30754a640e8a2`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:014e3c0bdd12d4ca9cfaa6c96b144e76cd520820404dc58f7197fa19e64317dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3967faaa5bf9da6bf52cf6b74c472099dee79a12b89910987706f1d2d70a78ea`

```dockerfile
```

-	Layers:
	-	`sha256:67f548dbb9c8004ae628ac561d8f6fc201ba87c65a60c4a079cec8d2440ce6ea`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 7.4 MB (7389768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2cbee656bdac5e14814e6f6ca5767fa43be4cbb6fc83e9ff0f1cf1af9d18d83`  
		Last Modified: Wed, 29 Apr 2026 23:15:00 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json
