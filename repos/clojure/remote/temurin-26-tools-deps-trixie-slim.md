## `clojure:temurin-26-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:0f8ceec02f7e5e68dad574e5b2be8170f51b44182c0fccb2eb77d595328f78ab
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

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c2075fe09703aa1c3f20540d0f5897078913d0e14984d29c33a050c1d3b8ce1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193257681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e9de6e5a2725fc8e51863f84a2e1c0e64f4c40bbf256ddfc068a66eb2547ddc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:48:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:48:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:48:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:48:09 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:48:09 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae057653e95449414ffa53a83a009b9002265f7c0d6fe05e931e62d09386fb5`  
		Last Modified: Thu, 04 Jun 2026 17:48:43 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1b41998ebca4e4927e93a37538f9fbb7a51fa6504b90ecca7dcd7257e973bd`  
		Last Modified: Thu, 04 Jun 2026 17:48:42 GMT  
		Size: 69.0 MB (68952373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93ab39d42fde1fc6f37c24efc33bb6ec7901fff3b765db67d8c15f130ac9064`  
		Last Modified: Thu, 04 Jun 2026 17:48:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f756eb9640b6b3628c3a5d2db2f559193fb8484e30d45b048a9124e6380403`  
		Last Modified: Thu, 04 Jun 2026 17:48:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7679b1bbb794d5628bfe78530d7b4940edb25bdab98fac6b1954c95bd3357d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7631834a9ad5e3b1b2b8c190d509129eff5deb8acb2d1def0b287e983697ebe3`

```dockerfile
```

-	Layers:
	-	`sha256:b56cd310fcdc0ecc499734a1bccf988b1db89056f77634428c19b49d75351a89`  
		Last Modified: Thu, 04 Jun 2026 17:48:40 GMT  
		Size: 5.2 MB (5222133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0e33d3d8f9757f1eb608bad0a5aa347ef18fccc6cb95de1fddd923312075c51`  
		Last Modified: Thu, 04 Jun 2026 17:48:39 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:048b8e079f3d97bbe4d4d24302294342292679fe1acbed0233d65ca39fd72d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192424683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c94fe35fe46be8ab61dda9033a2f543d7658292955ac35b623f0e71d4ddb296`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:48:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:48:05 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077db24e093cda06ad93ba6d74b521b15ba4d27fd6ca18e48832eec0e3153fa`  
		Last Modified: Thu, 04 Jun 2026 17:48:42 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9ba7a92e2f9d5d694fc8e0a3e2e79bee43601c295897de3a6450f71dc0cfa8`  
		Last Modified: Thu, 04 Jun 2026 17:48:42 GMT  
		Size: 68.8 MB (68777375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62a04b083be732c123064141e7f4d5d5cad6c88ef7c5a5e9850a64bfcfa2205`  
		Last Modified: Thu, 04 Jun 2026 17:48:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494bdaabf37437adc091cbf6a32fa989f9d7f9dad1fbe50f25ee3e1147d6d84b`  
		Last Modified: Thu, 04 Jun 2026 17:48:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8c2a8ef02236f9f94aaac156cf9b31d09fd62f0e428e0fcd633aa874088cd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4d6429be6ac56333172be354430685fa35d31b6f54d246ae26cbec6bcdccb7`

```dockerfile
```

-	Layers:
	-	`sha256:790da101ceee23a4077c1c3309cd5fc682b83b1df49cbcd436c2621430f819ba`  
		Last Modified: Thu, 04 Jun 2026 17:48:40 GMT  
		Size: 5.2 MB (5227891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d801393e88b5bde846448b8a2122abca3098fb53e846e385b5c366bd345fcd`  
		Last Modified: Thu, 04 Jun 2026 17:48:39 GMT  
		Size: 16.1 KB (16076 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cda5154c751026184b430a854bc70e1f6efa87c19b685e11a1a92ff2f52334c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a113ff1630af652abc13d8727f9edac59027fe34e45bb17a25606f81804825`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:11:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:11:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:11:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:11:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:11:50 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:12:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:12:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:12:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:12:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:12:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f636b6ca285aa4b80f814ff4cd48e03ca678cbc494379c15e3bad72919b21fd5`  
		Last Modified: Thu, 04 Jun 2026 18:13:14 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c58400a390e56b41a82a63618b94da041df19edad3e213dddb1d4a476b4282`  
		Last Modified: Thu, 04 Jun 2026 18:13:14 GMT  
		Size: 74.4 MB (74369309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1eaa3d8c91982554b51e311003612f0bec24ac01e6e1c5ada3daac8ee5c0ea`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c49dc6ee02244e4732d9e27a5cf892eb2fdb74011adafc8ef92cfba49d570f`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a79d5a44c9ba3cf3b5214e37f2cdbf1f81109ffecafe8f14f1714f5c8d7d179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfad9a9bd61b935b0eecfb093574e60a775edadb8f9a4fae9ba4bec2e620435e`

```dockerfile
```

-	Layers:
	-	`sha256:4566d547b7aabc17700b41d1505be6630350b11e74548058833d77d38f07d3f7`  
		Last Modified: Thu, 04 Jun 2026 18:13:11 GMT  
		Size: 5.2 MB (5210440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ac0b681f4c8e100ee1b95b440611f97d52583620d7db7fa44f73967601efdb`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:60df3988664ebd25c6b1e9c222eacbb253e38719069a3c659a6ff3a8600670cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190316488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca7e9867adad36ff194901779b1850a46b627c8c167281bf13dff00d2690242`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:47:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:44 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d223e7f61fbb56fa858fe22e15cc6c6fe102c454de5b2d5f8ffa9a90bae0eca3`  
		Last Modified: Thu, 04 Jun 2026 17:48:30 GMT  
		Size: 90.5 MB (90536985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19052f635d755aba63248f7522d253017a7ee72d2e739ebb7609bde471be5de8`  
		Last Modified: Thu, 04 Jun 2026 17:48:29 GMT  
		Size: 69.9 MB (69932537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fdc48e22ac4c41a2b9746fb04871ab29038fdaff2a7d059e931f777dc8ee3d`  
		Last Modified: Thu, 04 Jun 2026 17:48:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1932f370c074e476645aea7f3d03b24b9b408e1a962ce49f97c656aff006950f`  
		Last Modified: Thu, 04 Jun 2026 17:48:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a342d8885fb2d88a4a7404c5a313e14dfa2c1d4f57895882d11e2d1ef3c26718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668bb23831eaf1a39f15261dbf3ad7011d65cd94e4a1266a29c2a995e45fb205`

```dockerfile
```

-	Layers:
	-	`sha256:2abf2c95e24d578aa212afca096c23a29fcb4663fd71ff1220be63ae1e2d9e9c`  
		Last Modified: Thu, 04 Jun 2026 17:48:28 GMT  
		Size: 5.2 MB (5203243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c6df963cb55f4a2c4e6a28248528f2e476f55d307b5dc1d6ca33a2fdcd0109`  
		Last Modified: Thu, 04 Jun 2026 17:48:27 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json
