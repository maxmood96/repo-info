## `clojure:tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:d8208cf8aa472ac4ce3e3aac93358cc601a28cb80dfdd0c7125843a59ef57579
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

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7ce886a04178ea47f0d4cb9a048d8d64da48e0cad1329e7671002910d0b464b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262065497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20442036623809bcffe164674343c97298376828d3715dc5571aa99dbc469239`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d191f8d391a10c91afc36ee510f13456ce1de6311e2ef8482fd2fb6a91be078`  
		Last Modified: Tue, 03 Jun 2025 05:16:49 GMT  
		Size: 157.6 MB (157634492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1db118c6490021b92a6b224c8fb7acfeab036e5cec64d74adca93cd846df05`  
		Last Modified: Tue, 03 Jun 2025 05:16:48 GMT  
		Size: 74.7 MB (74674583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bd0af2c30718e2c83f4f2c1d36f8d75441a9a7d88edca859a29476aa8765cc`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafb6ba4760087089f3c8959a5689f721b93e261d6680dac5299c6ae80b75c4`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4d2a98db660f7d3fa7432763e52a2b56ee97f9b5d9f521012a0ac02c43a76e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2432219e7194963334f35fb820ca5381db75f02eddc9bf530df6d38d8113a908`

```dockerfile
```

-	Layers:
	-	`sha256:089841dc9f183df2985d61efaa4fd878baf262c5e537c53e289f5f5ad67a2e01`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 5.1 MB (5115855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e33d8a8c52a5344fba809be019e62340439097c249490cc0d13d0d0fc2ea1db`  
		Last Modified: Tue, 03 Jun 2025 05:16:47 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7daa908b1258edb5ce9509f71d5874e96f209b7b9f1a095b1a689b5019b5182e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257696059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ca57140ab223dce2ecb7b9795dede44d1a5812acd685c64418ed4296e0ac0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Wed, 21 May 2025 22:31:23 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7a5d4d95ee7c4b7368fecd7381ad1f1df01a0f09f44935428120c34eaec211`  
		Last Modified: Thu, 22 May 2025 08:33:26 GMT  
		Size: 155.9 MB (155928844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7a94267835518d0c0bded50b4eecfaccc8dce71e44455ab605ca1cdc63c468`  
		Last Modified: Thu, 22 May 2025 08:37:51 GMT  
		Size: 71.6 MB (71646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbac1f11d609e8cd7079cc3af4248fe7f03c29501dcd6722745ec610b56291c`  
		Last Modified: Thu, 22 May 2025 08:37:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748fabb94d6424c9df256e55da879c09c757a5b77ceeaa26c73bac30dcb0c4a5`  
		Last Modified: Thu, 22 May 2025 08:37:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc5deecba130c8e6e431c36083dd0c9f99355f8f713c55339aa4234e540aebe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2567d1237f254322ecc9b80daac941a37eef5f6485d97f06c816562e2b7a898`

```dockerfile
```

-	Layers:
	-	`sha256:5940a3e5ec106427bd261f02bfb313276b6523215d6c26a61650fa8eb440dc88`  
		Last Modified: Thu, 22 May 2025 08:37:49 GMT  
		Size: 5.1 MB (5121648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccefd59c5012d72df237f4c00ce30c36114e9f98a353b31f2c51ddb61da9226a`  
		Last Modified: Thu, 22 May 2025 08:37:49 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:55b71df246b958f8631752028a776ddd5d8deb2c83166f2836e0fc788d07615f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268602510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765c24e2e4ac547784ed9d28176954fc104ecb4ad9e7913547784f4a99197b59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Wed, 21 May 2025 22:32:27 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2ce2f26a5a51be9f341e0593649527056f67d551a767199f037fb1a0b6504d`  
		Last Modified: Thu, 22 May 2025 11:32:56 GMT  
		Size: 157.8 MB (157804906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e263dc17de727b5a1d71d9f1b021bb76023dd7beb8164851681b841ee798f4`  
		Last Modified: Thu, 22 May 2025 11:40:01 GMT  
		Size: 77.2 MB (77215997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ad04c255e4d8be726a484b0d6e57a6f87c69c92599646b0cb73d95fc07ec6e`  
		Last Modified: Thu, 22 May 2025 11:39:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39f5b927c8778201e8557f6577eaf5edc2b31046c39f3b685b8715c917bab32`  
		Last Modified: Thu, 22 May 2025 11:39:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a01b0873347370d0f85e4230ce660a8255382d47b838328a77a8997f9a106d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c7a2bc65a75fcf5ce8be68c6e700d7706d27e3892f609191ded9f352e27f47`

```dockerfile
```

-	Layers:
	-	`sha256:e19786132f64e6ac878776924d4f3282f9d9d3882a880eda481fd8dcdd0c6eb4`  
		Last Modified: Thu, 22 May 2025 11:39:59 GMT  
		Size: 5.1 MB (5120238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d09491034aa672088e25bca4cb4767f13551a26284d582a9c335c166feb245fc`  
		Last Modified: Thu, 22 May 2025 11:39:58 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:d3fdd6f0910afeb3738dfdf70b1730a1dd32d3d645d09c400107eed00db7e1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252387964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e8e7fe5f5d4fbf345860a88474828148c47b398ee573b1625d55e56d6d3721`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Wed, 21 May 2025 22:38:21 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2f883243c7cda03adcd9f44b58b22feb78b4904813045b15aec217a35b4569`  
		Last Modified: Thu, 22 May 2025 00:12:37 GMT  
		Size: 153.4 MB (153449674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211b59c743c18d7c70a1841112e481c8d25254f4860a3824b7ffdff0451f06d7`  
		Last Modified: Thu, 22 May 2025 00:33:20 GMT  
		Size: 70.7 MB (70691895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e6a238d72f702b7814b9af39a305f680868e61f583569514fb90d1fc2b0969`  
		Last Modified: Thu, 22 May 2025 00:33:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b681e94ebd030478d45411cd00f28bef75dabd0358131dbd2a365d64083c4109`  
		Last Modified: Thu, 22 May 2025 00:33:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7264862233caad25fd46848868eb7324a50db71888cdd4861243bd732c336b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0322a570c1e9069c32f4b2bcb7ce1614d83a9ddfdf61386e13d4a8f2180b60`

```dockerfile
```

-	Layers:
	-	`sha256:4d9d285c583417b1386ace9c7277373a9d126339c82fb40a22a39e06873cef4c`  
		Last Modified: Thu, 22 May 2025 00:33:11 GMT  
		Size: 5.1 MB (5105331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b9bed869b33f17560bc373b95d1dbf91a1821cc2754d5c66231a5eb3d5960d`  
		Last Modified: Thu, 22 May 2025 00:33:10 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:02a0f58678ae68ce8ab7aa2267f183550f3eedca77d635bde2cf26ae2d1f9eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252148027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6093bb1b85297edb15bc81483ff98271b724d0f314adefb1ea6680ef3784dc53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce31050e492004a774304e4a6a039f15374ef94ca4f31b4d1ea37f80078b58a`  
		Last Modified: Tue, 03 Jun 2025 06:29:06 GMT  
		Size: 146.9 MB (146910974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79acaa246d843a853b8f572c0627992f21ddefaac20cdb6baa089edb674a236`  
		Last Modified: Tue, 03 Jun 2025 06:34:32 GMT  
		Size: 75.4 MB (75406394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ac87e596eb31c60a3c75d65d001ad67d04e0efc578d0a69bfcc0e1d8536e0d`  
		Last Modified: Tue, 03 Jun 2025 06:34:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3041bf75c5b57773b63b1200cfb601b6a1058f2b349ecda475089df4f3ca2517`  
		Last Modified: Tue, 03 Jun 2025 06:34:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88b1ae0b30d455dd4d32ab5f4a427f348d77e554e472ccc79f65939a86909957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf417b9ad40d26c535f6bcc22fe4f1dd6df99a18b10c80dddd9d1420f5f5b49`

```dockerfile
```

-	Layers:
	-	`sha256:8dc6ced9764c4867926d570814a4df9dd8fef0dc50238c4f14fcfcad64a6bd71`  
		Last Modified: Tue, 03 Jun 2025 06:34:30 GMT  
		Size: 5.1 MB (5111779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566f6b5236ae0cf109334a5e648671d7d99e62366ba400df6929503032a65884`  
		Last Modified: Tue, 03 Jun 2025 06:34:30 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
