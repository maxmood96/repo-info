## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:63983b28afccc1197081f55330b388a4a4a304f49a191544cd24b0c5ec972b9a
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
$ docker pull clojure@sha256:8ee2feb43209af6b9f35d512f4d766eb196820736355a66c9bd80bf7b4f94497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246450718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d171c2524c45c7cde28b3a5f02fef0b3d90338d12bb233fa781d0e55d9a6439a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f29d863292760475f74c5948ae02914a5a959de6ef99285f09875341a7f75b3`  
		Last Modified: Tue, 02 Sep 2025 14:19:08 GMT  
		Size: 144.7 MB (144693356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e1c2a99fae520737558a491488040f2e0c0553829ec0ca38435b1e046ff382`  
		Last Modified: Tue, 02 Sep 2025 00:17:59 GMT  
		Size: 72.0 MB (71983033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d53b8608fc174f751c78eee4250a00bdc610266991b7c497945977a8c47723`  
		Last Modified: Tue, 02 Sep 2025 00:17:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174b356b59f40982b6f43db0de8577456d21dc02b4862546c004240c3c1428e`  
		Last Modified: Tue, 02 Sep 2025 00:17:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b24d281bad163c0eacad86ab9195f5d3d7dd0554c8d029255300e9a49714d63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2d630172b16a40fbaa865d38d3822aafa2a4fb8fb2bc872880a2c41f6ce20c`

```dockerfile
```

-	Layers:
	-	`sha256:8ca7c23b52d59ea16a42423e1f815453bde3b926fa308a050bf176bf75f33cbf`  
		Last Modified: Tue, 02 Sep 2025 03:40:21 GMT  
		Size: 5.3 MB (5255237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d035cf627bf41b1a5de626ce56ecaf7d8ed4ac0e50388cab744b63e06073ff2f`  
		Last Modified: Tue, 02 Sep 2025 03:40:22 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:264d54c315035a7a04720a77592c0daa38499a782ed928e5a6b6c9ae77fc116d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245483056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0a358bf988e2220063f746a82c7c0485c6284acb70b7bcb1923c37035e9164`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee34086bf2ce6424ee32c4273d500b58ad791b413d934c51d0a7ccc27d83cec`  
		Last Modified: Wed, 03 Sep 2025 07:57:34 GMT  
		Size: 143.5 MB (143542200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a118de65b6491625110a6b6a152dd6af078edb34feb5b47a956f63f80bb2f3`  
		Last Modified: Wed, 03 Sep 2025 07:57:31 GMT  
		Size: 71.8 MB (71803769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8b4450780649a5990a33fc8f9c803b2e66f8b86d15f00e862381830406a096`  
		Last Modified: Tue, 02 Sep 2025 08:58:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3fcbb3e925090b01350593c1f0586b3781778086e9cbba9dfe308254d46df8`  
		Last Modified: Tue, 02 Sep 2025 08:58:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab5cad081770f873fc7c4f310f81589a21827dc02802b20726d2f507c0a01218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c697c3b0bd428d3268fdf8f15e2cf36f976903c8fc6f9debebdc97f9bdf972`

```dockerfile
```

-	Layers:
	-	`sha256:1e96a66e10b22492366787cdf7d7b6250a1e54d266959d4ed266a2ae856c09ee`  
		Last Modified: Tue, 02 Sep 2025 09:40:04 GMT  
		Size: 5.3 MB (5261006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9862f18f819e87103b6b319250720ac0eeb061ed527f9a044addaae8739482`  
		Last Modified: Tue, 02 Sep 2025 09:40:04 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f278c8399c175dd5747f1b5af4f65e34448500e882f4c7119f6924b071a7413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255356668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e44e5799375193c3ed6f56064fda3df04124bd493ec1de013f93f30a5c55c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b349faf7983fce1c8ca2fb5d8c746b906568d15aab429edb60743a6ee7e0744f`  
		Last Modified: Tue, 02 Sep 2025 08:40:28 GMT  
		Size: 144.4 MB (144372651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb17cbc46acc79b35677b4aa3d9ec5ac2d7ffb03ad07b4d6cf95abaae4aa833`  
		Last Modified: Tue, 02 Sep 2025 08:50:19 GMT  
		Size: 77.4 MB (77388760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b3c8ba72eb7ff76dc70330ab35223616b79ad39b2afc2964106777beb9bcba`  
		Last Modified: Tue, 02 Sep 2025 08:50:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9db1258ee7a53d92e3e592c38e163a13a83bf967186a82b31ac213588204546`  
		Last Modified: Tue, 02 Sep 2025 08:50:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ea9d7e495f9a1a236f076bbf4f8e9a7e6ca8b2e9e8e0fe4342435d12cd7d92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2d6d88d0ee4b988edc21305e0c724ec797752924f83c2cc790514b28c1468`

```dockerfile
```

-	Layers:
	-	`sha256:8510807ff5fcf9d906dee737798d254172af38577dc1dda306c29a86a7a03556`  
		Last Modified: Tue, 02 Sep 2025 09:40:09 GMT  
		Size: 5.3 MB (5259608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7098ca736044413de4c483596abe9fc389c0bfa68706aeedaebf9b528d285a40`  
		Last Modified: Tue, 02 Sep 2025 09:40:10 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:497e19f9731e7ffc4b5683dba2a72c16403611c50226cbf9c52f4ef87653ac54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237724255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e4bd04d70263d6f6c6cc5234b1d92037d885639b6ea23ffca5028dfee4f9cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4003c8df477a56c140d3903d6cff477740baf1dc3729dc456ec4837e6f283fe9`  
		Last Modified: Sun, 24 Aug 2025 02:06:17 GMT  
		Size: 138.6 MB (138575688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87158597cc3d80b4f2093dfa5a1e19d4cb29fd6c7fa2a8a264c59e8cc501cc3`  
		Last Modified: Wed, 27 Aug 2025 09:13:28 GMT  
		Size: 70.9 MB (70875898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9895235db1164df00eb1e382d6e29d5158336bd86705e5e83efbeac5b594f5c`  
		Last Modified: Wed, 27 Aug 2025 09:13:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e24d27fc290119c0e63edc8c3d4e81e59fc7370f9d5eb490250f13faf8d857`  
		Last Modified: Wed, 27 Aug 2025 09:13:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd792c2fbd1fde43ba3ad69f64be13ab0046aa3f1bae9abc319f05dcdad636f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ef738175a469794a21a725097bc4f7ded2a23ff9000bc060db426eedc20a6d`

```dockerfile
```

-	Layers:
	-	`sha256:bdc73ff082b2f693e38da22a5d2b6f43afb6c3c89fb682735e6803bade8e587b`  
		Last Modified: Wed, 27 Aug 2025 12:35:46 GMT  
		Size: 5.2 MB (5242782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d23b239548b3555a2b3196554f52c84fbdebe0f3ce07dae3d0209574840ee8`  
		Last Modified: Wed, 27 Aug 2025 12:35:47 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:be2186aa751b9a00925e99850a236c970ee6b95817928caa581828d0d02913b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30881328e6227a46a74d41d9e4d541fc27602274a78588bbd3af3775016cc602`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a1e9e470b7c88bd21688fbc518ea5bdf98b1d2fab1ef9fc4455855387c7eae`  
		Last Modified: Tue, 02 Sep 2025 02:01:48 GMT  
		Size: 134.7 MB (134724306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd9c40373aef1f01b7679f0a307a4d51e88dca4638c77791d3733c7709fa66`  
		Last Modified: Tue, 02 Sep 2025 02:08:44 GMT  
		Size: 72.9 MB (72949443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d059112eb820eb91b568592afadf6769ab48c854df04cf5d6ce27f42ac5b96e2`  
		Last Modified: Tue, 02 Sep 2025 02:08:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7edd659a911a3da9d638710d7f6c89b84c6f0651696f7844536432926ff2423`  
		Last Modified: Tue, 02 Sep 2025 02:08:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce54678c787db9e1418398a1203cf03b2c86241bad9b2b1d47b423e318f68816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fa85f436f2654ed94f1d35d6163afd49515b7842bc572063811cb6e9e52076`

```dockerfile
```

-	Layers:
	-	`sha256:a2750e1cd266f093ff0aee03ef951803c9a244c236db306a8a96be9d0b093b32`  
		Last Modified: Tue, 02 Sep 2025 03:40:47 GMT  
		Size: 5.3 MB (5251161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1ab089ac12b1d8b8a259f6a9f9f8ca986c120865fdcea43a4ff895e25aa02d2`  
		Last Modified: Tue, 02 Sep 2025 03:40:48 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
