## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:4e78d5a47979ed613544306bfa32f2511152e29b04593e6b3e430f6dc1983e7e
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9ec10fb02a0de4110b852fb9284aef2abbfdd5af5a01938c0dac17e2ef803cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292655610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76662be622076ef5c74cd0088c82f6c49d63053f12a5c1e642417f3833e6322d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:36:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:36:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:36:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:36:28 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:36:28 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:36:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:36:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:36:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:36:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:36:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558fee7e4a87e2b718e22b89e9461b1694a9102e23747f8a65b25344f885617f`  
		Last Modified: Tue, 13 Jan 2026 13:05:18 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb56682a365c9e50864ea403a4089b6c24d1220e3309d8bf5863f1d895ba3b9`  
		Last Modified: Tue, 13 Jan 2026 03:37:23 GMT  
		Size: 85.5 MB (85542905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d45e5cfe6962ab6b379841ade55d9134117b83a44c789a252cb9dd6255034`  
		Last Modified: Tue, 13 Jan 2026 03:37:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9669c4f869b03f27f591884beb9df35e99462a4371747e01097145994880e7d`  
		Last Modified: Tue, 13 Jan 2026 03:37:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8e9e8ed30b5e5a2eccda1370e4375fd78558c2a1c3b16918ca6875d553e4b073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76a416940e06f20e8cec3a50d71569d55a250bb3b5feaea65c8394fc970496c`

```dockerfile
```

-	Layers:
	-	`sha256:b803b7e765e5f2345ffa63030c0929fdcac8cc79eb82d1e46e43c2d2df2157f9`  
		Last Modified: Tue, 13 Jan 2026 07:44:37 GMT  
		Size: 7.5 MB (7470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dfdb6994e167428fbd042406940198a8414a487d03a742175eda925cf75812`  
		Last Modified: Tue, 13 Jan 2026 07:44:37 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9d026327f0f7e8ffb9d2c8a7e0e92e0f0e5cedd4e839aedac3ba475ae2da7d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291117995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d846dbcf027cde7beafff18d03e6016ef8a820f2ebdcc7bb94334007cdfe39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:40:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:40:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:40:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:40:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:40:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:40:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:40:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:40:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:40:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:40:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50103df3b22742a97ffd780d056298bf2f8c116260a3b1f5bb398d1b828194ed`  
		Last Modified: Wed, 14 Jan 2026 13:17:57 GMT  
		Size: 156.1 MB (156107655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521860dc24dfb20533e73d11bc46d6c57ac4733f29acc6e649167847fd169ea4`  
		Last Modified: Tue, 13 Jan 2026 03:41:10 GMT  
		Size: 85.4 MB (85361220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddf363523fd9d505babbf85cba4bec15861912086fa473e69e8c6f3989b0421`  
		Last Modified: Tue, 13 Jan 2026 03:41:06 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e712d2ef9fb2c050dab5ae101780f8451c8f5b74c0763b5f1ea74ebdd6b8f63d`  
		Last Modified: Tue, 13 Jan 2026 03:41:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f31bdd141a81069fef9ebc4be79d399a8b5091ca267b3f55cbb3416840614a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1361ad6d22fcc57fd98fa93e64f7b1ec427f6cfe11a26c6a5a1fc79da80cfe9`

```dockerfile
```

-	Layers:
	-	`sha256:34d7d094f5b9f14d5d43316642bee17c8a244d4e8b9a90d9a30b191180901ed6`  
		Last Modified: Tue, 13 Jan 2026 07:44:44 GMT  
		Size: 7.5 MB (7477958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad230f2596bec13fecf92477d519c94d16007fcdc71c8394a9fddfc6ee57742`  
		Last Modified: Tue, 13 Jan 2026 07:44:45 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2d486fd1f7e49946d8f389a9bb68b73c98fb8ecd144d6f203ec9e01ea9281209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301999340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a171a7cd69c2bc958a3b7ec22611d7f3ec822f575ea677c3d3919188f29d9101`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 12:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 12:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 12:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 12:22:55 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 12:22:56 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 12:25:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 12:25:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 12:25:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 12:25:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 12:25:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb1fb4376f306eadaef720e8550fee0db4e7f2f64a3c535d26f70b6366bf18c`  
		Last Modified: Tue, 13 Jan 2026 12:24:34 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cafe75fa9f83ab28666f37f5b6f91f28bce2ea9f4edaee38a653f3579d10d42`  
		Last Modified: Tue, 13 Jan 2026 12:26:32 GMT  
		Size: 90.9 MB (90948386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb4f8d9a5340bedd239319125011e1a897b400b21c8d688460540c42218195`  
		Last Modified: Tue, 13 Jan 2026 12:26:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008bf13301bf5996dd1781ed8b3844427002898a599d3581a26bc706adab314b`  
		Last Modified: Tue, 13 Jan 2026 12:26:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:54be3162f4eb4dbfecc0c0bd3ae4b2c626feb5b242bc843a1908a952fde919db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561b0725f3d666af536d160863f8f6acdbff465d81eafe37684d79355807dcbd`

```dockerfile
```

-	Layers:
	-	`sha256:b649aa2926955f20e906364e61a8ac508def36ea1dd643b7ee31ee54d89e206a`  
		Last Modified: Tue, 13 Jan 2026 12:26:15 GMT  
		Size: 7.5 MB (7475349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27f2b4ed6fbf4fc73fe9fdc2c8d69c7254d472ac7ae7fb1eebf92e01a1d2e0f8`  
		Last Modified: Tue, 13 Jan 2026 13:37:00 GMT  
		Size: 15.0 KB (15001 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:aea3b67f5e2348a324c88b29157f5fc7927f854a3fe9f1d458cfc2b6ebab794f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289390536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34718b9cd2f95f1b811b76ef48df04ce72393439ad632f11076323f1a4fa0edc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:55:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:55:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:55:50 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 06:55:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:12:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 07:12:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 07:12:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:12:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:12:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a377be731c175125b38de6ef2031ba27b78ddc0d786d1f6e325bc386ce396481`  
		Last Modified: Thu, 01 Jan 2026 07:02:46 GMT  
		Size: 157.2 MB (157194284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c72f0d129abe5cd093f36d09c465005ec8ab9c45516d3f2cfe2fe30794ad7bc`  
		Last Modified: Thu, 01 Jan 2026 07:17:03 GMT  
		Size: 84.4 MB (84424059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11afc06695c414f2015f48b88833a95231642cb4b05a2e1cafe68b9e82d4471`  
		Last Modified: Thu, 01 Jan 2026 07:16:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a7b4e2ae23b32f22861ad73d08cf017a9f12e0cfb58af0f2a6b61d6be5b5d`  
		Last Modified: Thu, 01 Jan 2026 07:16:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fae0bc798bbdc67135c02f8a6f805c14656bb59b89f0ba602ba965399f484411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29ccacae198bc38af88e805746f8be4f9b5397b8b03f5265bdfd8d61ffac28f`

```dockerfile
```

-	Layers:
	-	`sha256:4645eee8a9e990694eb04d3da4665d24fc5b7adeca6b13214f64dac9e1fec083`  
		Last Modified: Thu, 01 Jan 2026 10:37:15 GMT  
		Size: 7.5 MB (7457946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a0431816a4a43d19df7d746cc8f3e1b331f87ccd795f59f575e98cf9c0983b`  
		Last Modified: Thu, 01 Jan 2026 10:37:16 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:87fc4c109660f95c30833011e7011998f1756679a535ac86ede7ba526333448b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282928200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a846f07ce9e3149f2b98f4ccac4ee5df387f7bbb58b85a0a080e188c124f1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:06:55 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:06:55 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:07:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:07:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:07:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:07:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:07:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c1cbdf0d72a9dc68d0af80283ce47cf61751f5eb2e9a6c1457edf37d0fd199`  
		Last Modified: Tue, 13 Jan 2026 03:08:15 GMT  
		Size: 147.1 MB (147069835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccce5668196fad87b76b4ba9dea11bf8ce1baedba96e668dc8112b70cd9bad8d`  
		Last Modified: Tue, 13 Jan 2026 03:07:55 GMT  
		Size: 86.5 MB (86508626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f750d4bc3cdf70214497df36d119d1a0ceb8f4bdf267f4812f5aed27da2b09`  
		Last Modified: Tue, 13 Jan 2026 03:07:50 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3836fd80b1f1709f0a00c902b5a5d17196cc50b29a4056bbaef91a4950ae7f`  
		Last Modified: Tue, 13 Jan 2026 03:07:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a15d22d73c0956f14b92981d6d0025d9369ca5e83db0373b620faa7384615457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08861cb24c146f6be51a729168b1874bdd772caec08dbd90fc2309bbff763a4c`

```dockerfile
```

-	Layers:
	-	`sha256:f65dbc337ebf01105f50e35b8f9895bfda71d575ad3efda57547148afa42f550`  
		Last Modified: Tue, 13 Jan 2026 04:39:59 GMT  
		Size: 7.5 MB (7466850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae1e19c008f1c735a3c1477273b784b4cc3a09387ea7ca54c9258ebfc090a6a9`  
		Last Modified: Tue, 13 Jan 2026 04:40:00 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
