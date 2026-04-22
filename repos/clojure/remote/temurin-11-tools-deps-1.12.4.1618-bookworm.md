## `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:5e76cf3dbb9cc4f1b7c1a2f846e040c0e4f632ddbfaa71e2e9d1b236066c2073
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:113b677ccf163065627a5dbed7cb26b6ec409323085a4fbb765786431f76684f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275462741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae950a1a45014354a1c012888b92648145ce555f9d87771cb61b05f5d038f17`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:02:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:45 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c235822ae767753eebfd96dc8d59127c8d2e59a178619638fd31ba2c99d190b`  
		Last Modified: Wed, 15 Apr 2026 22:03:25 GMT  
		Size: 145.8 MB (145806843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c31c4c1df7078dd3469b1e4fc4a7571ff99287eeadcb592bdbd4b87d2578657`  
		Last Modified: Wed, 15 Apr 2026 22:03:23 GMT  
		Size: 81.2 MB (81166429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd957e555ab780843d42e5b83488bbaa85a948be4457cf946c1b9f5a2b2e3afb`  
		Last Modified: Wed, 15 Apr 2026 22:03:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:578ca7e43510d2e21279b0e6175be267aaf7cb472728171f542de5c30e9b56c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758f62132fa18e2bc9ba4b573aeb5274b0aec890bebf9feaeb958448a6fd5e30`

```dockerfile
```

-	Layers:
	-	`sha256:c0604cadb063d86185f6456ad2c4af88afdaef94cf4708f9a118303794edfd1e`  
		Last Modified: Wed, 15 Apr 2026 22:03:20 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ae0f9ca311ae29552a7e0c25edd411ce2c23ec178061889af56df6c16d94f6f`  
		Last Modified: Wed, 15 Apr 2026 22:03:19 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1bbbb2d59939f3fd07edf1528113d8d5978e0cc54bb480727ca17418fc062672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272048641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf6d980268377d4d69f80bfc1644f2cd5d81567e5f7a987621e399dc0298e49`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:58 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552a5082121fb2ebd807c5a86e671730c73060a10c23300a7ce52bc5169bda32`  
		Last Modified: Wed, 22 Apr 2026 02:20:33 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852d47d3d54241c0c6430e99ccda3a80451b36e468515152a1bbbdde6060a20`  
		Last Modified: Wed, 22 Apr 2026 02:21:13 GMT  
		Size: 81.2 MB (81174124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b833f8f1ba9eabfcb22527bf40d7f973d094a94ce504ceb2e9fec7c9f2158703`  
		Last Modified: Wed, 22 Apr 2026 02:21:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bf6ee19dcfaea258e0279e0d5f124ccdf0abda567212abc654d1ffa88a0473aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cc8b027d4d7fca936122ee98dac5d9e26832931decf0a26449e7cf997a8bf9`

```dockerfile
```

-	Layers:
	-	`sha256:1d7bcd8fdfde7a166dbf7f246d5bf06142bed15f8deaceee5ca42c80783e6a0f`  
		Last Modified: Wed, 22 Apr 2026 02:21:11 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae342d99448533143ed8a244f52f3e5442a3fea3bd451f0bcb0bf077238d5ba6`  
		Last Modified: Wed, 22 Apr 2026 02:21:10 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0459a691592f78c3485274fb55bde8204bc47c026200ff28a28c264e6e6f8a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272339109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4cff9097a942f3298551186cc0cbce3d662d4a969a8b24919495cc60aedc87`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:39:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:39:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:39:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:39:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:39:16 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:44:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:44:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:44:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f08576a3b8b271adac7d002e7567dcf015c8ac81d3ed51022365675ad7d50a1`  
		Last Modified: Thu, 16 Apr 2026 02:40:26 GMT  
		Size: 133.0 MB (132997390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5b2d28f58d27d879a08b3dffd6722ecbf502deb0bf504104d9e7871e3ab222`  
		Last Modified: Thu, 16 Apr 2026 02:45:36 GMT  
		Size: 87.0 MB (87004134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c44bbd818bed766f0a0ce9a6533c12836146ed2370422ce5e988b9f57508131`  
		Last Modified: Thu, 16 Apr 2026 02:45:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:11e56866391e290d23110355c919ad5a160a85b0f9a0f4c73bb5573ac7dd4ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213b4a4f82f521e0730834657a63c887226a961d77de1be032781116748cbc41`

```dockerfile
```

-	Layers:
	-	`sha256:f193b7cfabe68603ad032a3efc23f348770fb2a47bd738b5b58f90172ff42056`  
		Last Modified: Thu, 16 Apr 2026 02:45:34 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0fa04287c329dd2d8bab4107e68bdd0fd46b829c2b5b974f37023226b77df6a`  
		Last Modified: Thu, 16 Apr 2026 02:45:33 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:39abc3801a9f6fe9a578cfc1b6d1cea08d4caaff6736f98d7c1e237f1f849a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253690712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7cb12869ee51744422cd38fff188f696ff84fad5906dd418d34308807607c6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:36:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:36:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:36:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:36:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:36:06 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:36:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:36:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:36:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ea59ff267ed71c1e33bbe4293d70b747d8359eac1781ffba708fd40e2a3a4`  
		Last Modified: Thu, 16 Apr 2026 00:36:47 GMT  
		Size: 126.6 MB (126562151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede37d9d115beb0e8b34dd8e1c45582172e621d2cbfaac718da87fce8124c1b8`  
		Last Modified: Thu, 16 Apr 2026 00:36:49 GMT  
		Size: 80.0 MB (79979834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b70fb7d529025db69bb5afb4ab1db6fcb1a96ea4afe295c15a8bb5514b85dd`  
		Last Modified: Thu, 16 Apr 2026 00:36:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e46ffc9e7a3c9dea4225cad6cacc0c2aff94de3c5d1adc411d1d71c26190dcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a633e1719f5992129bdfa6edf6ccd91bf20c1dcba1a1cb00d1ab182de21d03`

```dockerfile
```

-	Layers:
	-	`sha256:dc00f95e9fc7cf2f1d3c679dae5dab2aff7322313e35141cef2104165987cbe9`  
		Last Modified: Thu, 16 Apr 2026 00:36:47 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74231854dc30445ba810106c39e86c590d62fe3d086e44c3e3a224d4171ffaa`  
		Last Modified: Thu, 16 Apr 2026 00:36:47 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
