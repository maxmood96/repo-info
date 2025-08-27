## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:0ec891bfcf360477a6f0076d8262aa51a0bd1c5d292e6b7421cc12ca04221c6f
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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a98382320e74e999b26e78235b4e7d132a39d2bc05c41002828bb7255b595341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191731874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875fd323993c9d8a075350fc53bf028b38d47c3aa60c65c61f1351375e87df2f`
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
	-	`sha256:e8416f29fca1026c5c7a3c8384a49ce4c6feefccc6be86dab25a49668aefcf36`  
		Last Modified: Tue, 26 Aug 2025 17:28:26 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca0b19c0abc80869a51987f99243690c29372c1f15a5ddfe013414c844ac57a`  
		Last Modified: Tue, 26 Aug 2025 20:14:12 GMT  
		Size: 72.0 MB (71982317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17045209dfea8885051d2086f1218a9bcc2b6c2eda6d8a8389b8e3fd899dfad8`  
		Last Modified: Tue, 26 Aug 2025 17:32:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7fc08c00879e3915edbf78e7d9813b630a58de2bd0e4f6cd96e4535c6fb79`  
		Last Modified: Tue, 26 Aug 2025 17:32:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5b0cdcd9047e8c2ce6f8227289fb6fa3804091022a6701d020de54de93b9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fc585ed345baf88b59889eea8852f1c8c91f8a0335d5d292b28b0ec5934f7a`

```dockerfile
```

-	Layers:
	-	`sha256:8ff5293c604f843de81052eaef13853d42df2c0d70adbe1bdb199983d41ec6ef`  
		Last Modified: Tue, 26 Aug 2025 18:43:05 GMT  
		Size: 5.2 MB (5205885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238763448f0a2c268f846f38d663c74e8a5bdbeeece932b34f910110dad7f59c`  
		Last Modified: Tue, 26 Aug 2025 18:43:05 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; riscv64

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

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f65de55a0f61a5a4639abbcdda8ab9168db8668ecad637cdd7f949cde7af3d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188010192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135654e9105f7d147bc72d2c6afdb3bb731990f1ff3b0ce5abc8a36329e9f67f`
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
	-	`sha256:ec43252ef36a8b912f0b9161e21f8c05ad6c75f47c25da09877a4661719d555d`  
		Last Modified: Mon, 18 Aug 2025 18:26:18 GMT  
		Size: 85.2 MB (85226400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f6dc2ce0826786f1a8e1e9960886ae873e5e453ba7c949f3fa04e96b749734`  
		Last Modified: Tue, 26 Aug 2025 18:53:10 GMT  
		Size: 72.9 MB (72949690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e2cb30f563a3f26843d3560472618630165dd835497bc4efbc8035989064e8`  
		Last Modified: Tue, 26 Aug 2025 18:53:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8f1930e7d2ccdbf10531e6814c85e63be7fed74972890c79c1e0cdac9520b8`  
		Last Modified: Tue, 26 Aug 2025 18:53:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:adb5dc8d8d75165f89d23ce3c1dbcb00358f03b2bf604125181ab9d41f273f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fefedc5523d0ae6e870192d06d3da6cf5bad00f9562fef701a8ce277dd79f1`

```dockerfile
```

-	Layers:
	-	`sha256:6afe502212c7b60b410656767dcc9c042012e7531e6e90d3d45bd4a8cf50940d`  
		Last Modified: Tue, 26 Aug 2025 21:39:09 GMT  
		Size: 5.2 MB (5204357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8de19593509fca85bd1e7177252af18a706b35c5419829f1fdaa47e47a7999`  
		Last Modified: Tue, 26 Aug 2025 21:39:10 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
