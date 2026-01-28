## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:2e2c5296d0f60ca4f26d089a9b572c757e46617791a55de2c953a9778c43214e
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:988312680e6e6afd7abc873a7f9274f22f8b896df78f68845125ff13c884603c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262545492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfb94369be53f2edf1276a059bbd1398033b27a93c1b1d22f9d2536246f0f3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:01 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5589e8feadbcd9f21af866f74bb236ac6f4ccd60797f119ff967cf0d5e999df8`  
		Last Modified: Wed, 28 Jan 2026 18:06:42 GMT  
		Size: 157.8 MB (157826064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862596b5acebe0e7d248a6846bebd7a51214e623e699b2579aec31fcfe76dba7`  
		Last Modified: Wed, 28 Jan 2026 18:06:40 GMT  
		Size: 74.9 MB (74944705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ba8da280927ea98668beee086421e38e8708e60f7b4ca6097232725ae64c9a`  
		Last Modified: Wed, 28 Jan 2026 18:06:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fba502a7f15daf6cb57291714635bdad6c43a1637544bc752ff1ff5036c970`  
		Last Modified: Wed, 28 Jan 2026 18:06:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27bb100ab0fa633445ba7b577d205396a82640e7c0682f3cdbaf6f3d68ba03d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938e636abf005a83e53bc4902d386ab782411c19454a9fe8c7c527d890805c24`

```dockerfile
```

-	Layers:
	-	`sha256:71ace6e84ba5d42bbec78d7408972a631a87034222b43e3b6eebf30e86edc359`  
		Last Modified: Wed, 28 Jan 2026 18:06:36 GMT  
		Size: 5.3 MB (5259401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52a0b67dcb68516ce1de780ab019d74c670ed7e6ebf6da9e0318f3b6538d0a0`  
		Last Modified: Wed, 28 Jan 2026 18:06:35 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:88039ec8b86a8dd300433cc76ab82da6073c9145cc837d2df57bbb354afaa23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261364596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4790770e3744930174fce354a3df8548ff0c8acab03883e7cca9948b4a6d93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:05:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:05:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:05:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:05:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:05:52 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80cc3360b9e13d9309f0f4eefec2d0079b5f0e674cd4ddef08a16d003377a1`  
		Last Modified: Wed, 28 Jan 2026 18:06:33 GMT  
		Size: 156.1 MB (156107578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a081b0178e7549c243ee41821ff6230834f19f7219c091953d1a9b59358967`  
		Last Modified: Wed, 28 Jan 2026 18:06:32 GMT  
		Size: 75.1 MB (75121931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d248d1e0c63956307ce96b7b9b0a5a4aec64bd55cf6cba1bdc89b9453af679ed`  
		Last Modified: Wed, 28 Jan 2026 18:06:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21de90c0b7eda3ecfd1ea7e5c6d4c89844553e3a48b427a2bea7dc626841bf8b`  
		Last Modified: Wed, 28 Jan 2026 18:06:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f66f742a7c2077d7e23a04971696552a1ec39d84debd5e0b3316dc235dfee57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aa1c1314ab383b2888d4536983dcf4655a253c05010b7396e2992c72eca084`

```dockerfile
```

-	Layers:
	-	`sha256:7537f7580af4c90b3b2a27b7687593e88eb9faabf2cc0c11f18d209a7e8f1745`  
		Last Modified: Wed, 28 Jan 2026 18:06:29 GMT  
		Size: 5.3 MB (5265170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa79c4fd2cff22d91ffc986f14b59f586049f8a0ee3a2d2799acc03be4010df0`  
		Last Modified: Wed, 28 Jan 2026 18:06:29 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bb903e4b948330162e1642958d2673bc984d2cb7b9e75a3677f4d423ab1c28d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272129860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0831c19edda23ef7fe16407a20d03911d3e23f38cf74616a400f62cb2a2a491c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:31:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:31:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:31:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:31:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:31:19 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:32:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:32:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:32:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:32:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:32:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb8f4600d979d25ba9491f1c0b276d63f57f611e75453e2f2d5361bcc2ead2c`  
		Last Modified: Wed, 28 Jan 2026 18:32:52 GMT  
		Size: 157.9 MB (157942895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155710f318c7463bc829ce3a6500318ed369d6ae183edbbde317a77fcb92685`  
		Last Modified: Wed, 28 Jan 2026 18:32:50 GMT  
		Size: 80.6 MB (80590322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb0bff8ef1f4de78cb60eca34ac9bd54fba248a5825c61149797bd96c5d00c7`  
		Last Modified: Wed, 28 Jan 2026 18:32:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533b81899dd88f9085870cab4864f28f841484b47e29a8ac14fabe13486c1eea`  
		Last Modified: Wed, 28 Jan 2026 18:32:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f47d3b34e4cb5a67a47ceb93ab95b0011326671236975e98f07bfcf1f16d1d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91dcbb4b605a6706ea888cb76142c05f54e618935b98e2bf2f21032a7f79ed2`

```dockerfile
```

-	Layers:
	-	`sha256:2bc0accc996e753049857bcec3b058811ece74712d3e140f799795dd8d3453cf`  
		Last Modified: Wed, 28 Jan 2026 18:32:45 GMT  
		Size: 5.3 MB (5263772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c9ed171cd5d4f928c2cdf48f8bf8c8871da89a91dd5ced9f209bb93ca51524`  
		Last Modified: Wed, 28 Jan 2026 18:32:44 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:d8d5d3e5e25138d04ea82d75022894c7946040d230cffb8dfe72bf96fe2f30e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256345830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803799bc0b3c19d19ee267c29eb4276fec30531754ed0c7824e6da6488a4df52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 03:58:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 03:58:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 03:58:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 03:58:05 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 22 Jan 2026 03:58:06 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:21:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 22 Jan 2026 04:21:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 22 Jan 2026 04:21:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:21:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:21:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ce3d8fe97e3f0f300cf6a379bdf8a6818893898d0842fdaef865eeba68c7ff`  
		Last Modified: Thu, 22 Jan 2026 04:04:03 GMT  
		Size: 157.2 MB (157194340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd76cb8af4dd3e38c7eae3325e8a0d72fd9a14b14d9196f7ed152291a2e92b7`  
		Last Modified: Thu, 22 Jan 2026 04:25:15 GMT  
		Size: 70.9 MB (70878764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6701652d5cad47430c5847ee2d32e960cbce9eeba80ae41575f27844dd3808`  
		Last Modified: Thu, 22 Jan 2026 04:25:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163d6293dcc1354641ef524165f4e596d16ea1efdac7a0239b30b8cdda7a6e90`  
		Last Modified: Thu, 22 Jan 2026 04:25:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44c725f99be72cc4a41677f685ed4bcad57bd6cf0e313ae48b9e61bbaa817640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb570a6660733c963afab1a9d5c884d5e894f5950c5ea57c48dc2dffc00ef8c`

```dockerfile
```

-	Layers:
	-	`sha256:9afaa7a08b4ec2ac3c028c1322907b57ebfdbce41d5c3edf445fbcbb1faeaabe`  
		Last Modified: Thu, 22 Jan 2026 04:25:05 GMT  
		Size: 5.2 MB (5248863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845059bf7a9f09dbecae5d277ad04857343d2075b936d47dbf30527de3ab71de`  
		Last Modified: Thu, 22 Jan 2026 04:25:04 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f498e2b0d63ab32ace9d1dbdb8440e507d9ae8702403613188640491ef6074ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252471651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa145c5ed0f8e58eb2627038b0d19539f792268f8699dc276997a7b4f8602db4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:19:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:19:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:19:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:19:34 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:19:34 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:14:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:14:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:14:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:14:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:14:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e307e5df525a8baf85f7de5a221c6604e3d80753489f585e9dde342af99154`  
		Last Modified: Thu, 15 Jan 2026 23:20:14 GMT  
		Size: 147.1 MB (147069858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01459ad739357b2f212b09082625e5d80d2c2390f0ffd7d2d5c21a3c9446f32d`  
		Last Modified: Wed, 28 Jan 2026 18:14:48 GMT  
		Size: 75.6 MB (75567342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bdb3b418cae57435ae581018ba1c8865e7784444b0580fae3c37e82465de42`  
		Last Modified: Wed, 28 Jan 2026 18:14:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921451cf75acf92970e2ad09708c0e786545f1c0503a4bd66f5ac7285ebc8c31`  
		Last Modified: Wed, 28 Jan 2026 18:14:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94c819425a9e3a6e9bbfb22c56134684cc3640adc46d4faae038b4ae3205c2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033919772809b4458a5cd7cd2f3c3cc3e7538db9233dfd91390163c0ae770c83`

```dockerfile
```

-	Layers:
	-	`sha256:2a32a925d6fea19408ebcea4b7346b22d1dbb82de4e82379196b7626954a1f71`  
		Last Modified: Wed, 28 Jan 2026 18:14:47 GMT  
		Size: 5.3 MB (5255325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a82cb0dcc4c37afe2456bec32a0a9f7b86a09905d0eb826e69dc4075c96a2f`  
		Last Modified: Wed, 28 Jan 2026 18:14:47 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json
