## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:6c1a40c8e9988d4f521c550c7e36309f010224dcea145bfb4d26730911ca24ea
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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:621b3112355451b8c48e0ec8f23922d73c60378efe7ff2c45826f33d797c6ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278695061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc81941d8bfe43f5ae308ddccd4cdbfea656fa2c204b079e296aba45b1c201f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:43:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:01 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50643fb3ebf9a1eb7c3640d2b098b466dc4591d4afff6cfdcaed4bec499c7aa8`  
		Last Modified: Mon, 10 Nov 2025 05:05:32 GMT  
		Size: 143.7 MB (143679948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fbc0b5640cfbc9fc294da63f5fc206183f1acc5ce87a74d559b720ea952a08`  
		Last Modified: Sat, 08 Nov 2025 18:44:11 GMT  
		Size: 85.4 MB (85363638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d720d81ac7c888be2f2f937fc2610599a33beb854d51172758842bd2798293`  
		Last Modified: Sat, 08 Nov 2025 18:44:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bc4f1ff56c2cb5fae3687f02796141a65696f86b6a7f9f07d21ad9e19b7e21`  
		Last Modified: Sat, 08 Nov 2025 18:44:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:619b9ec9f7d30f5dc32fdf2dedb4620eb8ac327ee84e8d1153a32c345798a84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbafe1e6988de13bf98280462e4a23652ca65f50f38454612659ec0e1e6a656`

```dockerfile
```

-	Layers:
	-	`sha256:5ac70912d4526b6eb650c363b5df9be3d1f835968a891fe21d0d5fd21ef9ed3e`  
		Last Modified: Sat, 08 Nov 2025 22:45:03 GMT  
		Size: 7.5 MB (7473931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5898dc203b2f2624acf345aea3f85f4b86410efb0c20f8460d1d0ae751ab65`  
		Last Modified: Sat, 08 Nov 2025 22:45:04 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; riscv64

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
		Last Modified: Mon, 10 Nov 2025 03:21:13 GMT  
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

### `clojure:temurin-17-trixie` - unknown; unknown

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

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:6a56ba2e7f1121057c0ecb722111c7682ce41f3d200d9a3825f5620cd9f80ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270721127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863c232fff0481aa80d469701fc68dc6bafcac0bc512ceed53c2b3bd541d88ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:39:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:39:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:39:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:39:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:39:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:45:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:45:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:45:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:45:35 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:45:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fb01b7f7bdd48ce68cf5bc1fa2e5f51b291cd23fe79f128847de11af6c4ff9`  
		Last Modified: Sat, 08 Nov 2025 19:40:07 GMT  
		Size: 134.9 MB (134859055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d45661671264b46f7365ad827ce3d1993efced428057db91fac5263b7efe9c3`  
		Last Modified: Sat, 08 Nov 2025 19:46:16 GMT  
		Size: 86.5 MB (86508731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0237ae59a716f2eca7fc1c38e6a728a7eb47e91e11c2a635cc850296a4667`  
		Last Modified: Sat, 08 Nov 2025 19:46:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5bfb0c2b2a0f6dbdb83ebfbcadcaae99dc5579f2a242af1de2aecda8d9ba22`  
		Last Modified: Sat, 08 Nov 2025 19:46:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:61c3314cf62691ca0efe9d2f63f7919136698ca07966e42707cd830ae9ed5068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fddcacfacbd14a55e8ae9df50d1058ff8fee1f6a8a18523343f11a97a16af3`

```dockerfile
```

-	Layers:
	-	`sha256:5dbce6843bf1c23111cc103b9609bec9c35a04efca4e59a8cdbb32ec7f53c5ae`  
		Last Modified: Sat, 08 Nov 2025 22:45:21 GMT  
		Size: 7.5 MB (7462823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4d3b1b0c0ebae6af797968e9ae6e46bef771f20956b0ad9ed103b2d21ec2a9`  
		Last Modified: Sat, 08 Nov 2025 22:45:21 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
