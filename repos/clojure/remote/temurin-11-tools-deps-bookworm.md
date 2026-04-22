## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:8c72088c31ca0bdfbd6fe7cdad9cb72d6af8b32c4eb0a56b3e0af7aefe727efe
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
$ docker pull clojure@sha256:9eb1840eb57539e1fd0c494a030903e28d26ca89ef3c0536d44f2f31c7f3b633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275462622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4600c6e7f8ab0f3616f2553db39473f57fc39a5c27c541b54194254dd8c343d7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:17:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:17:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:17:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:17:23 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:17:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:17:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:17:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5419099bc8f3a1a84218f3e8db04ac67fa66924d18c7afc6b3fc93293d381c`  
		Last Modified: Wed, 22 Apr 2026 02:18:00 GMT  
		Size: 145.8 MB (145806794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b67ed0f4e5fe9fde39f76f50fc27411c4731ebe43c78641c26f4a4009c1585`  
		Last Modified: Wed, 22 Apr 2026 02:17:59 GMT  
		Size: 81.2 MB (81166554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086095b2c3e2ca209d30bde1e0b79ae66703eb76fdaeed95f6ce45ba5786bdc`  
		Last Modified: Wed, 22 Apr 2026 02:17:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:333433c2b52e8fc9102fdc10369be2d380dc119b00dbd8b3daaa92a9e3373922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5563415f3e165d31ad4591ed5985f602270ac11129892be96c8f8a09c289f8fb`

```dockerfile
```

-	Layers:
	-	`sha256:284064e9d3e25c53a4969c764c04038fcd356c52b8683ef16cc9eeb19b75990d`  
		Last Modified: Wed, 22 Apr 2026 02:17:56 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b4b4e0c0fc485f1d46c27726c34576afedf0c0d12485747d2a37d95702c251`  
		Last Modified: Wed, 22 Apr 2026 02:17:56 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f07ab984199d4439b7afe29e594c3b7227b376c7c0e4f85995a2f46625def66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253690536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6bedfdb2929721241dc1c8e832dc4b4fd11b117226c42e14d7ee0facf6535e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:58:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 03:58:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 03:58:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:58:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 03:58:25 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 03:59:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 03:59:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 03:59:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e0b2edc82a3ba082e9f30dfa4358139881cfd62d2d6d055012699a091c83c`  
		Last Modified: Wed, 22 Apr 2026 03:59:03 GMT  
		Size: 126.6 MB (126562180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a03b7d18cfbc1193c2b55ff8e661be25f67fef39d5490f9b6aacf742a755d`  
		Last Modified: Wed, 22 Apr 2026 04:00:08 GMT  
		Size: 80.0 MB (79979741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd42e17401e27ddb87c7375a6b40e2aa492c36040031ece9014941b82972b3c`  
		Last Modified: Wed, 22 Apr 2026 04:00:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be3af0284db2dbe76b4c9d887b4aa1211d0d4a84b56b5ad6595396433dddcd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce866bf4044b52e9e99b72a12f60b39bbc265023cf1ae74154d860ef23483f6`

```dockerfile
```

-	Layers:
	-	`sha256:94529d99d826a93bdb4b82b75e98f0f231acbc4aaad4b9018db37a418b4e3fce`  
		Last Modified: Wed, 22 Apr 2026 04:00:04 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6ab35e9889c625f5bf6b3ca294ee1f825a0f50ab8b3b58f7e74aa34a669a1c`  
		Last Modified: Wed, 22 Apr 2026 04:00:04 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
