## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:612a45074131f9f69d5dc2208248f6fe1b5003ffa5406a76f454ad93a60579b7
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
$ docker pull clojure@sha256:e3c34cf3b2fb1c8d1a9d23da93139bbf1d0670d8f67e583938aab6eb50ed0662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242873142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9086f7efb1c74277ccff5b9c6760f8edb0b50bd133eb7eefa5ebae931658886`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:55:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:55:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:55:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:55:37 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:55:37 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:55:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:55:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:55:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59502c1cdc1320ce54dd6b746a3746aa8fc2a6af0f0ceb06ebd21430c057e534`  
		Last Modified: Tue, 30 Dec 2025 00:56:28 GMT  
		Size: 145.0 MB (144966626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095920c2d2aedccaef641aea853318cc650ce8f557c800ddf50bc6f67b117adc`  
		Last Modified: Tue, 30 Dec 2025 00:56:23 GMT  
		Size: 69.7 MB (69677449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e759a8b236e0612bd056878c05b917b5916efd9afe01a3c1959b6095fb1f09`  
		Last Modified: Tue, 30 Dec 2025 00:56:17 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fac110f58abefa44be6d80c273d54721a4a65a5b6ab810ccf7f2e6c4d42a1967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d50114fdf19ff06d9db9394b4903588369a1560f616981f499e35394ce62ae`

```dockerfile
```

-	Layers:
	-	`sha256:cc424a6d2546a1f0949a898bb31c61d1e13540757db58978040c1c43a7f7397e`  
		Last Modified: Tue, 30 Dec 2025 04:36:37 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994576f8fb97da629366f3b38a399a2c0733122e91027bc483123822ca62891e`  
		Last Modified: Tue, 30 Dec 2025 04:36:38 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1afccbe7ff78ceb7a71236c4f6f05457227c6059197b7ca749d0193440e39a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239392718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed6cf97e783d5619074023a7e26e84c863646f1746c9a2f14b22735c3fa4a0b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:56:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:56:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:56:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:56:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:56:47 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:57:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:57:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:57:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b953184a5bcff83a5d0c900345e9b62026699d603033cbe8aa968f2a2710918`  
		Last Modified: Tue, 30 Dec 2025 00:57:38 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5091c5d13986e8f850d14e72336fa1275f245df01ce161846933d3ef3c2d1ceb`  
		Last Modified: Tue, 30 Dec 2025 00:57:34 GMT  
		Size: 69.6 MB (69558286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5285690a322377d9e4322fb2d218139748adf10a132aa2d3635339ac96ea1c16`  
		Last Modified: Tue, 30 Dec 2025 00:57:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d8b31793394e639ebe4ca23121ef251467bc98bdb45dc6f93a93c272efa9f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd8f17a593818443040a86e32812faca16fc0836234b881cd56d6a855b2771b`

```dockerfile
```

-	Layers:
	-	`sha256:af0ef9cebe20ccfc18cca3f6ad1020f34cf7bea872c45af2bb7143ec75517050`  
		Last Modified: Tue, 30 Dec 2025 04:36:43 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451a8730541510d87af34f648b8e03dc279f8b1b9e89eb1f8fe24ce2fed2b0fa`  
		Last Modified: Tue, 30 Dec 2025 04:36:43 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:69e0465009257719eb5f490352e7ab29849ff560cf983da2e1d5525d60f135b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239661120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ccccd4d88145d1fd99d1c9a78b0be166ba76520b3e530dd321c2517415d19b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:14:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:14:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:14:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:14:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:14:15 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:16:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:16:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:16:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d8ccc35fc31711a7931dd555a5784bc61992d973063264ed06d23cca9c64f7`  
		Last Modified: Tue, 30 Dec 2025 05:18:24 GMT  
		Size: 132.1 MB (132081964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260af39645f62526779a9353bab91c1f1a99c27a4803e39e57ba7727e13288b8`  
		Last Modified: Tue, 30 Dec 2025 05:17:40 GMT  
		Size: 75.5 MB (75509669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc2426080ccba654a2ec1e33817d8ae747a2e0d05e67c366969bddb9615597`  
		Last Modified: Tue, 30 Dec 2025 05:17:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d522b27e2a4ff6a7db9648ce9c52243673617e92fb14199d56102d298ec22f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bae5c05c0136f49bf5df0e5f0942d3d65462f7dae85a873b79135ed26c2c773`

```dockerfile
```

-	Layers:
	-	`sha256:0d910917a81d4e5d214f83aac30bb102fa4c92fde03891ff0a54f7cd4fc3c9d9`  
		Last Modified: Tue, 30 Dec 2025 07:34:59 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c292c8733303bccfb82795ba8dab85b870e86d42d6964ca70745dcf7d845c4`  
		Last Modified: Tue, 30 Dec 2025 07:35:00 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:811ea844dbd4f517dae7dc90fcc10d2a0bc3359a0bd84524fea86e851ca9c56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221068229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c5a70d8b1c711c5e0bca19d43613483c2f92e561fe912562e24edf40b1aa0d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:01:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:01:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:01:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:01:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:01:29 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:01:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:01:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:01:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecafc31a8cbbadb7cb515bdf13e00436d9fd6739120638d8356a4a42e35d125f`  
		Last Modified: Tue, 13 Jan 2026 03:02:27 GMT  
		Size: 125.7 MB (125694449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8db0412ed356785d2f7acb0b7fcb005d1e5e9bef8fe2bae413e2d7bbe7504e`  
		Last Modified: Tue, 13 Jan 2026 03:02:08 GMT  
		Size: 68.5 MB (68488721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d2542f4fec3d527759247338f313166106bf8a11487029c662829d9bfa44bb`  
		Last Modified: Tue, 13 Jan 2026 03:02:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f95e3424885d2eaf39d41ff5a63cbce261e21d07ad5aa09ca5d6190a0a6897b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195d6da755275b8484376e9159c3130b85b58edcec8672d41a77d02f43b763d8`

```dockerfile
```

-	Layers:
	-	`sha256:718b326b109c55aca4aa87decd0d7d20e48987fb20b93cdac99bf3cc2c24ed2d`  
		Last Modified: Tue, 13 Jan 2026 04:36:05 GMT  
		Size: 5.1 MB (5124864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81d97084fdd539ca337747e459eecebbdabc5347e74577b87be6d44f77b9c41`  
		Last Modified: Tue, 13 Jan 2026 04:36:05 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
