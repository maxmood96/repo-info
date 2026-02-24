## `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:8511246e9b9eae66c528bb56e01c144f26c9df02ec49ed83f9c7d464fb6573b9
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e18b0dd3e278575c6f46376ed667d130f6ee1e07f88c3ac4b47c8123c6c5f1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243543487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b595d2c8521e0d6c985cada01603b323be61e3909c708ff6b3bcd6457964c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:55:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:55:09 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60736bda4a126cde07eb9cfe023df12424cebb8f8097d50feadfdd582d1ed0c0`  
		Last Modified: Tue, 24 Feb 2026 19:55:46 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8dcd7011ca0b198700356e933d3c182e66f691eaa6ff380e1d0742ee215b6d`  
		Last Modified: Tue, 24 Feb 2026 19:55:45 GMT  
		Size: 69.7 MB (69677460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd16d20e1eb1cfdfd042ea849fed7a1d6fdb701eee048032f82af00dd966ec3`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ab166a7474605658c8f48f4e6f705167f5ac007f803618109f6aec8b93a27f`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f066beca628a76be006afa3d1bd511ad736e60fa3966205f52965e52856c5be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d191aeac6eb6be8899c3f4cb4dc6e7d72d49fc5f0acf0ac2bf21505d9b64618c`

```dockerfile
```

-	Layers:
	-	`sha256:2297ca580c396ba5c3a7485b5e7b3f13ad7bb0787ae441432c17971c0bb9a211`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 5.1 MB (5114654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7931e8414badd5b96767dae80a37334f999c491fbb845b622b4fff9622105e0`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85688ddc0dd8e2ef1464847425de0b6483ee58ac71fd4fcc2b170e4d5eaf5e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242225957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f57c4831acf0e38594be2831df977bf96606f7db319f251778e0d0ab17c86ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:05:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:47 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c2742c5137d1adc9a98d2d04fc2af2b324f40c2bb44d64cf745d7fc28fbae`  
		Last Modified: Tue, 24 Feb 2026 20:06:24 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93afdc5a90782f31576de5f1d4ac872726bed77f1c7a870252e50115bea3075`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 69.7 MB (69672639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc60605120f4162ac1cc494f9303cff558b93a3e5c963e611fc91430a21f25`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505f6dae05b13ab2d88ed57d5dcf8f0959c21b0ff693661921c025e5ee170e1`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec0a119fc5492aad752dea9ff79a5b2514011a348098cb093b5d156862f593d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afcee8b11c2bc86c0d38ebd6714459ce6be2b15f69c1ae0e2de4f749df01e01`

```dockerfile
```

-	Layers:
	-	`sha256:2069f65882dd35b955efd1086ea3aa4ce72b8a8e5249d61f57aa4f042fea74e4`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 5.1 MB (5120415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0c4660032702981c9f775c6b371e9de2b029e7d1d2baf00eaa522c7c0527b0`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce0034fb812d2f625f263ecb25cf3f6d3177f9b160f8b8c6ac4278a988a4193d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253022086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43938c27bbe760d6238cec7d25860fc144adc98a5d9da616ef02c5fc32a886a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 23:45:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:45:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:45:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:45:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:45:08 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:51:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:51:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2bcebe1436b2e06a46e1026a9f267beb7b738921e7b714b94ecc1b9526b812`  
		Last Modified: Tue, 17 Feb 2026 23:46:43 GMT  
		Size: 145.4 MB (145438175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404b6ec3a53c3fcaf85af756b1d9f106beba11002b8052a39a920da47c732d41`  
		Last Modified: Tue, 17 Feb 2026 23:52:22 GMT  
		Size: 75.5 MB (75514154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0478af211283e6b920c2a7f5af0c12421eac9e3bf79010f2ba852f42d6763f2`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3834b12747b5a7a489b1ad0b133814c01f8e8381eea7d7c649ca417f85b35d8c`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70e81ab2611d9ae9911f1249b0427847541ad6e384512cdd4afd1857c226ff65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed3ae80eb520c3958847dfa469b62fd5579b18290cbe868dea24e4ada7b46d2`

```dockerfile
```

-	Layers:
	-	`sha256:7b22a5270bb8abab9b39259a237c307c3e6e594c9817b1c0f5044b27851115b4`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 5.1 MB (5119812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c493a2071a6b4add4db49f2fbe0012ed27794250da486ee3316b1692ea60472`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8a12e361600ecfe6502ffe5c7f58ddc00609d0a6b5860f6d4e820522d4eff8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231002995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3576c054716134dc92404454591e05b1e589b9231d3b491d9dda447d7165c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:08:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:08:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:08:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:08:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:08:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:08:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:08:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e535dc0d305223a844c3403214deb9ebadafbe1230d72a59516621edab4af`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 135.6 MB (135627120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703ecc0c2437d5eb8010fe147bd4bf5d372dded03e1d0b8db9f89c46ce65c1e`  
		Last Modified: Tue, 17 Feb 2026 22:09:21 GMT  
		Size: 68.5 MB (68490448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b3f1a76f0898489211d80bddbcaffeeb88c940603ea4f1f787b2833721702b`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb938f5390d545f64e20ba9316904463d1b9618926c67f5a3c72b50b6801251`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e85c0390be761e67343263bcffe058c11c81f5bee2acb7d82c9d150bba2d45f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05ea605e322c32a7d2eebd822dddbf1d3c1fd253799e7c1cf821db4b047bc5a`

```dockerfile
```

-	Layers:
	-	`sha256:a2f0c8b4ec3934730679b56e87ef2b74bdec8e35fddc544c34847c2b301ab4f5`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 5.1 MB (5105975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73052c71733f33c0db0bc101c62cc0f8188fd4ec124ca0679ad167bbdf87615a`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
