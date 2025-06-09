## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:a34707a4a0fa62960b8eb5e1b382fb34e5810b4a1b7afb6a6570f22e212a894f
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
$ docker pull clojure@sha256:1e854d69339376a1f5073a1c33182ba0c847c73206306ae2a4a6c61a75eb8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282089907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f96897a83f73f37d48dab8011158a8bc6689d55988cd22842cf9a477a46083`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e513432e22464bd7da0f7fcd93fdb45bb58bee3d06b2c36bf82260f9706122`  
		Last Modified: Mon, 09 Jun 2025 19:34:41 GMT  
		Size: 144.6 MB (144634949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4a8c26311bf388a240f70cd353266e6b2a863f302b41c9db99b51fe8f471c`  
		Last Modified: Mon, 09 Jun 2025 19:35:32 GMT  
		Size: 88.2 MB (88207009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c00823f4be82f5f959b95855c3f34b95cf01920f03405199dd3ede0882bfbd`  
		Last Modified: Mon, 09 Jun 2025 19:35:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b316b9c213c8f33a5959bc43dbc7e0159d9a7e2a18a91e05c32f87f30f75b556`  
		Last Modified: Mon, 09 Jun 2025 19:35:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:67cdc78880bf8a8c2a504bb1aab31b0eb6c04bb769ccdfe8e45709611ba81e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120206ec7204b4fcaa377493977c0a4f60bb95e4a8b8f4a3b589bd9bbd791047`

```dockerfile
```

-	Layers:
	-	`sha256:68e0a798ecb8455ee429a4f807b5593826b455d4508cdb8b67c94d762f65d34a`  
		Last Modified: Mon, 09 Jun 2025 18:38:19 GMT  
		Size: 7.5 MB (7458635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8a1ad929f49b58414a16db4a8f67e7ee61046abf9045b9d27dc1aa51ccd6dd`  
		Last Modified: Mon, 09 Jun 2025 18:38:20 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04bb6716f76b16bf6841bc9f18efcd9242a45c4342b8f69e04f6809304e3fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281643151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e71c64fd94b15a30ec1563d767712e1d8ea558be3713c879d4d7abd9bd611c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716c0c482281cd83847775856a8d2b5dd899b670a27f613e6c9f63273d5d058`  
		Last Modified: Fri, 06 Jun 2025 12:50:12 GMT  
		Size: 143.5 MB (143512625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b20f106202c77c1226f8e33ccae56ec009989ab360ad9e78cc99a5d4b2a32ee`  
		Last Modified: Mon, 09 Jun 2025 17:50:21 GMT  
		Size: 88.5 MB (88511193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90f199128bc83ec050fbc662c91877c7af5995082fff9033bb3d02413e7e5a`  
		Last Modified: Mon, 09 Jun 2025 17:50:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07d627a61b498b34c942e540c7ab53ec7da5945558446168fa8eb0ef7948db`  
		Last Modified: Mon, 09 Jun 2025 17:50:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fbe14280fc10e3d7659cb15c758eb8e6f74b8519e0976f39e32787fb5acda473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0772b79940a12e59532346638d31b3f42236ae2e98147997bf51f5ebe2a601`

```dockerfile
```

-	Layers:
	-	`sha256:1c4c08c8bede2f4275a8b7478dcd3745eca9d8438e92a90debb20c3e3c4ad55c`  
		Last Modified: Mon, 09 Jun 2025 18:38:29 GMT  
		Size: 7.5 MB (7465665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f684e5a16efac745911be855112a1fc964ea04503a863b79b280fd33cad677c9`  
		Last Modified: Mon, 09 Jun 2025 18:38:30 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2467a004315f7c909c684af056b24db73736ac07f0c84df80b6881286b15289d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291312402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe38cde0845026a49521278f7fd1b6ff9e7db3937ca9427d085805b8e0b3a7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fd7f4fc1007a30b1949050f0ba69932c1032b69ee73e8eb4d85a1f11db273`  
		Last Modified: Tue, 03 Jun 2025 08:51:10 GMT  
		Size: 144.3 MB (144280585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378d026768dc7112a489469dade2d6b8098e6b9a51e805e66e2e83c3a3a4d1cf`  
		Last Modified: Tue, 03 Jun 2025 18:56:04 GMT  
		Size: 94.0 MB (93950231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a829ef5615b502753351f7118504464780eaaebfcada66d3a90ce9712d935cc`  
		Last Modified: Tue, 03 Jun 2025 18:55:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1646688320cb2a910b38aded6bce9d3e826e0379ed3cbd69d7f1eba29d10cb0`  
		Last Modified: Tue, 03 Jun 2025 18:55:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a9febcf8f0258b79a74a80f5962360a90fc842d78f90d074fe7c1c5c2653628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13eb535caac06d2fd1661d43b97e4db5fe692d24b125d8628bfa5fbacfa8efe3`

```dockerfile
```

-	Layers:
	-	`sha256:1ae581bd58afa70e8d8a4774cd3842c68342abc749c7bd00bdac51de0e399ace`  
		Last Modified: Tue, 03 Jun 2025 21:39:10 GMT  
		Size: 7.3 MB (7322833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f5bd6045ba459831503398ec4be1e572ad5323c38d12bb6730e8adfacbe98f`  
		Last Modified: Tue, 03 Jun 2025 21:39:11 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:347c188774acea7cac0f2f75fe8ecaa634418b792ac28b30cf2df66f9ab357bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273080946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caadc596f5ea26b8189767392bdd21c06d934530dd8b4e56bffe0abffa8935f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23085f00cc2fab5db834062a7c0906b2e2764d3635d1f0a0795de617ce89767`  
		Last Modified: Tue, 03 Jun 2025 08:54:41 GMT  
		Size: 138.5 MB (138492460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609640a3b5f4eb42252b4f8da7c75f750045321461e7dfebe04bb47459c65ad0`  
		Last Modified: Tue, 03 Jun 2025 18:38:33 GMT  
		Size: 86.9 MB (86856034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb57208bc5f371ce0be7df48e2f1b2d0734b1ebdf45949f2918c41b81f451f7`  
		Last Modified: Tue, 03 Jun 2025 18:38:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14556201c47a89cd2882acdcdbe484ee8f8d32c94a390344116752885dc420f8`  
		Last Modified: Tue, 03 Jun 2025 18:38:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c9866e593ea32e2776c8395eed9bda166a1ee00b92cb766e8d13014e1689b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea8170acd48e15f07532838ebd78cbb81240e8d77cb4fd6772c153667214946`

```dockerfile
```

-	Layers:
	-	`sha256:d134c7a67259e70357c660abd6cabd736418a5536267f972fd459bcff8a9d19e`  
		Last Modified: Tue, 03 Jun 2025 21:39:17 GMT  
		Size: 7.3 MB (7304408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940a6e461a25762dc83c8a9994c9244aa69dce4d23068f037ed9a900e6b3d024`  
		Last Modified: Tue, 03 Jun 2025 21:39:18 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:f7ebc5b5b59390d70ae9c94751cb6f0f9c8f413fe8bf710e2c8436ab895c734c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272949954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acec9057fe8ee8ccdd382ce246b5efa4c60d9736b315e44283a612e22d388c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3774d10487b032eb1a2167ed2afb6c687158159ce2ed561584cd53595528c`  
		Last Modified: Tue, 03 Jun 2025 06:16:20 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0c596d41d21a947efff471afa38ec61d8cf66e6ec6a07b5ebf1846aca66af`  
		Last Modified: Tue, 03 Jun 2025 18:35:47 GMT  
		Size: 89.0 MB (88953138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b3fd3840fd8f53345fe08b5ebae1c9e94e1dcfb31d06acfa5a1a195745affa`  
		Last Modified: Tue, 03 Jun 2025 18:35:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cddea6c461131a4a332c5ab8eed664b9566f24136fe17ea54290c7ae789cce`  
		Last Modified: Tue, 03 Jun 2025 18:35:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e156f72741d2b05edb12becda552c623f5de55249580f6e4f39aece85a65e146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7330135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bf26d96e3067f640762d4b9fd1d929e4443ac7ebb7d490cae6509d4f80edd4`

```dockerfile
```

-	Layers:
	-	`sha256:4cc1621b615bfda5956e23d69915f8328a7c440b5ceb8aa89d7131e5fbede2fb`  
		Last Modified: Tue, 03 Jun 2025 21:39:23 GMT  
		Size: 7.3 MB (7314338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c90823a04b46d0520a33154acbc5d533741a96397cf8f1f7d068ea5459525c`  
		Last Modified: Tue, 03 Jun 2025 21:39:24 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
