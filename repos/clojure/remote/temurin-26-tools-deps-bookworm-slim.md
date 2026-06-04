## `clojure:temurin-26-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:7adf103c58b96a1bed176d36ef2debf6339683c19b3c82d3a32da4f6d6ae64a0
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

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:aa9755311090e7661f8b80178e8153d4d7acb06200f1cc7b22177149fd82e0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189400002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000cafff9ba1323bc5ed5992e7560a4993316a1b5ee79e030d60618de776f0da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:41 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef54e0e7065aae35ab4ce8dfb665e55386f20fd738a50c7a183be4a8c5346c0`  
		Last Modified: Thu, 04 Jun 2026 17:48:14 GMT  
		Size: 94.5 MB (94524374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bca024635b76f2fe3f04f0d0662e2b701cb8d29db8e80eec4208f1cab24e9db`  
		Last Modified: Thu, 04 Jun 2026 17:48:14 GMT  
		Size: 66.6 MB (66641043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9348323c8147acaa2ceb9e1578e94b194d8c351af843f9ee0034837dc26e8e6`  
		Last Modified: Thu, 04 Jun 2026 17:48:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ff2b24badf1450abd70b022fbf95dfc70b39e081fcb49eac2c381f57ff5095`  
		Last Modified: Thu, 04 Jun 2026 17:48:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce8e00a1c731d77a06df2bee2bc54aee8983ffbccf92e9f88bb489f9db416b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27164f4bcb75bb1cb2cb33b694abb9adb66cfee2498861c3185f220841cba506`

```dockerfile
```

-	Layers:
	-	`sha256:28b3557837d35ade767d4f0caafa0504e43d84d2fbf0f81b1cd9f65d6a3e6b6b`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 5.1 MB (5078872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b825edde962a05079925fec38fb2fec57d32131eeebd3280a13d1a887953983`  
		Last Modified: Thu, 04 Jun 2026 17:48:11 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf93e446eab084faff06a0a295054e85d6f246d7945b7813b2bb43453b1518bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188262558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fd14002624b5bfd7e11f5b7be2811bcc50bef4466a6d281d162e6831d23ab8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:40 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5684be6891a3510f705b227d4f5b7efd08bdab2a5f3543ee1a44ec1e8cef7e8`  
		Last Modified: Thu, 04 Jun 2026 17:48:16 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3ffc687c2b23d622e4c34d182aed1d07d9cf6953732607397c16c52d4c31cd`  
		Last Modified: Thu, 04 Jun 2026 17:48:15 GMT  
		Size: 66.6 MB (66642124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e7b86d09e17c0c6d4ae98300e03dc07edb3a3b30ba935b11d66d2c49238219`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b463853fbae0298c5c30023e24fef91229eeade58573146e6d76455339a5da`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2316dadc63a7909f25d1fe76fd9da70cfc0cf48df397dd04096969f777b8acdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bb3174e505cd41048759ee18355b3120e2b13d244b882dd3e4c4b257913388`

```dockerfile
```

-	Layers:
	-	`sha256:1cc64bdac657ef5f503d60ab4bdc282f3373f307d53db9e72c376b2f441b8aba`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 5.1 MB (5084630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:997c1825159e95929f3cfc775fd7ab0f95416121eff20d12cc3aef7b8eb65fa4`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dd22c5a51788589bc708029aa1887f44f42623ac553ab7779582f27622812773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198454714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75bac5b407a2d5c8a848a6f95487fa2f35ec2d789d94990b50062cffc689ee8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 18:09:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:09:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:09:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:09:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:09:48 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:10:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:10:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:10:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:10:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:10:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18416d856c46dabef603a8b5e34f6bcea406e58e90d0f8512480fa42d49830bd`  
		Last Modified: Thu, 04 Jun 2026 18:11:04 GMT  
		Size: 93.9 MB (93902080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc68c3dfb41e011ac15554437711da52b197ed2b6837cfb5b8f556a40fb73313`  
		Last Modified: Thu, 04 Jun 2026 18:11:03 GMT  
		Size: 72.5 MB (72475846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c996297fd6377162c53edd74a31f171657849ffe2442b0e4679ebf9ce7889a89`  
		Last Modified: Thu, 04 Jun 2026 18:11:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4266dc4f5fc342922b87352ef53bcf5c2b1817470b02097ad0e0fbdabd70ea3c`  
		Last Modified: Thu, 04 Jun 2026 18:11:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bb276688c6da46b98ba29823a6e86536c31a6f945f9cf7adf432744235a8285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c1955b01644bfafe197f1282c192787dd64f2bebcd0747f29272853549ee32`

```dockerfile
```

-	Layers:
	-	`sha256:2d987134854fb195fec383d91459137c732b0910b657a14ae052f9da2bf60d7c`  
		Last Modified: Thu, 04 Jun 2026 18:11:00 GMT  
		Size: 5.1 MB (5067966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d845f134d4c7e076bfbee87fffa2b76269d2d2116cf070a2f7a7adf6383c7c`  
		Last Modified: Thu, 04 Jun 2026 18:11:00 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d5802c8486d7216c9d45d52bb24c54ab6b80f494bda83f28ee6fe8003f1577a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182878463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d1afc07abd82799bb4d71f59852d7645eafb2281599c28ea544a05e944cf76`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:38 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b063d353bc70375acd44707944372fe5fefae3ec533f153ff30f5d841083f09f`  
		Last Modified: Thu, 04 Jun 2026 17:48:22 GMT  
		Size: 90.5 MB (90536969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68806e77dd902027c28969fba276e3474fa0d6707598c8170c012856f3c72441`  
		Last Modified: Thu, 04 Jun 2026 17:48:22 GMT  
		Size: 65.5 MB (65451855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009710d5a551bcfd4e8b40a1db0b69659373905dfd68100f0620dd4453c28e1d`  
		Last Modified: Thu, 04 Jun 2026 17:48:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d567d35dddf260068f2ad5b2c1659c548cf50b520f576986301f75a3c9ee091d`  
		Last Modified: Thu, 04 Jun 2026 17:48:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebaed629905884f9b636caddcca53d9bbc3b78c9f708f292573e6dc2d5b3a767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e538eaa4f7ebcceb5c62b60c0485b3c666c82ea032af913637a5c9d40dce0251`

```dockerfile
```

-	Layers:
	-	`sha256:5ce86145d9f7de8267a97622f73c75ad6fb9c13c9d353c8ca6881d84f91def77`  
		Last Modified: Thu, 04 Jun 2026 17:48:20 GMT  
		Size: 5.1 MB (5055379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44396c94e8dfbb99910fd15ea0027630e19562c9d710d4383a43d26e83e98cc`  
		Last Modified: Thu, 04 Jun 2026 17:48:20 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json
