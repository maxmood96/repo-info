## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:bee547fcb92ac65031bf591aa7030d75bd1fd136edb20710cd32bf5b8603bdc7
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:94466682f64407d1e4d8b4329248e01434db5fa86462844020a468f262941893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240766883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a69e0c26fe53f5483a68a8841d654145602ee4f97660e7cc5b67f812525bd2f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:15:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:58 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b139be38763e67841b4b9784d2215b175e4c76c9b570463f69323d4a35ae91`  
		Last Modified: Fri, 19 Jun 2026 02:16:30 GMT  
		Size: 145.9 MB (145886130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53302701e6805685076a986772c6870b9ae9f1c064fb4332ea0a9b248dec8046`  
		Last Modified: Fri, 19 Jun 2026 02:16:31 GMT  
		Size: 66.6 MB (66642486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fa870820a1874de1c1960b82b0e54c7e775d8933e52d6d859743b589450055`  
		Last Modified: Fri, 19 Jun 2026 02:16:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3187630c2d5f020349cb0b24daf3d609501c451ed528c91b5a1b7a4467d1e357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5447a7cdf45cbe91e55e50265b8306e1b651a189fd984fcb0e097278985867b5`

```dockerfile
```

-	Layers:
	-	`sha256:030b9e15d470e6952bf75a976df79c7faffa1392b8ede33abeeca151b7d2ad01`  
		Last Modified: Fri, 19 Jun 2026 02:16:28 GMT  
		Size: 5.1 MB (5133515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936720735ebab8a4526dd56ab442ebb0482d061e95563187d1a04a91f556576d`  
		Last Modified: Fri, 19 Jun 2026 02:16:28 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2d4ddabef13dd9a2405356e1996eed877113262a5edf27b13f296a3b925c4a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237348308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697af6a46066b6fa10532ff71e262c419c82c362c7ae41062624f2838597ba6`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:04 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2121b9d7a31acabc95a11e61fcceab22aec170314c0943227adf0bfdf6c6f`  
		Last Modified: Fri, 19 Jun 2026 02:16:41 GMT  
		Size: 142.6 MB (142582140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dbae597b639db3138c6ed475f9ca82a93e58916fa62a99552de8bc29050157`  
		Last Modified: Fri, 19 Jun 2026 02:16:39 GMT  
		Size: 66.6 MB (66643217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed92cf94aea41e76331a61232f87e2ae07d8b9ccf4afa0eaa148d490787269e`  
		Last Modified: Fri, 19 Jun 2026 02:16:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1341a8dd108495b73bc5ca08502f0d509442e0e9264e111a0d08e4f73c67d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a325b89ae9f92e19eff5bb28ffe64fdc5e9328ac6c9f22dd2eadc62866b25d04`

```dockerfile
```

-	Layers:
	-	`sha256:e7401d81243a85d49a8aaba9e3bc263ee618bf1652c6b97998f174b2781f16ed`  
		Last Modified: Fri, 19 Jun 2026 02:16:37 GMT  
		Size: 5.1 MB (5139894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:871b0eaac4f8df7daa6d8200645b29a8744bbc8284743a35f64a92b1c550b357`  
		Last Modified: Fri, 19 Jun 2026 02:16:36 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f9434176d0337172cbad4f1be2fd27708c630abeb09fc773f95124f32e6b1cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237669641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71a4f56cf871ddbcd44ff41eae548ddb45d4528ba5661c1fc1babbe88e67eea`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:24:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:24:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:24:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:24:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:24:59 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:34:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:34:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:34:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09682529f6dcf184fbf2932f1bc6307869164c5cfcc088948da539898ec50cb2`  
		Last Modified: Fri, 19 Jun 2026 02:28:55 GMT  
		Size: 133.1 MB (133110739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce70297e8b7ca76bfe793ca189fd93b93ca7e0c78ad19c7d61a15bda2a6b7e46`  
		Last Modified: Fri, 19 Jun 2026 02:34:44 GMT  
		Size: 72.5 MB (72476316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d5cfd6f37063617a408ef540c299af267e1b385bf76f6c245b79de3699c74`  
		Last Modified: Fri, 19 Jun 2026 02:34:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:228c594a526edd5bd19605edc6726343cb6c5c3ac456afda2cda188a9f5ef6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40e9c05efcad58695b9b9c809939cdebb256135cf7d7ae247cc65300d640cd8`

```dockerfile
```

-	Layers:
	-	`sha256:3e6e328b9b5c27302301ae256c0203850d1f9dc2be258bb7d50ab238594ad6bb`  
		Last Modified: Fri, 19 Jun 2026 02:34:43 GMT  
		Size: 5.1 MB (5138058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c92b05ed43c7fe145efd37ad77d71a2e0aa3b338909f69376ee6e1061ffbb21`  
		Last Modified: Fri, 19 Jun 2026 02:34:42 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2c2e1c10ffbfe8708772bc83f77b52802fb0506ba7c40d5c757240e2677d8242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218998896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187af8f6a2b2716c49218024c7bf47c2ecca3a9a466c498ea4066e033325aa0b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:53 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:13:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:16:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:16:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61d6cbda07a1a85b6a53b221f86a3eebbfb9b38c4eb3192694a80b88b525000`  
		Last Modified: Fri, 19 Jun 2026 02:15:29 GMT  
		Size: 126.7 MB (126652584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d3d6eda1617dd56eb59513bb152131b9e62b6b255952ad41eb3eb0a7490dfa`  
		Last Modified: Fri, 19 Jun 2026 02:16:22 GMT  
		Size: 65.5 MB (65452160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f437958c4cf4733b9f7d2648e984a51cd36e172ac852ac3ca0b091b0417a4`  
		Last Modified: Fri, 19 Jun 2026 02:16:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0875c7c7d99e8c7abc9da9251cd139f7911ed19b202c9d24a8506b1e5e6af8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1785b665bd08033ad9eca637519924484d38d50f39269e4e802ed072ebaebd5f`

```dockerfile
```

-	Layers:
	-	`sha256:4da94c15a4e6bac402538169af745100d67d54d8eb89d6ee039611dc1e7af928`  
		Last Modified: Fri, 19 Jun 2026 02:16:21 GMT  
		Size: 5.1 MB (5124840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108ba4aa01b09c6d89924c4d8979b5e18f5424c10d02f55fbd25bea5bcd14b64`  
		Last Modified: Fri, 19 Jun 2026 02:16:20 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json
