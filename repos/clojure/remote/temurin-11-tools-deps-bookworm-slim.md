## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:1860aa3feed691af083fe44fe87b4844a4f565e198a732bd8103a9aaa5cfdc59
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
$ docker pull clojure@sha256:0ad7f29303f9ea806673301bc4a5666135dec0b1038ab856f363fa75c37f1967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242873314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f220e5021f798035b996db98c8e0f7e18f6fddada879337b5a27203e5a4734b4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:19:43 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:19:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:19:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:19:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8ca222c40fcb5e2501810db248a7a583daccfd2a25c3adacad78fbe51ad24f`  
		Last Modified: Tue, 03 Feb 2026 03:20:22 GMT  
		Size: 145.0 MB (144966653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a4977b0dce7f340bffe6664e8733146a1df0e3759ea655285dc2fd2474e48e`  
		Last Modified: Tue, 03 Feb 2026 03:20:20 GMT  
		Size: 69.7 MB (69677528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19143627ab7bcc78d44a2974d6c55f5e160358dd720e9b2d93b345c434cf72f`  
		Last Modified: Tue, 03 Feb 2026 03:20:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b12109a554f5f5f2d9fe292c659bf32863cfceca00059886c14c10ac4426ee3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73eeb4fcb57df51510665f9f0a925084cf67d86dab97c627ffeecfbaa69d33a`

```dockerfile
```

-	Layers:
	-	`sha256:c4bd2da9b419cc76d11a6fae75e745eae7e0a57b70f9af9c5c2d67fa661f5d63`  
		Last Modified: Tue, 03 Feb 2026 03:20:18 GMT  
		Size: 5.1 MB (5133541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee0ef68bf681eadc36c9a6f01b3e0a4fb64f51cfb462657aefda250115f2229`  
		Last Modified: Tue, 03 Feb 2026 03:20:18 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b448eab9c02f85cfbbd8b0bfff306bfd2c783731ba4f7c2135481a765bc20a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239511182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba87bb2fcaad1c516c19aacba5acfea930f5445087dea89461d2ea9444580d8e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:09 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560f18c60b3632f3f29ae81d0429fa39a0cf25bda5ef7ef79edb137b1cc0e15`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 141.7 MB (141729908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a6df18faa19ae16b36c09abcfffc33c7fbe31680a187badb64d5e8932a5fa8`  
		Last Modified: Tue, 03 Feb 2026 03:22:45 GMT  
		Size: 69.7 MB (69672806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7db922f117ed4482e2eb86d3370529aee8c150e667d4f70fda3e5b866c664d3`  
		Last Modified: Tue, 03 Feb 2026 03:22:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b4b24672391400946a1b48c375be1b4c7730253b3623d5925376214bf58c3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691954caf86e4dd50435c8bb21fd2ae6f69eab96118e54a538f2193cb020c3f5`

```dockerfile
```

-	Layers:
	-	`sha256:9e293ef4598e21adbe83a4ceba96a3ebfdf62c0cbdfc669bb13141fc99a228c1`  
		Last Modified: Tue, 03 Feb 2026 03:22:42 GMT  
		Size: 5.1 MB (5139920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55e20776df282a4c0fc6cf2f03b027e854bbb082db5aaa5861a3f4843f4f0bdd`  
		Last Modified: Tue, 03 Feb 2026 03:22:41 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8a719505e55bf5274845f05b9736a23a4d6c5205419d470a0c72f5f90fafac85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239662939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802796e779dd9ec71221df2d0810ecbb5647e4264740e57cebb8716c87445591`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:34:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:34:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:34:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:34:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:34:51 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:38:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:38:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:38:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91775ea6b360b47d3003bf9fce8b6bfafc6000ef76da1b159098b664cbe3f91f`  
		Last Modified: Tue, 03 Feb 2026 09:36:05 GMT  
		Size: 132.1 MB (132079761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f9db717270b7ff73031d268718145d34677b00a2716bcbe2548a4d48874d7b`  
		Last Modified: Tue, 03 Feb 2026 09:39:00 GMT  
		Size: 75.5 MB (75513818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e37526324407546fff442bca88d861409791fee2f5a1f08601ac6f79bad8a8`  
		Last Modified: Tue, 03 Feb 2026 09:38:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:046b4a57a78ff74614a494742db9097c7c7b6fcba10cde1b57e17461c3419e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7272ca81d280d9f605f60bce364469d257f43234fd777b81846855d69b7df162`

```dockerfile
```

-	Layers:
	-	`sha256:9a6df60f12ae841d21e1a186b8059e12a3c103cbf61c1ac4cfb57b8cc63d44b5`  
		Last Modified: Tue, 03 Feb 2026 09:38:58 GMT  
		Size: 5.1 MB (5138084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bfff0941854a61012d41975d269f7d95a970255af4855713e787f705cc42dc8`  
		Last Modified: Tue, 03 Feb 2026 09:38:57 GMT  
		Size: 14.3 KB (14314 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:579b8e668057bb6d25b11e2ddb325fbf4bd65c10ecfd22963482eb2d00865c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221069715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93654d47b3da4423221fc7d9efd31a203ccb4cee6feaa5e471d1e0cb182820b4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:00:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:00:47 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:00:47 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:01:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:01:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:01:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b3591739c8d13426d26ae562b07944292bea51d804a77ffef024038f2ef0b9`  
		Last Modified: Tue, 03 Feb 2026 05:01:28 GMT  
		Size: 125.7 MB (125694835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adda30ae1ff7fc252e52fa452c8ecb2f19528cbcd326d5074b07df5ab42f686`  
		Last Modified: Tue, 03 Feb 2026 05:01:28 GMT  
		Size: 68.5 MB (68489851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14842f586948e163a4cb5986c5ed2a978adba3c5dc0219b267ee3ed6b0d1232f`  
		Last Modified: Tue, 03 Feb 2026 05:01:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:155dcb11ef81e560c41815a78a65d74f6143a52726ba8188ac3529a99b8e16e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de2f3dbcc7bd2198d688cc4ef60fa1e8b6811fe4b07f622df650c02f32d2f42`

```dockerfile
```

-	Layers:
	-	`sha256:2d81b10baf0ec1de50375ab2d622c53b0a2d0af7de7616ff4e44e85b172045dd`  
		Last Modified: Tue, 03 Feb 2026 05:01:25 GMT  
		Size: 5.1 MB (5124866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26fb217e3f19352528d1c1ae6545e86cf689c7bb93278ae6260a7e40f22417b9`  
		Last Modified: Tue, 03 Feb 2026 05:01:25 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
