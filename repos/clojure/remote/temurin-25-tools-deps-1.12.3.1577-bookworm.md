## `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:d3d94e6d67569fbe3f7a450f804ec590f6a412f9390a8bee56440f2ca3882fc3
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:501b00512601dbd87d0df3af83de0fe0e851345ac7e004fa8071474bcc449905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221662954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d629103e827a11e27f56fa1c206611103bf8eaf71a6a8f20e098df8800dfdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de3c803c78f86ec8fdd124bfa526c2fe0537b09e51108368f2de3fc64137b33`  
		Last Modified: Tue, 30 Sep 2025 00:56:30 GMT  
		Size: 92.0 MB (92036051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbc659be69a9df86a90fb25271879efccd54545dda86d60e89ca086fe698e7`  
		Last Modified: Wed, 01 Oct 2025 16:15:57 GMT  
		Size: 81.1 MB (81145307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43f9be7c24fef1bfebf75e9b30c74753d3d3f30053ae6bfdff5a17973161d61`  
		Last Modified: Tue, 30 Sep 2025 01:39:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aca36e864ce9e9289cb663d1d2014ef76165935695ce43141594a3d979e95a`  
		Last Modified: Tue, 30 Sep 2025 01:39:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ed02239e427b254822b99f7ec39e99671926767a81daee653ffd1c35d1e8061c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490c42ad42b2ce062e90bf0a6c0c8aaae0a72a4b95833ba21448b54afe43ed16`

```dockerfile
```

-	Layers:
	-	`sha256:7caddb34cd58d2fbf41523965bcccd2d766aa630d4bcf7d695beb2ad201c763c`  
		Last Modified: Wed, 01 Oct 2025 15:42:20 GMT  
		Size: 7.3 MB (7327540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090ebe44fab7b70641f30f55d795439983125e686857ece35bf24b07762fe1cc`  
		Last Modified: Wed, 01 Oct 2025 15:42:21 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f4b88745d12aaf67ba76b9ad94c137888463665ace26f933d3f617a6cdf930b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220433499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79202e1d7f037e7a4c042fbe5ea12325549f9f9f27ae537de5c9c3df032a97cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3866ac08101de08c5f170e3171ae8cad60aaea9bcd54aff259e360bd6025cc8`  
		Last Modified: Fri, 26 Sep 2025 17:56:26 GMT  
		Size: 91.0 MB (91045253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b6318812ffb6e71ffce05ff3bf319963756302f42483d8b2df2860ed719627`  
		Last Modified: Fri, 26 Sep 2025 17:57:13 GMT  
		Size: 81.0 MB (81028187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416ddc8dc7b1808588de63815f6521707c8bf4a2704b526c36563c4e90099509`  
		Last Modified: Fri, 26 Sep 2025 17:56:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306f36de681ad529605cc06304ae1d96eb80f5a8d3126c424d3ae297a2e26f36`  
		Last Modified: Fri, 26 Sep 2025 17:56:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f206e1467479ee04cd0d049f7ac5a818182ea6652d1ae210188f00abae59cd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42dc718384c6c56bfb36392a49d8da9c5bc54598c4987284182c1d4ac748a0fb`

```dockerfile
```

-	Layers:
	-	`sha256:2f0f1a68d82f3150fd9bbf1c26295ac4584ebbb8010fc8d2dbcb9c3b2755b070`  
		Last Modified: Fri, 26 Sep 2025 18:43:50 GMT  
		Size: 7.3 MB (7333372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f69676a0d2fa074af9327feae528af3e792c28330d672204c43b9c554887123e`  
		Last Modified: Fri, 26 Sep 2025 18:43:52 GMT  
		Size: 18.0 KB (18004 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a9aecbbc2df10ce388cd2e08794a2c3792d40ad5e129463c594eef66e51b1cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230910328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30efbcf0426f5b5cf2ebc8033cc0cbb9f20af43e22c473facfd490fdf58512f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40adee7564f2c9c2e68b70cbb9b73d3429060948d5a0a001c8c14d1b365e7826`  
		Last Modified: Fri, 26 Sep 2025 17:53:41 GMT  
		Size: 91.6 MB (91601753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed47c892fceeefd052d1e85b1335daefce04437d3bfde6d46e59eba751cb3567`  
		Last Modified: Fri, 26 Sep 2025 18:38:21 GMT  
		Size: 87.0 MB (86980713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a51806fb4a12a79aaa8af0b15b4d87e8272b9d52cdb714b18c626f328f7a37`  
		Last Modified: Fri, 26 Sep 2025 18:38:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48eb42380ca12dd2fc83a4d3442aadfb979ddc9cf4f14eb17f3f1df4546330f0`  
		Last Modified: Fri, 26 Sep 2025 18:38:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1f22fc77c668faf2b254488f64f0d85b672a7a7ce03d01f3af97422d184daee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88285f18d44851f51f1c523d6e890177872af879afe2e7c23fae89fcba91e85`

```dockerfile
```

-	Layers:
	-	`sha256:1c506292bde320b3627cde963a01f5037c56e7e936dbf50183b612c4dcdb65bb`  
		Last Modified: Fri, 26 Sep 2025 21:40:54 GMT  
		Size: 7.3 MB (7334088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2617f33614caee7de0ad4bd7ad32fd13e7663db3256f3ea0f1cfbbc83ae580`  
		Last Modified: Fri, 26 Sep 2025 21:40:54 GMT  
		Size: 17.9 KB (17898 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c43c69fd1067fd517ed0687cbf5a041adea9e264c3fdf0355f58e7f34c80fa54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215300875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f7dd08957ee370e0e471811ddc77453689b93f0bd86efec74b00689cb73a92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe3799d583306df2ba78a61ee5b66b91b84d986ef666523b05e98262da10f06`  
		Last Modified: Fri, 26 Sep 2025 18:42:30 GMT  
		Size: 88.2 MB (88206399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc76c9216f8226fb0cef06113b16f59b5f6437b592bc0af2ce8c80f1b3fe5d7`  
		Last Modified: Fri, 26 Sep 2025 19:37:03 GMT  
		Size: 80.0 MB (79955892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6443e3c4bb06a89b9ba2689c79e521f8c742300c23cf8ff618684406a2d4ade`  
		Last Modified: Fri, 26 Sep 2025 19:36:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66099fef22b06831b9c6e2681c8a8c8c98e4718b2108315781dd670fe5de0f`  
		Last Modified: Fri, 26 Sep 2025 19:36:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b800a1697cdbb0b272626372df06b9fc30c19ae3563b6ea5841c0463e00b2b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045a0f622e189f3870ac22a7617585ccd6fe1fb13bbb12a1dfe2445b81a293e7`

```dockerfile
```

-	Layers:
	-	`sha256:6eba486e1ddc504c57d83d9b58f96c8d77607b9d2ea8a27b5cb63f40f6d22396`  
		Last Modified: Fri, 26 Sep 2025 21:41:00 GMT  
		Size: 7.3 MB (7321407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e8edce959d268592ca72f941ea6823c275af642819486db205f22279d1caaa3`  
		Last Modified: Fri, 26 Sep 2025 21:41:01 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json
