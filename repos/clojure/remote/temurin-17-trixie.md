## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:515ee7631b76cbcbf0706a4a26f2b6bafb4a5496dc3fe9cd6ba3743df9a5052d
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:058ae3ef48398ce99a347493d0f34b4d0d48b76b4a0e8e7f8161acba00bcbf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279674989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d73c259cc7636c1a28232fc7a613944c64803e53d5440b77cc8273d44df9c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:20 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f416fdf73ff86acee259d85982a75c5fb3bedb6f96362d0a26779d7e7d4669`  
		Last Modified: Fri, 14 Nov 2025 06:10:50 GMT  
		Size: 144.8 MB (144847948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1380c131e24b0d8bf7782169a1e61e8e12dad9eb0b5ee72b0cdc6476be3cf1be`  
		Last Modified: Fri, 14 Nov 2025 06:10:47 GMT  
		Size: 85.5 MB (85540368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845840340424bf799a98147e6be429752e95cbb085c9e5d2a5b3bd564bca7b91`  
		Last Modified: Fri, 14 Nov 2025 00:54:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b638b1b3b1720ae13a9bbeb3c96f23ce934da8b122bc2a73adc6a67d9d70464`  
		Last Modified: Fri, 14 Nov 2025 00:54:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:84b4ac7229c6005632ce68c3b48cade4eb6a538e820ba33153d7628c798a7eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f03e8d0ff32aceb417f3a4e86549f7cf04532ac6c1b01af40f821a5b95927c5`

```dockerfile
```

-	Layers:
	-	`sha256:a9ef6cdd9379a1a48aa4bbfcf46a377b9a215b781ed6e15f6f67a145db1700c9`  
		Last Modified: Fri, 14 Nov 2025 04:38:08 GMT  
		Size: 7.5 MB (7466901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155392313f841ac5a2cb7fca1eddadfea3fd358868499015f37b9e33c5c15b46`  
		Last Modified: Fri, 14 Nov 2025 04:38:09 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f48710de0880effa213a566a37fbad3513e314c885a1dc703d7863a8be5acca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278694856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c5d87db9bea4409b5f1e2841bbd051b7fbcfdfacda8742e7e89a059ea10aff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:20 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816ea3f8578a548bd2f3fae1a87c6a6036e4c13c40cec6314a79a234652d21e0`  
		Last Modified: Sat, 15 Nov 2025 04:34:36 GMT  
		Size: 143.7 MB (143679885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a54a230d52f407ab21d61ad82f2a599761e8bccd49ee55a6350a283c9350637`  
		Last Modified: Fri, 14 Nov 2025 00:56:20 GMT  
		Size: 85.4 MB (85363494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ba726f31a1883b5b85f4688c8aaa10760794ae2fa7c51fd972d8e61f443426`  
		Last Modified: Fri, 14 Nov 2025 00:56:09 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae126dabb57d8ce4a5dca1c00fe8133b72ae918b96aa0d331208b48cfb48b308`  
		Last Modified: Fri, 14 Nov 2025 00:56:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb455fc18f268882b4580baa74544817fb9d03ea2a0674ec41ee4349ee2f0fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d476ab12c1d9e96992cee91df697c3a382f4d31cea0c51544c844cac11079b78`

```dockerfile
```

-	Layers:
	-	`sha256:b7eca7bd214d9ab3d5353e3cf0619248214eb88a38f7d213d95c7f471f1b5650`  
		Last Modified: Fri, 14 Nov 2025 01:44:37 GMT  
		Size: 7.5 MB (7473931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297cc0e6c1eae6a92806ca996000bee47930e3a7e81bc8e25f3921a708f412e2`  
		Last Modified: Fri, 14 Nov 2025 01:44:38 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:dedf8ea561df91285e6c98b91116db21826c4d11e2226f6158efe31d8765647f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288585695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c579a1ee16ce4f2481e2e39e275fde850348c103139864711177bb497c3acf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:04:12 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:04:13 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:14:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:14:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:14:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:14:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:14:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006adae81b39e8c2eb6c4f5beac67c9c4f256bd536a083ed9b0394d34fb5b0c8`  
		Last Modified: Fri, 14 Nov 2025 07:05:33 GMT  
		Size: 144.5 MB (144525223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abe0641f6d79c243f92815470298622f33eb831ba6ff1ff6cd1323d4879ac5c`  
		Last Modified: Fri, 14 Nov 2025 07:15:18 GMT  
		Size: 90.9 MB (90949300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4236e23ebf480a92891536ae1953f46c454aef482fd4726fafa4775e19712af1`  
		Last Modified: Fri, 14 Nov 2025 07:15:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b8030b5d5b2f3061b9a47e79a01902f92116022576a1963b720d1f05ec527e`  
		Last Modified: Fri, 14 Nov 2025 07:15:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:701fe50209cd0d150a89f06ecc2f7c3e0af405841f3053dae4076f92da01f93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb691eeaba47cef088851959446359feabbeccc6b797934ffa044d1ad5e92703`

```dockerfile
```

-	Layers:
	-	`sha256:6a12f71c174ab3bee381d1af179c594f9a9da319880f2e6ec50e258cced3442d`  
		Last Modified: Fri, 14 Nov 2025 10:36:44 GMT  
		Size: 7.5 MB (7471320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54475dbc87de95af42d33f37c8e833a9a10cdb70b7c0d25c835491a781b65887`  
		Last Modified: Fri, 14 Nov 2025 10:36:45 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d5c538baaf4b262b0160830cde324c9200f07fe23575e0647e3bfe53c9ac86dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277246824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329430befa1cda7d47e6fd9406921319615765c0fdbc11849b225197e73ac6e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 21:00:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 21:00:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 21:00:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 21:00:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 15 Nov 2025 21:00:17 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 21:22:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 15 Nov 2025 21:22:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 15 Nov 2025 21:22:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 21:22:38 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 21:22:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734a358c92adb84badd879c1e293b2d1f8f6cce639f35f64ee300e91fd4043b4`  
		Last Modified: Sat, 15 Nov 2025 21:11:27 GMT  
		Size: 141.9 MB (141889560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f053ab61654223094863c6268d38ed0744c33ef58f962fbe13ff1bde8ef8fd`  
		Last Modified: Sat, 15 Nov 2025 21:27:14 GMT  
		Size: 87.6 MB (87585296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfa071e6561150e5a552cdd002ef1c1e8a280ab475006d5f39d62bcf709f9c3`  
		Last Modified: Sat, 15 Nov 2025 21:27:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd3d80e34d7263bf4be23b4514e2b1de24b883bb536426410993a57aa87ef1`  
		Last Modified: Sat, 15 Nov 2025 21:27:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:890dca5bcb661fb1ac7c4e4ba22388b2f14482f333a1c8a54d1e29ac2be4837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9477747143cc37095dbe2ffc06736bbb76fec7529779339333b6f61389046b69`

```dockerfile
```

-	Layers:
	-	`sha256:38a1ed8605abc98fc5ee22b5360342fa45bb042dab2d6793d53bbb3c16691b4d`  
		Last Modified: Sat, 15 Nov 2025 22:36:17 GMT  
		Size: 7.5 MB (7452925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d84ac8e78870d925d3c34943f3eccefb2f6fb44ee2a770007b071fb66969f9f`  
		Last Modified: Sat, 15 Nov 2025 22:36:18 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e5a0cdbbe33e4452d3528e3a312ca8ef46584bddf8c4c27a57d721eb9fdeaa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270720635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c75b5c63298c96a97e3378ce6f3f2775de7f1e3a0342d027e31ede331cde2a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:26 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:58:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:58:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bff8e87cb45b3d7167fb65b8d0c1a1a90dcf5a9a1a0b85730e1a46f7b11588a`  
		Last Modified: Fri, 14 Nov 2025 00:57:05 GMT  
		Size: 134.9 MB (134859047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e16a83f3588b741e3dc9c8877e891652f8b9af22897ceebac74c8a9e5b7fbf`  
		Last Modified: Fri, 14 Nov 2025 00:59:16 GMT  
		Size: 86.5 MB (86508249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c3cbbb5f14918f9745e924d5a4ac866a03420bfb17b68a05e5151346b7b969`  
		Last Modified: Fri, 14 Nov 2025 00:59:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e168ef7feb7da18f6302fcbb0955a170e8b040b747ec54f68761c5c1648ff5`  
		Last Modified: Fri, 14 Nov 2025 00:59:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bf1e36416f953533bf47df9a1dcb6c128e08d4768a468ca1e90d3ebc3a8edf18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc73837d221a47eeb99d8043ef36e5b860585cf56d7f77ab41e657f023c2db1`

```dockerfile
```

-	Layers:
	-	`sha256:c77108fc3f6f60ebaa0b55fefd9133beb769c33c0e6747e2a37bbaff8e4141c8`  
		Last Modified: Fri, 14 Nov 2025 01:44:53 GMT  
		Size: 7.5 MB (7462823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4dfe353929003efe4ea1b431f3f5ae6a2d3ccb2ef275170178a4b6be4a1705`  
		Last Modified: Fri, 14 Nov 2025 01:44:54 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
