## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:a0df08333920c74aa84fd952b2fe8103363bd703c982742abcd991d44337c201
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:67cf1234986dbdb68b1b9b6e08e141c7281400531e05afc9e89c59f152e240df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190171076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31068a08e63d2b902880a1579f7798f1ea8bb103dd1a5d5aa0b3d28ca566fe69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:57:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:24 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c680aaf948313775edab478b261700c07edc015c5ae963a95225d1dbcc04c53`  
		Last Modified: Tue, 24 Feb 2026 19:58:01 GMT  
		Size: 92.3 MB (92256275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331c31d53782d34556ab16b292dcc4483d85066546e4ba0dd093954f9ed6523e`  
		Last Modified: Tue, 24 Feb 2026 19:58:00 GMT  
		Size: 69.7 MB (69677481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f090127a6ddec3fdf2ff8c9a32b1aa31d369a468af76906feae802a94bd7222`  
		Last Modified: Tue, 24 Feb 2026 19:57:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf87fcc5453fa2b80bc5d3d7841cd10d7efc2905866eb070fe33d7e25d8e2005`  
		Last Modified: Tue, 24 Feb 2026 19:57:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bda6a771908249c0ab4496122343fc49a0f2d11a22c5d303fc438722ab1f18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7985bbd5d5c11e294203f0ca2934474d17f95214779f52fcd3169e931da52ec`

```dockerfile
```

-	Layers:
	-	`sha256:b85f4f2a6f45f209accdaffcbd9a42cd828e892a0defe7b7ccbe60babffd8966`  
		Last Modified: Tue, 24 Feb 2026 19:57:58 GMT  
		Size: 5.1 MB (5082748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b978928346a31a8fda7112f2d12beb1929d8d0c381e9ce4241a10ad34f5986a`  
		Last Modified: Tue, 24 Feb 2026 19:57:57 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cbb7e99b68203843cd8ad2724b6c6f75ebe82e17b90da8dcfadbb0a520774094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189078083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599a0ca2707a8af0f780283c25fe5954133c49dbc6ca2b3efaef2ab18f3706d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:08:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:08:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:08:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:03 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:08:03 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d5732d5aa084fcbdd6750b258b128deaf3b98960d035ef5dd79040d0814c83`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 91.3 MB (91288264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4a0c19c3d97625ea263bafda71cba690192c34385fff1ad526e38e671de5ff`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 69.7 MB (69672699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1161c46c0e36d69d1d230930a64415d53315b2622ad929cc5b7428dc5e66a20b`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aef022da370b8d97dc407779f0068dcefed388e874bfb63ed5e1c0774acd62e`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7844cc6c50c106c6811208c5c587d587df80a6a1e359fd769f79163ec21002a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4d38c621d6374d488bc98efb1a0c37a04b275f4e93906a00b2cfa666847213`

```dockerfile
```

-	Layers:
	-	`sha256:ac6a0a44ba7ee64aebc515c60763175329b82bd9ad2b35dd15862c6d2a22d22c`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 5.1 MB (5088530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd47e0484615410fe2d50d7c0e4c9f62708e44909bad5f3e9f00bc0eda809f0`  
		Last Modified: Tue, 24 Feb 2026 20:08:36 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ba21ec4963ea21d4e0ae3efad26dfb2cc580d885f5a7f5fb4d413bf967f1cbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199216822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fc958b58d01acd7176e51f6ab2352e48f6ee5282ac77174baff581b6619cf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:46:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:46:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:46:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:46:10 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:51:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:51:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cb234547828975d01511eb3f1e2f07f4c3226976323dbaf0a3fe8832f8431`  
		Last Modified: Fri, 06 Feb 2026 00:47:43 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7d1bff7a7aa17d12bfad8d52d8030be45d899e876e5cf39f0f2c8d9fcfde89`  
		Last Modified: Fri, 06 Feb 2026 00:51:59 GMT  
		Size: 75.5 MB (75514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feea98bb1e6e49d6287c83e30989b16ea90787b12d2ccf31792e8ce47337c41f`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f3e6a206e0bf371d7ecce2d701cc3627bcb799a2f65be0b2b875a0a201c6cd`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14aaaf781f8439cdfdfd1c7b600c3afedeb03eb30c8af74c773d6cfd880379c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c90e9260012b338bb83095fa85b6e97cc9cd83c0a2b298f773ece7b14dfe71`

```dockerfile
```

-	Layers:
	-	`sha256:b14b64cc28c2b0c4a6b418ce8ef20746a12c684dba6be2ec8dba519a0697db23`  
		Last Modified: Wed, 18 Feb 2026 00:05:49 GMT  
		Size: 5.1 MB (5071230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a7855f8cd12557371e34e9d9ca4b864806a49d2709466af8bb837159ea0a48d`  
		Last Modified: Wed, 18 Feb 2026 00:05:49 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:54ca839f270a8981f4f94b595fd76bda843c0ed27a3e71a925501d076ae05272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183609736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad414b62689ed4a2a3a171fae02077cf778ccdf5eec3c6bbb165262ec167fe8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:18:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:18:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:18:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:18:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:18:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:19:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:19:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4636a94cb236173f2946325ca125ab41014db7d1266b07c990630f0108714938`  
		Last Modified: Tue, 17 Feb 2026 22:20:02 GMT  
		Size: 88.2 MB (88233848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c97c45197cc0e279cd8c3f369b2656351c10fa5ae8b60fbaf106e1a10ad7e1`  
		Last Modified: Tue, 17 Feb 2026 22:20:02 GMT  
		Size: 68.5 MB (68490462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc1943add3341b425e7e354cdbb4b9c7a12dc20d1a9bd073fd0a6c02777b07f`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5319830448305c9fb934be3699c4c723781e069c0e94f77e96bd17d6dff8d0`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9a131a57b8e920f33836d66f7bca87ae9ecdffdb32aefc35e948966f9e5e9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af3bcf39b3521153f8790199c9b368da700eb6d34027aaf870e1bccfec92cfd`

```dockerfile
```

-	Layers:
	-	`sha256:3330dbc2d44a7ab6bc4eb6b7461ebe3111f48d0a43792613ef7cf3cec7cdd4e1`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 5.1 MB (5058631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c19a37954aada8ba76121c51e498d115d8db40f769d42f6b5891a2c2b2aacdfb`  
		Last Modified: Tue, 17 Feb 2026 22:20:00 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
