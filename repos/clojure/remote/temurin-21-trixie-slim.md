## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:eb657846b6d9c2bcff03b8e1f8f51694bbca00ec4876340fcb1c408b4a7f53ca
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

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
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d191f8d391a10c91afc36ee510f13456ce1de6311e2ef8482fd2fb6a91be078`  
		Last Modified: Tue, 03 Jun 2025 05:16:49 GMT  
		Size: 157.6 MB (157634492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:461940bc9292c6b69f1b1668b85735df7eeb78a714210ec61436632d386964f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261007886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2507b56aad7e352e1802ff1aa510f68670aa4e6b4e7c92b365f4f884b4b6d`
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
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4a1faf17299c1f04638ddc5d736ac61ac6707116abce4ce0b018d30b88ee49`  
		Last Modified: Tue, 03 Jun 2025 10:58:08 GMT  
		Size: 155.9 MB (155928817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bac19571b9e850460613ecbbd52e33c6346aa778edf6aff58afb2e1819dfad`  
		Last Modified: Tue, 03 Jun 2025 11:03:52 GMT  
		Size: 75.0 MB (74958576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf45360683ebb878926d1c024a14aed6735fa7fbda93c942cf59277638328161`  
		Last Modified: Tue, 03 Jun 2025 11:03:50 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bf29144707aa25634ed45409e3b685616ca1719bb6142badd65ffec6bae0f6`  
		Last Modified: Tue, 03 Jun 2025 11:03:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e7860e4149dd014e1ed7090e927a55f9466e6691ebc6c5f14259b94b05140ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b92f834975a894f7fee0b4b8af32bee19971cdaf6cd4dd2b11aa71e7f1d41e`

```dockerfile
```

-	Layers:
	-	`sha256:b4dc3e8b95511d27caf1d9afb495189a24a70e6316dca69526059662c6d9a2b8`  
		Last Modified: Tue, 03 Jun 2025 11:03:50 GMT  
		Size: 5.1 MB (5121648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d62eea8b6a3f18ba038b42d494ab75cbae60f9d4ba16a61b441a535d539e1c`  
		Last Modified: Tue, 03 Jun 2025 11:03:50 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a543ea7df564f9e620df8ee2c4ee963d63d928c01a87556eec3b322df49727c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271800751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa04a0d1657880e18193ac5e5d05334384a3c18839aa94aba3e5adc54b80ab1`
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
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ab9d4ac6bb74fed4f1c45b064cd14cdabf6a0b701738b0c7f33fe7866ad1a`  
		Last Modified: Tue, 03 Jun 2025 09:13:13 GMT  
		Size: 157.8 MB (157804907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb31a64aa6c77040d004fb14bcb8d354a7b742beda7b9b9fe997f1418f2d11a`  
		Last Modified: Tue, 03 Jun 2025 09:23:22 GMT  
		Size: 80.4 MB (80414238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7094399e485424202cbdb36b480dcfe71e878389c4955339a164e96f51d472`  
		Last Modified: Tue, 03 Jun 2025 09:23:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327bcde6305134d91391434143f657d202ebb387b28cd21021ea521eedce4bae`  
		Last Modified: Tue, 03 Jun 2025 09:23:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf2b15a244e4f6711fc48210f86b7be3dfda4543b995977033a9514c22fb1010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21bdb8ad60ad88dcd978ef7f028239ff07ed00e4b7f6f71ff40fb5d2a34c1e4`

```dockerfile
```

-	Layers:
	-	`sha256:23651d7e03d54a9f86e2dbd20bd940c2dff61682a42644853ae0c1fa21f7c33b`  
		Last Modified: Tue, 03 Jun 2025 09:23:19 GMT  
		Size: 5.1 MB (5120238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe9712d9b5992068cc8752aff9982b4d0b1396dbae8a85e340b521add3ff5ee`  
		Last Modified: Tue, 03 Jun 2025 09:23:19 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c704a5800a43b1e3b95cd61f30531097a11d7f845498408d486294901577dcc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254986730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa70fa35c760d2bbe1883b806b29271adb9874cba71350a0c63ec32d36ce879`
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
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5009b64f50fb13ff55ef1af62e2fe1e6a6ee386115f6dc3a0f39a750f60310`  
		Last Modified: Tue, 03 Jun 2025 09:46:36 GMT  
		Size: 153.4 MB (153449629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064fc5691a513e680aac6a403957d81b8e69074028548ca89cd84efc6a3bede7`  
		Last Modified: Tue, 03 Jun 2025 10:09:42 GMT  
		Size: 73.3 MB (73290706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416481516488fbad2ba5330cd46058a5c59fadb94d1c7cc426fd7b236d6fccb9`  
		Last Modified: Tue, 03 Jun 2025 10:09:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d697d041d71ec8ef462c779d92e30bb6d05a76a840ba08c5fdb5cf812f246b55`  
		Last Modified: Tue, 03 Jun 2025 10:09:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b002d02865acab61c8ef274aca59f67d4f815b931986db10348b1d7fbabaa8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adaa2debab47b28d8727714651a7f56b934e4d7c737b04c9b0d0331ef4113de6`

```dockerfile
```

-	Layers:
	-	`sha256:e9da8aaef8fde138c880c9e9fb2ecc0dcc0d15573b4b8d81ba6050d344fc5f09`  
		Last Modified: Tue, 03 Jun 2025 10:09:33 GMT  
		Size: 5.1 MB (5105331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d6d1117a58d5177d6bcbf4a6e336170f84574adbf6559a7b0da0131bb281be6`  
		Last Modified: Tue, 03 Jun 2025 10:09:32 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

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
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce31050e492004a774304e4a6a039f15374ef94ca4f31b4d1ea37f80078b58a`  
		Last Modified: Tue, 03 Jun 2025 06:29:06 GMT  
		Size: 146.9 MB (146910974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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
