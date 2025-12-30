## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:d1bb3351975a3f4f3a59307289365b6ab3de561a7d04cdab10945fd3dc2417d0
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a258f2531e92ae538602f8d1e6ca63886baa2f20b38106689c5c00a2cfff55ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239661522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72bfcdbaa37fc307148bbf6b8ecf7efdbd7d2f6aea893ffac68b2d085cc2e3a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:17:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:17:17 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:50:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:50:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:50:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4470482a8eaaeab4dceb8ce35bb823da20ba2a67978f6a17163d36b3afe2763`  
		Last Modified: Tue, 09 Dec 2025 16:20:08 GMT  
		Size: 132.1 MB (132081995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed327483e2db9c7f805373164dcda71f1d7028e6df20f1e51b7c754b751441`  
		Last Modified: Thu, 11 Dec 2025 22:51:15 GMT  
		Size: 75.5 MB (75510038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9c0891562495a9f4e39e819ae35edc59ef26bbaaa8ef12b72ca65f5bf9acf2`  
		Last Modified: Thu, 11 Dec 2025 22:51:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:edf2b7fee1cabcae7f2f8488bdf87e0a0d5e350277b037610c075e248ca3e62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc78035e74800e974058372336257f4623e71426029cd4735541fe952e0bf798`

```dockerfile
```

-	Layers:
	-	`sha256:786ce4711d330ec99e3bfc45a70d162c47b3822475acdedf30134884322852a5`  
		Last Modified: Fri, 12 Dec 2025 01:35:24 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccc1aa307c94c562e6c52269bf90f61953bb5b2ba22b3840fc412498c6c7bb3`  
		Last Modified: Fri, 12 Dec 2025 01:35:25 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4a12cb4d6bc160048aef297cd6b919574f879d689295cbcd4db46f3931937b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221067028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d69fe91bbc556e2ea2a3ba0f7a645134bb245ab1d5e716ebd8f890c1d7a3d5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:00:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:00:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:00:04 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:01:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:01:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:01:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff53d604fe848c35801b54e3cd6935b79c58a7fcd5d1f56c7a5f2c6d134bb58`  
		Last Modified: Tue, 30 Dec 2025 02:01:01 GMT  
		Size: 125.7 MB (125694398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c4ffebb58f4db10e22c8228d2f6d321b9ee96a333115e68633cdb274c63fbc`  
		Last Modified: Tue, 30 Dec 2025 02:02:15 GMT  
		Size: 68.5 MB (68487588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667eb15d4c1d511a2f6c23dc078930ae67bdf9dacaf30c6f8361554e14ae6949`  
		Last Modified: Tue, 30 Dec 2025 02:02:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3998d36be1cb5174c34eb1e8af08389b15a9f4bd8f0fc26333f96c54909899e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543951e2a86a677e4636d77c662cdbfa06ca781f95cdf5e815a42d63c3c88afb`

```dockerfile
```

-	Layers:
	-	`sha256:542f7058a8f7fbb32b775160d8809cb591af8e77aafdfeff686ef9cda704cbaf`  
		Last Modified: Tue, 30 Dec 2025 04:36:55 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c7e60929959271550c3dd21f290c96996cb49861f0843c69e446dd9c15cf8c`  
		Last Modified: Tue, 30 Dec 2025 04:36:55 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json
