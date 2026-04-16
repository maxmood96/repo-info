## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6ac71f66b1d704d90cb69d21d4959cee681cd212618986523507056b9a4d7b16
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4adb5e65a31420fffe0ae51b37e5494005db07d5ec477f0068745250675412b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243565158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d8142669fad3cc0985a617d471c267b581453fde4de9054d2c757651d26be8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:04:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:14 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445e9209bc7fffc61cc34dd35b140bfd31fce266977e15cea579a50c6678938`  
		Last Modified: Wed, 15 Apr 2026 22:04:50 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6305fa441cda656d27508c455dcb2f85d26d44310d409ddb11f44405ad358116`  
		Last Modified: Wed, 15 Apr 2026 22:04:48 GMT  
		Size: 69.7 MB (69699034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8796477b9b1b7179f822c3c97d01da2f6919c0c38f1336341d4ba8ec37c6faef`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37096caea4f666c5a390009519be8bba220f265aa2a43df398b4e8b94ad2aad5`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5f006678e20b25434f1a3da87f3237a07354bf011792b2a990ca4c09acdba63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643517ddcfda85125ad6ea72fac164cb7d78d4273eb4c9bf3d35a0d229273f9b`

```dockerfile
```

-	Layers:
	-	`sha256:ab5dd1cc40db9ecc31eda938d85cac3449267edca6847a8a056038b7c3bcf8e6`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7094ef20895391cb4c4b6d1a455133e9f49d0890fd33a3cc7e1684a991c9909`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 15.8 KB (15834 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:07285d534910d4c30230f74ac8559029d7bb0de0a60158a330a1f9baa70202ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242244514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ceaddf8c4fb9ca47f1435f7254a0af1ce6bba5b698390b635418814df0cb4a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:15:32 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:15:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:15:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe2eb0c07bca127a9a6f6c686331481ae65a65fd10aa1f5706be81f4c697512`  
		Last Modified: Wed, 15 Apr 2026 22:16:12 GMT  
		Size: 144.4 MB (144436254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5747a5caf67e27a045f61fc5542ac83792ebd9157f7bdc28960dbd6b4c6d795`  
		Last Modified: Wed, 15 Apr 2026 22:16:10 GMT  
		Size: 69.7 MB (69691049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1256204316d80ee6c01c7c9be1491a3d6b7bc8b08b396bf8ecf6ac5c550cfa`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511a23fa6ef3e6dfc7d041701d822f3257695663176a405c378f93d048b4186`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20e8a3dd3eaf85f9018fe722d22356a591359409ea6219a44a2f8dd1d585f481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7895f0a52f6d5c096da0ceea1cec6ff2cbaeb94f730a9f7572c3d9944d66936b`

```dockerfile
```

-	Layers:
	-	`sha256:28092115f3dc4d4253dcfb2d4d980dd600297a3ef6f087a04dea45016661439a`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1d2c11f4abb6bdbebe8b79c353bc98331ac27be4f899d75917ff8be3b60d00`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bad32db0664ca3fbd4f37522b9f7302c425853da6eceaea629a60ae06e226204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253051391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87133c6fb0ced1de4d0d092be1bb52ade85649871f6c05446acafa36605dfb46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:37:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:37:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:37:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:37:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:37:47 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:42:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:42:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:42:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:42:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:42:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e8da204b05d826de29378d25fee6dd2692a8f7fbf5cb6fc40cf39d76c6561f`  
		Last Modified: Tue, 07 Apr 2026 14:39:05 GMT  
		Size: 145.4 MB (145438191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c532308bd3954dc130ad019dd1f55b8c7e5cf8a7dcda39142256be6085296e`  
		Last Modified: Tue, 07 Apr 2026 14:42:58 GMT  
		Size: 75.5 MB (75533693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975e711b99648b74e2c7d4d8f6a3a7bd63c8f3db9790b4547e15870924f33161`  
		Last Modified: Tue, 07 Apr 2026 14:42:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1244de520cc2e610720336d4902e98b9c0f3e87a8f88d7270663c8375afd27fc`  
		Last Modified: Tue, 07 Apr 2026 14:42:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0950ade2d742079df2a115295ae5567f9bce8711c398c61e7c2a89207b09468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67624d919ffed094b481a80609d7dda9df28c113e44fd9bd87c9f3c4e83583ce`

```dockerfile
```

-	Layers:
	-	`sha256:551f953896174dca014299f74e1b92f2455192fdbd843f997947ba9eede3fce9`  
		Last Modified: Tue, 07 Apr 2026 14:42:56 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4533b6c5bae9710b029d3df65a97ad1b2f6c43f9df4feaaf7d952ce09218f12`  
		Last Modified: Tue, 07 Apr 2026 14:42:56 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c49bbc8756d5b5196ab0a2e3fbb03442e84432c32f2916a3136aa942105eb68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231033220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2738466ae56fe12f78ff1da6aac23d61ece6c589bd8d75d30e968384d3aaaf98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:41:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:41:51 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bb5c429c7fc69853b04b7b379880a199d321686ac73dcbc03c18f0876fec8`  
		Last Modified: Tue, 07 Apr 2026 05:42:27 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f953c4f5e6f098875cf19eb3db5ff7d0abfb254428c68de93299b96694c4a`  
		Last Modified: Tue, 07 Apr 2026 05:43:27 GMT  
		Size: 68.5 MB (68513692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cad3a8df70817bf4981b9ebe26551ccb21cc70c8b26dd30b94797da4d2da1`  
		Last Modified: Tue, 07 Apr 2026 05:43:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745761857dea9e94755cf32032e4a4215a981e608a8d912f33b09cc33cf31b4`  
		Last Modified: Tue, 07 Apr 2026 05:43:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09063ddd60eef1525e8748509cfff4651cc44b2f07a5b7c4809e7272476eea09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c971cae8112d07562f318b8529eb3503362e15dcb8d3c1c97cb817f91f437e1c`

```dockerfile
```

-	Layers:
	-	`sha256:de5a1f01aac64a7255a51b81341e53932ce7c5c51eccd6edd909a8f9156c875e`  
		Last Modified: Tue, 07 Apr 2026 05:43:26 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c4075fc07f7683aaf788fe5d1e0680958d9409a6b9cd8d0a6920dde10a44c1`  
		Last Modified: Tue, 07 Apr 2026 05:43:25 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
