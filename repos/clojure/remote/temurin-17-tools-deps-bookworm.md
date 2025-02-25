## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:efc4795466a30909257547f769ecd552a62f6a152df135f57996523c5090905c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:642a09eeb5bc21dd4783eb55a6026346fe48ee19053a4a19d42c5e10c4635498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274037845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9dae22d65fdd2873790e162ab42c6f6763867b7039b1b826cf7310d9f5e70c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d8f0d47dff0ce19b8d433830013cbb65165ac9cf7731cd27c9d558068358a`  
		Last Modified: Tue, 25 Feb 2025 02:33:16 GMT  
		Size: 144.6 MB (144566545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a775a1814762f04bc70ddc5a75f7feb59ddeb821c443c10df130e84ff581eb`  
		Last Modified: Tue, 25 Feb 2025 02:33:17 GMT  
		Size: 81.0 MB (80994156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68519367c62445d7019b8e784560c6f928c66d8f042b01ab0fa068ea7f554ab`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b7008f44cf4624da881fcec684d05f2cb41bd1637ed9628b8eb3860dbe76da`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:70fc9e2e943100222e0fcaeaee3f32746e84f968ccae39b1e97a76d55fcce19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5818d1ead06acf0f208bb7a242977cfe2c2ef6078a437c0a7d4a82111be172`

```dockerfile
```

-	Layers:
	-	`sha256:f019d1dbe63990252dce60154af6e8c5c431e088a1a800d068e60ecab54d636f`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 7.2 MB (7171096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d6ea11116c4711230ca47a5f707542d7e3927efa11180090d677be6dae57b`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc0aaf02b51bad0426fdb3cb48a0096db130bee8e23cc4dda2492094df7ecd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272606586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d7da7210581fd0a1b440603c6a9e7b77851a5dbc99d34caf9464c8655031a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece757aa0497472085ecc56d9989c1c60e5e6753869c29bf01bb2400f7d2e1ba`  
		Last Modified: Tue, 04 Feb 2025 23:42:45 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32cece22e6a1d58a283361b902e540de86d3ca6eab8287c8afea8f21f05cef`  
		Last Modified: Thu, 20 Feb 2025 03:51:31 GMT  
		Size: 80.8 MB (80844263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740566a2c093bcc89a81483ee8defe18f88a06981901d5e6aecef8e071119fc1`  
		Last Modified: Thu, 20 Feb 2025 03:51:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a55b19fb68963cc370df6c30ae66d99825d7771f02f81c4078b9e4792d44363`  
		Last Modified: Thu, 20 Feb 2025 03:51:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5705b7ed44bf9eb291c6fb3d1e758b2df3010df817bf35c5981590c127db6c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f2a26855ab4d5bbd11a7969ef63d1e0506a2702c11c0504e5bb960666b04c3`

```dockerfile
```

-	Layers:
	-	`sha256:54e0679c41228882c7b52fcb7b29185f244a8b5fe6080a5b5faeef733aef5f82`  
		Last Modified: Thu, 20 Feb 2025 03:51:29 GMT  
		Size: 7.2 MB (7176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e77f44ec568990c4a1d96e51462e08d333ff31a84138939ab3336fe1fd9d87`  
		Last Modified: Thu, 20 Feb 2025 03:51:28 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
