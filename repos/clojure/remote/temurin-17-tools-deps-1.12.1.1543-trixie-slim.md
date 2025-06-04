## `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim`

```console
$ docker pull clojure@sha256:da3832e3f636af17730c172c64427d53e5786d28579d228e01fb273184d31901
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

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:308f8dbb81f3b172ef175c7fc1805422fc0a4f195a2cbaeabd7d3ff2af4db0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249056386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9e1acc7c26694f95835b5a42cdf431dac6caff8361e82a6df03f69c5115871`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4652fe390832cb451f9074a7189cf88400e116c8ba451214832baa5e31766848`  
		Last Modified: Tue, 03 Jun 2025 18:24:12 GMT  
		Size: 144.6 MB (144635030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b0b95e69b1cef6d3b4f378f3ced88960ac514f38425c8f47d44c68e8ed4001`  
		Last Modified: Wed, 04 Jun 2025 06:25:12 GMT  
		Size: 74.7 MB (74664932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b64ed66bfdd871067facaafadb040b668f02523f966087601e4348e7addf49`  
		Last Modified: Wed, 04 Jun 2025 06:24:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4dac42524172d5f86e1999ee0dbb745ef9b37a9efa127e625dd546994870f7`  
		Last Modified: Wed, 04 Jun 2025 06:24:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:774fba473f9b9f84ad7c97c98045f05ca3a7c18d56a578829ecc288cb11d1363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8305ba9f8797e36f780e6cb9c990b6b4e02e05e74035af06d6d1853d072f6b82`

```dockerfile
```

-	Layers:
	-	`sha256:66f8d092cbab2a8311ee489d9debe8422e7b737c2331fa0e3a81d388a72222a7`  
		Last Modified: Tue, 03 Jun 2025 21:39:14 GMT  
		Size: 5.1 MB (5112065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46373f19334a3ee200d7d6814583d2d026d5043115b77d7c8aadc2cfd2dbcf56`  
		Last Modified: Tue, 03 Jun 2025 21:39:15 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17fcd44a4dacce109652ea2b251f32ad1da11c3eb1f40cc7e029fe47e1d1212b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248600604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b652391862e486aee304d9ae486b9b0bb18b9313c015936aef13c7e5cd6a9cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa191031ed8a3c8712cc547eedf7bf4ab856214d4cc0076e445d91663c3142`  
		Last Modified: Tue, 03 Jun 2025 12:51:45 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d34d62b80547811e3aad84ff332e03e3f74b25eb7de37c69ee87dc8ea31e331`  
		Last Modified: Tue, 03 Jun 2025 18:44:28 GMT  
		Size: 75.0 MB (74967462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c3d68c676e61d621e97cffcdee88c359459dc0a839ea2f61966f34d357c780`  
		Last Modified: Tue, 03 Jun 2025 18:44:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e53f85c134dc1beb8087e81cb8ce215bda680412682151a97f11057b3e5d221`  
		Last Modified: Tue, 03 Jun 2025 18:44:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:161500fd7ed75dc5084512698430b19da850535738f446910633cfa0c7c48c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30282af2dbf2edbe46b76d5eb7e879a62b2a93d9512be1fd04e113824c554389`

```dockerfile
```

-	Layers:
	-	`sha256:bc5416202a8f385bc14e3be004b7f9aef74c2d6c0958c1b5f581ad6fe04bd09a`  
		Last Modified: Tue, 03 Jun 2025 21:39:20 GMT  
		Size: 5.1 MB (5117834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf515870d9922b5ecbec4cb235dd00cbfb2e304b82b9256ec503a1d3fbd33805`  
		Last Modified: Tue, 03 Jun 2025 21:39:21 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - linux; riscv64

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

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - linux; s390x

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

### `clojure:temurin-17-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

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
