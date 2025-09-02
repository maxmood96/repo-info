## `clojure:temurin-24-trixie-slim`

```console
$ docker pull clojure@sha256:b05ec1e8566da76cd259b7a87d99a3524ac98e83f01a09619c22c9c492e162b6
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

### `clojure:temurin-24-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:857a8483135779a88b4193b10724666d9e7b8630ccea7d406ae7f0c9485606ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191732443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e30555399bb4e89ab1d6156ba9f7f54ea7398dae9438816e49a2145977d3ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d22a7bfee203ce2dc886b6addac184161a053c956642f2b8efe28a208a8345`  
		Last Modified: Tue, 02 Sep 2025 01:31:24 GMT  
		Size: 90.0 MB (89975181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9ed6908cf2445a2a48712c85ace8a7cef509a9619dcaf92cda9846186b7bea`  
		Last Modified: Tue, 02 Sep 2025 01:31:23 GMT  
		Size: 72.0 MB (71982933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17af21a7b1946e53bfb3389329d4d5cc8487e44c4cad8a522e9e5946c2441b57`  
		Last Modified: Tue, 02 Sep 2025 00:58:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baa8d6e3484613eaa1a0049ed9cf33fc0ef747fb604206ace034bd6bee860a7`  
		Last Modified: Tue, 02 Sep 2025 00:58:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d53f24edc3e772489733659c1a7def170b636c4d0ce5b1a641965367a76debca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca24c17ba00e1a534a2b8d4245e52243d84c82c614a964de3c0f1f8462f0b23`

```dockerfile
```

-	Layers:
	-	`sha256:efd894b53351051f6ffc82b494f35a62e546e53c344bf1ad3ede94a524691b13`  
		Last Modified: Tue, 02 Sep 2025 03:44:58 GMT  
		Size: 5.2 MB (5205885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e5b944ad33903f02fd4efbfef4d3d345731eb897ae87bde0de4f881f18ce36`  
		Last Modified: Tue, 02 Sep 2025 03:44:59 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aafd0b580bbf84593e20f095854e71caa4e0c939d65c4788c500e44f7a2fad91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191033243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c853b4fc46f913fa3c8f5979040089f1dfab9831424a5f769dee3bab8e29c30d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe54333b06ad8dc6a1c19356b2654e06d357097398ccfe7bcc23b46b25aca1b`  
		Last Modified: Mon, 18 Aug 2025 17:25:14 GMT  
		Size: 89.1 MB (89092501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432e489d4777f64036ef55d59490f9cdca26a201ab682742854572244a16b1bc`  
		Last Modified: Tue, 26 Aug 2025 17:59:07 GMT  
		Size: 71.8 MB (71803654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c6f7ab409941e185c29ab3bd060e825a11db4cb6fb8efffefaccc9c5cb6fcf`  
		Last Modified: Tue, 26 Aug 2025 17:58:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e63a0f205a7516d2859b9e9459ed964dda9038a7cda1e233e603dff006e2519`  
		Last Modified: Tue, 26 Aug 2025 17:58:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18c0a50e45cd73738202c7c7bf6a0113157e5ef7a592da2ae1ad49b977e48552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb24945a92b9347949d8e66d9b7a0bbe70275237a844f3086153d69db8e2035c`

```dockerfile
```

-	Layers:
	-	`sha256:d1df14bd68222f5c79aaf51a403e88e6f324b8a790f53b9f03ebd0b2c2bbb719`  
		Last Modified: Tue, 26 Aug 2025 18:43:12 GMT  
		Size: 5.2 MB (5211651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe98071523545ab8248cf53257d917533ec297ddd1b68499a9af9d0c03a86a24`  
		Last Modified: Tue, 26 Aug 2025 18:43:13 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6fe9182c1ced3628cb4ee3f969293455bfb97a80bacf946c3f4ce201ef72bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200902428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a4f98c2824291a674ef3ebcf0b50f781a4bc8bd306e421869be8c5697b9b25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344e68d3b82d646b17664e62a5168a46a359609aeb0118f6b14ccf55dbdbe212`  
		Last Modified: Tue, 19 Aug 2025 18:07:34 GMT  
		Size: 89.9 MB (89918237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4817a93d087a1c6456ab7e8ebdeee6ea90e04274d029d236b9282a417bb7eaa8`  
		Last Modified: Tue, 26 Aug 2025 18:24:27 GMT  
		Size: 77.4 MB (77388934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7625567a49e18995e8c4bbcc95729deb869f31656e00d56bad7f5184c41d3`  
		Last Modified: Tue, 26 Aug 2025 18:24:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a27ad64e62c11ae0d38e1bc7f214637c7b6e97358fb4fcf543669ebe9edf33`  
		Last Modified: Tue, 26 Aug 2025 18:24:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f7b1d366131b128e50300c226c3b8f378a4dbbfa73750df9319637ee02abb09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da7cb7029e080e7dfc73e55e0d9e3489bca21b546d0e024472eeaccb192488e`

```dockerfile
```

-	Layers:
	-	`sha256:7b6e925b0afbb74a409961bf89fd19982a199748de2828ab2febf52bdd173fc2`  
		Last Modified: Tue, 26 Aug 2025 21:39:03 GMT  
		Size: 5.2 MB (5211554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccacc20047026fa7f0cd44ad706fa4fcf392ade723bd7c65dbe3c095117ad85f`  
		Last Modified: Tue, 26 Aug 2025 21:39:04 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:3a38ec7fb7e75dfd7a8b3dc06f392ae7ac22aeb01577645ea326957bfb0c27ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186818699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16aa37274eef08d2355d9db4e31136be2f9ed5d91d9b6b03ef4dbd64589cf09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968e1c5a6cd6f5e83ac6331e97e27eeed78e5735d78cb563574656e787513c6d`  
		Last Modified: Fri, 22 Aug 2025 01:20:58 GMT  
		Size: 87.7 MB (87670405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c56c13f0d69c2806a6ebe3caafc4538f0e8ce498211cca7834c46b4475d537`  
		Last Modified: Wed, 27 Aug 2025 09:54:34 GMT  
		Size: 70.9 MB (70875627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67233fb35526bc104f9cc0d9dad61082856baefbe41e71bed7fd7d2e914ff54`  
		Last Modified: Wed, 27 Aug 2025 09:54:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd4bfbdd1ea3e9d79af79e6a42c011583f55edeb166249605723176bfbfa53b`  
		Last Modified: Wed, 27 Aug 2025 09:54:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c53e17e644c30fd4a8948fe1a01b4b451a23d91e348fb71e0beca496708bf2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b9fde1e051d28c7bc96005bc0a750f52a7041832553ea60fbf1b09d8f2ebf0`

```dockerfile
```

-	Layers:
	-	`sha256:62e671662d45f9bb45758b1f479de6377a0613efcb24a16688aadf015018d388`  
		Last Modified: Wed, 27 Aug 2025 12:37:33 GMT  
		Size: 5.2 MB (5195346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96792f6e5af16e07580383a178bcfd3b0a56e3a04201d9a1a8cf9a4b771fbce7`  
		Last Modified: Wed, 27 Aug 2025 12:37:34 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:714d3d9474592201367080341108f9587f1c09f28e06a06df0e7a51eeafaa387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188010078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fe19cbc65227e099df03aae1da5c8e20aa791b003534a0759b5638cdaf114b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1437af9f0e45b23cbf592c5af25bd0046406e1828f799bdc7dca263bc1547391`  
		Last Modified: Tue, 02 Sep 2025 02:25:56 GMT  
		Size: 85.2 MB (85226361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a05c7f088d871d70cb82290565b2f6d7ebf834fef5e9c8c52cb607a53b8d4f`  
		Last Modified: Tue, 02 Sep 2025 02:30:43 GMT  
		Size: 72.9 MB (72949616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed171166e5a5438077d530cb1c2a33cb84542e41a85c97b667f1e90384ec304`  
		Last Modified: Tue, 02 Sep 2025 02:30:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12b0f941bcf3e7746c0267ac164146f1d0a40697f866f5b6b8e4ab0fc4e8e4`  
		Last Modified: Tue, 02 Sep 2025 02:30:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eab10c059ce03dac2dcf3b05efa4b2a310980a95a403308f0de9d68ef6f1b7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5204f5ac3157ae30b2d465d9945d32c85c578ee0627a886b826a24b59ebe25`

```dockerfile
```

-	Layers:
	-	`sha256:d087cf430e35fb9267b55abd044bde9428e987f96b3294d64582a4fe5c11340b`  
		Last Modified: Tue, 02 Sep 2025 03:45:17 GMT  
		Size: 5.2 MB (5204357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2385655ff47da641ca8ca5ceeac19512fd32d0db29981c9301eac0dc8476b75a`  
		Last Modified: Tue, 02 Sep 2025 03:45:18 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
