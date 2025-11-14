## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:14bad44044b984ebeb31b70a0e4ef010ad5aff16a7e96d6ced69f4afb9ba2e41
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8bb1dfc2ac1c5547cd5285ae724d3e4e265c35734042173852b584bc9c6ea6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279675261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81731767c9210292fa52290a9a371b11fb94d5813d217eaa176e6dc08f11eda8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:43:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:28 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:44 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c083b5c9dfaaa493e849cd1ab542ae80108d0976c95fc709a0f2aa4b737d93`  
		Last Modified: Sun, 09 Nov 2025 00:11:02 GMT  
		Size: 144.8 MB (144848052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30df309a25b9a3a34e3524f5ab816691f686653aa9501bfaefe49a59f17db574`  
		Last Modified: Sat, 08 Nov 2025 20:31:55 GMT  
		Size: 85.5 MB (85540539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12f282de38dd4c93239047371a708c094fb5bfca6aaa14adccba408cc2caebd`  
		Last Modified: Sat, 08 Nov 2025 20:31:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f51d680c2df3e35531416d195ede1ec2ae35b9bd38d61a59eb7a424f840745c`  
		Last Modified: Sat, 08 Nov 2025 20:31:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7016ae9edef7eaf5f5fa1935eae5a4039ddb57f0fcae8a099778a276261baa22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa58f94a8bd368c575a788f1f41c521320c61a88485f310c47026ca3c9114e7`

```dockerfile
```

-	Layers:
	-	`sha256:ee688676e8cd95315eebdbe9e852b473d5a643768c88288015771d87ad00517e`  
		Last Modified: Sat, 08 Nov 2025 22:44:56 GMT  
		Size: 7.5 MB (7466901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2c838c6468d13f0a3f9ca84d77d2ca1e4f509e8e6f76966b83ae99260536315`  
		Last Modified: Sat, 08 Nov 2025 22:44:57 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

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
		Last Modified: Fri, 14 Nov 2025 00:56:03 GMT  
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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:deb9673acf55401937fa072ef9912a9190d22cb1b3d1869e5e172d8c7f930ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288586365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de169efeebc223e8608b56f06f694c9c28222518559c37544b47585551001ab8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:18:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:18:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:18:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:18:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:18:18 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:27:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:27:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:27:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:27:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:27:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e8782314f27b926983211cc829d4001e3f86049dca101a7fc7515489a4bfe7`  
		Last Modified: Sat, 08 Nov 2025 21:19:39 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bef78469dc688b9510000750b8c47c33427f62e961fd6b677012d584db0b6a`  
		Last Modified: Sat, 08 Nov 2025 21:28:40 GMT  
		Size: 91.0 MB (90950058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b708e9a665441d6cae19ae5cb96a6badc8048e10439f544aad4a514cb4484639`  
		Last Modified: Sat, 08 Nov 2025 21:28:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d641eb9831b7a89a5a4194453664fb32a93aa9b61754c062b14e1d9b3d7000d`  
		Last Modified: Sat, 08 Nov 2025 21:28:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:44555c9ab72ec88dbd9dee66a33025e16a2fa42317c8a2c250d042c5c8f9d7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4faef1181312ac3237d52e30b209ee2eb9182e6b625e7c13acee810e77dde4`

```dockerfile
```

-	Layers:
	-	`sha256:5f80fc5c8666593c16c4bca60856872636ccbe48fccd4225778862c369551f47`  
		Last Modified: Sat, 08 Nov 2025 22:45:09 GMT  
		Size: 7.5 MB (7471320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fbea389593c0a87633eb5269cf615f66165c3ace81146ebd7a58572a68f86d0`  
		Last Modified: Sat, 08 Nov 2025 22:45:10 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e88ae3d56eb3a8571fec285767a96c0b4cf0b0831d57b85287564abd101e2b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274088388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e73d11bde98edbb1263eea4f5ef03634b79a997a53b5bf268e3c57d94d6351d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:15:22 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 03:15:22 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 03:36:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 03:36:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 03:36:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 03:36:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 03:36:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ab2569f219df552fc00a9a5e017ffe204ab8c96ed1cf8ccebefe31e0bca0b8`  
		Last Modified: Mon, 10 Nov 2025 23:10:58 GMT  
		Size: 141.9 MB (141889570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8f2f4892c340b59e3d044bb44c7229d688a0a7adc06218384c3771e1a9eb3b`  
		Last Modified: Mon, 10 Nov 2025 03:41:29 GMT  
		Size: 84.4 MB (84426851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a660ef78c65f5998ff476acd1bcfb079330df7111ba94afc09c2428354d6c9e3`  
		Last Modified: Mon, 10 Nov 2025 03:41:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19937873cdee377a9220e95064d47e8e56f5d201f08b7453aef525adcbc2fa`  
		Last Modified: Mon, 10 Nov 2025 03:41:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6c87aae3555659d502e756ff316fc9ccbcfad30b6b9bae784fb2c0e73a7b0427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec242c14e792b9688e766c9db4134c7a4c7016a41e37909a41786f1323cb8c4`

```dockerfile
```

-	Layers:
	-	`sha256:73c56c52b5939c63635dcf149ab46b6e58c7505ead277d380a69414037acf389`  
		Last Modified: Mon, 10 Nov 2025 04:36:16 GMT  
		Size: 7.5 MB (7452895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6761d2ae223479d5be4b28b28e00bdb02c2e07f6d8ca841aa459f28cd785fe6d`  
		Last Modified: Mon, 10 Nov 2025 04:36:17 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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
