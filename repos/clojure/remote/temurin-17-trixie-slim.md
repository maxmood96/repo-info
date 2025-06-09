## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:1b8d5b5d54cde9b045c89d7d0c8eb181829a9788ce0195680e1e683dc6e6e9bd
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
$ docker pull clojure@sha256:5f28eb764a4fa2a4d9a59db69e2e02b8316d83a6934c2885b0f82134928fd19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249055271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdea47f05a3b1196aa8b94fbfb598b8495be26e067b76889ac01a592574b0a97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e513432e22464bd7da0f7fcd93fdb45bb58bee3d06b2c36bf82260f9706122`  
		Last Modified: Mon, 09 Jun 2025 19:34:41 GMT  
		Size: 144.6 MB (144634949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69861c5063c77015bff506ea216123e0810f3da51f083fe2aa695660a749083c`  
		Last Modified: Mon, 09 Jun 2025 17:19:00 GMT  
		Size: 74.7 MB (74663897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fc634be299b2142601220b3ee7d0d8d77c367a32b15d2ee2f30bff1e438fec`  
		Last Modified: Mon, 09 Jun 2025 17:18:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421dca674e66c2b9b0d9e712ff6d2fc4973740b1dd24dd45f72298fc381cb93b`  
		Last Modified: Mon, 09 Jun 2025 17:18:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b1b9ad7938e183cd4367f3e393bea90a5383e022c79da6489c21b82ceb8a214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71414063d58c18da0357c83371dba639d13333604f4b7cf38e88f0eeed89f2f8`

```dockerfile
```

-	Layers:
	-	`sha256:8d0517402431a98358efba6ace51b88bbb58e20fa105448e751b67b34f9e100a`  
		Last Modified: Mon, 09 Jun 2025 18:38:25 GMT  
		Size: 5.3 MB (5252284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e2cf9b5609a27049b438e81a457b316fbe2f26f8ddc766eba936f4749a6db2`  
		Last Modified: Mon, 09 Jun 2025 18:38:25 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f5c3f221300b8947166df14f7f9f77e0b7926322cea00fdb0b114e3362637e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248600499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46fddd64770ea0339c0e8a7cc01d5546b012e213ad1a3c01892dbeb2e3f9f27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa191031ed8a3c8712cc547eedf7bf4ab856214d4cc0076e445d91663c3142`  
		Last Modified: Fri, 06 Jun 2025 12:48:45 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf80e244821e65be1a09cbab69a3d8ee8fd7628ecc71f4003b6a027eb36f64b`  
		Last Modified: Mon, 09 Jun 2025 17:51:08 GMT  
		Size: 75.0 MB (74967355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f174435e639a44b467303a817621f43b33a79533e5b3a6b2c0c8798badad92b`  
		Last Modified: Mon, 09 Jun 2025 17:50:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e513901d64c8d6cc29da831fda489b66ef74c7e13697b10062a492765c4d2c`  
		Last Modified: Mon, 09 Jun 2025 17:50:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aec8bc8f04abf58644c77992d7091c5efba9794302b3a5f48906545fbdb6c282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6613c3f44e23621d6f85e8686d0c1c1df8c7d8210dac732bb7b6d4dc4e0c677e`

```dockerfile
```

-	Layers:
	-	`sha256:a5473e5db78878ad87357d0b25cdb6913b8c807c4a463b56df10cc702de78979`  
		Last Modified: Mon, 09 Jun 2025 18:38:30 GMT  
		Size: 5.3 MB (5258053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262b489a058cc74d315f9109daefd3613896f9b19033964ccc3799347eb2aca6`  
		Last Modified: Mon, 09 Jun 2025 18:38:31 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:15ac4feeb9016fc4ce373c5150bd3a40aa1c6be8ca2a469f8e31879c312be86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258264000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3d1605b28b0f3059dcddf3609588bd2e16cbb974cd320c65893097adf9b1e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe2f8a21171dd5775e8651cab944241a8c5250daaaecb5a5a99444957bad86b`  
		Last Modified: Tue, 03 Jun 2025 08:53:11 GMT  
		Size: 144.3 MB (144280520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce64bf212d62907ae43d89f7700b0438322ecd4fd0e4e17a11b585a7b81720d5`  
		Last Modified: Tue, 03 Jun 2025 18:58:08 GMT  
		Size: 80.4 MB (80401874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff4517376b89d5e17c2cc2e02f5a192999a3a723e9910db961e20140c0d2c99`  
		Last Modified: Tue, 03 Jun 2025 18:57:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6387d607db1cb8ebcba93972bfd168a27d340acfeba0b19bf22aab3c9c05fa1d`  
		Last Modified: Tue, 03 Jun 2025 18:57:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4a4745556e1d5726d5813fe93d29939607be7a83d664b888a3191847185bcd41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5847f14fa393d0fa75c91da7a302c87bf79c36ba3347a59dab123b32f1bd2e70`

```dockerfile
```

-	Layers:
	-	`sha256:ce30b74e2e60c837a25e163c9c529cf893478a02aae4683be7118c1e8804fedd`  
		Last Modified: Tue, 03 Jun 2025 21:39:26 GMT  
		Size: 5.1 MB (5116436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d703f5ccaa40fb43de7d012e56510e69eb7138285d521152e78cab489a567f`  
		Last Modified: Tue, 03 Jun 2025 21:39:26 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b11a546f5d37bf3e7c5e6afd5e6085cbcea26fb88f02b98c4ca3bf3fa3dad2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240046859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb053cf4cc740a1d47ddfc31ae880fca8489543ad4d37aaa4c4abb713350ad0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2900d390e81d9af67de96fc8c0a46074dae5d79691899bb1c249eff04d790cf6`  
		Last Modified: Tue, 03 Jun 2025 09:02:08 GMT  
		Size: 138.5 MB (138492458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c3f768d938265f4eecdcd3e1d2edac3aa4cc400d39c7ae1de1bbf4ae47055c`  
		Last Modified: Tue, 03 Jun 2025 18:45:42 GMT  
		Size: 73.3 MB (73308005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80374093b3dc83504532a48f6fe4f74fbe58b7225fde316649ae2febd2a0e9a`  
		Last Modified: Tue, 03 Jun 2025 18:45:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725cc206124549f72c20b1ea6ce3c0e4f9ae0a95aeda3582f6648b01995c8c7c`  
		Last Modified: Tue, 03 Jun 2025 18:45:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:911f6564aed1cb50e0b51671547c8a395d61b62fc90c05315a813e303c4448d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5115509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4388df33d91e98632d7a160a5311d98810ce4666d8719ffc9a1afd104241cb`

```dockerfile
```

-	Layers:
	-	`sha256:7a02f9fc8b907a17a6313ea5cfc2de06c1de33393ce8af87a9e89fed8cc114a1`  
		Last Modified: Tue, 03 Jun 2025 21:39:32 GMT  
		Size: 5.1 MB (5099610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e4bcb3784c694ab79a1a00611ff04dbe916eedc1a42cfd9a29b39667d434d3`  
		Last Modified: Tue, 03 Jun 2025 21:39:32 GMT  
		Size: 15.9 KB (15899 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:16d5e6a3416463e4015b16f28092b60201b773c1924e77398ba51ebe18306012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239910285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d37c58dda62f454ff0217d2e0255226b6a4d771e18868200eaa2bf31260a10b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89149c8ddf2f34bc00802d5cec3d426d775f8368fa79ab5455c34c0ba8a1e25f`  
		Last Modified: Tue, 03 Jun 2025 06:17:33 GMT  
		Size: 134.7 MB (134673567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9e3bd1c6fc559e24b01550c94539f58a3b8ea27c3ce35393cfe7faa0d7328e`  
		Last Modified: Tue, 03 Jun 2025 18:36:18 GMT  
		Size: 75.4 MB (75406057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9ef72f74ddf5583112a335da1fe842a869ebae043abb4307283844457d7d69`  
		Last Modified: Tue, 03 Jun 2025 18:42:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37ff66569e089375e171a3816a56971526e883faf0f024aaf8916cf3f55b74b`  
		Last Modified: Tue, 03 Jun 2025 18:42:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5048234668dfd5edc1b8b6c5fb93541d9a0798f628a2a2f7e97e8df58201473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db8a0477d8447db74a622cde2ec09d32a6dbb605e24699c2cf90d697c2c9932`

```dockerfile
```

-	Layers:
	-	`sha256:4dd92d39987c77b8d24105077f6f5a9907634bf7fb7a2196896025403b005279`  
		Last Modified: Tue, 03 Jun 2025 21:39:37 GMT  
		Size: 5.1 MB (5107989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be867a3b8b351077acfe7b35652f8efebdb6957028ed17f872ebc1a7b35a3a2`  
		Last Modified: Tue, 03 Jun 2025 21:39:38 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
