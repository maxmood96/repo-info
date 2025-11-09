## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f50b133a979048f083c8ac0f90ffc078d739c63838ba592b58f9c740b0a64edb
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9c5db8b3f799398050fb805598b35c2814da921ecdbe1c0a7106f015110fcbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274595027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e4a55362406797a4af71f0ed3ee2439159172eaeb5b0cfcbe1a29038ff282b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:40:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:40:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:40:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:40:35 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:40:35 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3667d242d7bcca060d4e2eb10b867c4fed5289fb4b5dd34e9a6490e1e73019e2`  
		Last Modified: Sun, 09 Nov 2025 02:53:46 GMT  
		Size: 145.0 MB (144966518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4f881221e0505f3523c738fc64f88a0e6915e6c09719f512fec6dd961dc51d`  
		Last Modified: Sat, 08 Nov 2025 18:42:20 GMT  
		Size: 81.1 MB (81146809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48754c5d1c3bff7c6250e4ae1050e800e983b44218a4e87771734030eb2d79c4`  
		Last Modified: Sat, 08 Nov 2025 18:42:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d2b5b518201a5ec22135be3eb76904761aea3b66b345e3c59589d486995b970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1dfc41f95fe5e76bef67b934fbec3c4b581c0ba382ef26acd6b89b0d19a6ee`

```dockerfile
```

-	Layers:
	-	`sha256:f576b758d5fc060356589ef02be7c487805f9bb2c712a82fe5c076f0dff1bdef`  
		Last Modified: Sat, 08 Nov 2025 22:36:17 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c6e2647ec28e6c52fb528470b716cc30d40753a2bd6153e4c23c2efc2a4e123`  
		Last Modified: Sat, 08 Nov 2025 22:36:17 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1387809c63bdc345fa7130fc66d97a6e9aaf2fc511b73acb3988009458f28fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271122515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242e9d35d73708f9ac9f0e7fa5b88decce3cf170a45aa5f642d70762de6503b8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:40:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:40:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:40:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:40:55 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b43f67bf20e6fb8c46ecba42d4e40f0fade02d551141dadd7a2a31293bb6a`  
		Last Modified: Sat, 08 Nov 2025 18:41:38 GMT  
		Size: 141.7 MB (141731669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2582fa99248c5a6ca8231888b62197746bf3f6e7a23cc97b2410d029f5a34c`  
		Last Modified: Sat, 08 Nov 2025 18:42:09 GMT  
		Size: 81.0 MB (81030721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29d14d45391585355236e660bef03a4141558d9571b5aacd4fcaed937ee9dc1`  
		Last Modified: Sat, 08 Nov 2025 18:42:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:17d1cd3827b3d4dccc54c500d41059f5cebe8e207a65c0444db3c20aad68eb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5f8593df3321db33a6000926c0637284bb7714daa57cfcd8578e14ae135b2c`

```dockerfile
```

-	Layers:
	-	`sha256:e69adfea354070709580d0092bf4b7e566ec8a61d723c6ee5bb82761f3df037a`  
		Last Modified: Sat, 08 Nov 2025 19:34:38 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6545384591c0b08a5bcf1ba7ed5237d5b462079231eb34b8202d1f53b8ac2d33`  
		Last Modified: Sat, 08 Nov 2025 19:34:39 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5e9b7e6e55f0e1c889b13a272790bd55a82f3049a3a60697d4e9057c5246019c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271394061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72a0d0d01ce2d1b19f4dff5bbdd14a92570c448aa333ae56ba045b8953522fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:23:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:23:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:23:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:23:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:23:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:31:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:31:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:31:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ab7f6f46e4d60fd95b0503e17b8cb75a34996b0edffaa55f4b37250d64c5ff`  
		Last Modified: Sat, 08 Nov 2025 19:24:59 GMT  
		Size: 132.1 MB (132079888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de06dcf7a7bdad01aa33af0548dd736aa1d8ef7d326fb6f9d176e41efa77daf`  
		Last Modified: Sat, 08 Nov 2025 19:32:33 GMT  
		Size: 87.0 MB (86986246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2ecf764e9f6e930c5857458c91b24d13bcb4498de304879c4b688009745db`  
		Last Modified: Sat, 08 Nov 2025 19:32:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:82877ab75a8b582641f95e37468f4cf2727fedc3fde06ddfe0370aad79a0c157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471416ab7b2422c16c376f5f722596c92443bb21c16a3c6f0ce2215a45270d50`

```dockerfile
```

-	Layers:
	-	`sha256:e190e5f5bf6774da08f2f574bb1b93ba64cf0125641708eb852567fc5111ff90`  
		Last Modified: Sat, 08 Nov 2025 22:36:26 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e4d194b61133bfd6d38330f6cc22070c93f95802c7d546b502bbe1f029ba67`  
		Last Modified: Sat, 08 Nov 2025 22:36:27 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:ea8f3b72934ffc83020342ed16bac785947118d6ea29bdbd589f2fc261e96c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252789579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ae6d6ade58bc987f12014af8ef13ad369ab2c9e9eb052435e061153a9269d6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 19:24:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:24:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:24:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:24:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:24:19 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:30:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:30:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:30:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2945cf63585292b2506b8085e166a7f8eeb0cccff213e6452228851e88a297c`  
		Last Modified: Sat, 08 Nov 2025 19:25:14 GMT  
		Size: 125.7 MB (125694385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118625f0477fb91ae5b556ef3bddfd9f85a7316a2b695d87397ab9d3b88b8789`  
		Last Modified: Sat, 08 Nov 2025 19:30:54 GMT  
		Size: 80.0 MB (79956458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094d7dbe3e4f96360a3f72f1d77858ce016dd28106ab8b914ed7eea1e984ba7a`  
		Last Modified: Sat, 08 Nov 2025 19:30:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d867331eaa76eec1c5bec28bd497328f13f7b53e14f97ea9366e3cf8d369788d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0182da31277e8833441518908bb77248f7ced4fe1756f39f616946ce9bfb0df4`

```dockerfile
```

-	Layers:
	-	`sha256:07983e45f13450d126c98c08428935c255174fdfd6f90819eb49a65eb9a2acb5`  
		Last Modified: Sat, 08 Nov 2025 22:36:31 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06adbcbc5d3975765ca35c205017dcd2ffe1404b86d38738032a3ea35294bf60`  
		Last Modified: Sat, 08 Nov 2025 22:36:32 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
