## `clojure:temurin-21-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:3cce6b5f4f7a8f361e5383e4c0c31b97b729492f4aaba2bd58e807e97d78ee80
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

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6c46b8f32119eddeaa999489a5e3f52cf033478a3ab0aaff195e03e5f4128fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292653331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65775fe3ee73890a904b708a8314deec3d3b3d548ff296ea6c9b9055ee885bf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:54:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:43 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6bed3d56e15ed9172c5fb79c2ce7db70c5e3396eaf659662c462a330b3fa68`  
		Last Modified: Fri, 14 Nov 2025 17:35:18 GMT  
		Size: 157.8 MB (157825965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1299984f1b66822240c7ff201e8848b8ebc89599ba48c720e346fcc24573c846`  
		Last Modified: Fri, 14 Nov 2025 00:55:37 GMT  
		Size: 85.5 MB (85540694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74e39f36d315e48a3d7e18aa4764d18a8b9e43c8756d429e8b9ad78517c5afc`  
		Last Modified: Fri, 14 Nov 2025 00:55:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d41c886681c9349aa577b2d4c731dc7f873175777d2034ab05695b3a0ac8fc7`  
		Last Modified: Fri, 14 Nov 2025 00:55:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8cdf2e2bc07f47633bb0cf76b11018e01b10da90fa8afbf15c97814b0a84d86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f9d2583cfff94cd326923ac56a92cec0be94cf169072dfd74b1ec8d5e40984`

```dockerfile
```

-	Layers:
	-	`sha256:bfa88d4fde451e0ba4fbc8b3b8aebfb9b20b9d41459211bcb5c01d02fbef203a`  
		Last Modified: Fri, 14 Nov 2025 01:46:02 GMT  
		Size: 7.5 MB (7470003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fea6effe609d44113d779fcfa6dbe13518caca128d5a97705bd220f27c3abbc`  
		Last Modified: Fri, 14 Nov 2025 01:46:03 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:542d3bfca02dc37b6628b60d68a7ed9aa0d6a1c7ac95479858fc6ecce6cfc0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291122554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d692bd25a05dd27fd9b7245fd920d3849eec4563ec3bde7ce087a1182f7cfb64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:57:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:57:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:57:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:57:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:57:04 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540b8ef56433ed6b440d145a164fe893a8e71997503087d6293b2c4504237ea0`  
		Last Modified: Fri, 14 Nov 2025 00:57:51 GMT  
		Size: 156.1 MB (156107652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f615759593ea7891dd852497905c7838369d2588b40b911323d4970e62be353`  
		Last Modified: Fri, 14 Nov 2025 00:58:07 GMT  
		Size: 85.4 MB (85363427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4420bceb62b22a7e09b5ce5ca4251727503e01d745e6eb54f66fc089e6a1e3`  
		Last Modified: Fri, 14 Nov 2025 00:57:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6914fedde2365d86db55589329992b9582a1082fc68acaa72e91f1986f16030`  
		Last Modified: Fri, 14 Nov 2025 00:57:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c8ef2e2541234be5d6bb0ea0181f777593d22810263f65d4d59e6086f5949e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40bc5764c50bd0f9bbe1262db8a909e4bcc60286320283702afb52870a37619`

```dockerfile
```

-	Layers:
	-	`sha256:1405823eb2b36a8ab7c6a89acee26a5470662cd328660c0088c9c69360e3533a`  
		Last Modified: Fri, 14 Nov 2025 04:41:04 GMT  
		Size: 7.5 MB (7477033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984cdf1d34a78bf48b0b087c59a02b58eada2bcf14b6d567d1162ffdef15b532`  
		Last Modified: Fri, 14 Nov 2025 04:41:05 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:093f71309496449537ab110c37ddfe05b5dc6616670b66ed7f3167569b1e2a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302004039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4570c4d56dc457d6a46a28d3ad81f261ec77787311608b7a0c11db1ddee7d058`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:22:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:22:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:22:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:22:47 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:22:48 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 14:17:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 14:17:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 14:17:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 14:17:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 14:17:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1846f067e1ffa573181ab2b7636dd7c09e6a6163953bc6affa72a6b0b1d4e9`  
		Last Modified: Fri, 14 Nov 2025 07:24:03 GMT  
		Size: 157.9 MB (157942937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4092c39c82e8d38613324e16e4dbc7abe54de79f47a1691a5cb753e6aa9515c2`  
		Last Modified: Fri, 14 Nov 2025 14:19:10 GMT  
		Size: 90.9 MB (90949927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137d2204c2501d908c7b7d01969b3dce9bd6447ed1bb2e79fcdcbbf829352419`  
		Last Modified: Fri, 14 Nov 2025 14:18:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6c26e865fcc39e9019fdaa8c545b20b33a4b18057c782daefd3753572173f0`  
		Last Modified: Fri, 14 Nov 2025 14:18:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7ebaa2e6a6b21393d0f4810c1ec8d94fdb6d9aa225e9a0274452fabdaa111bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b811ffbd365285fe477c0a5a9d37f2fd6e0c793df96057abc107934b63711b4`

```dockerfile
```

-	Layers:
	-	`sha256:ec45480bba58cda1e75fe16080dd6dd59e6e8c9d79e157e3720841d61754a565`  
		Last Modified: Fri, 14 Nov 2025 16:36:11 GMT  
		Size: 7.5 MB (7474422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d1e86e10d0c2fd407b9886fc09b6ce05816534b554aec3a8c87f05c0495250`  
		Last Modified: Fri, 14 Nov 2025 16:36:12 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3f3c827d11a598792a903ce6ddd3d0c6bc2cf8fa9f34bf9513dfcd18c647a472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289392829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909a053a98e79f7e81dd7d8348c081436d3f8395301155ff54f996aecf0bba9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:52:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:52:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:52:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 03:52:51 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:15:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 04:15:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 04:15:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:15:27 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:15:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be84f75f5cfb38b82da427fff2f97f31bf8aabe180cf4ebe04e740d623ca5d`  
		Last Modified: Mon, 10 Nov 2025 23:12:45 GMT  
		Size: 157.2 MB (157194308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eec011c3b8759ec22995899302c15507233f7757c20bcf1bebba1e61eb4163`  
		Last Modified: Mon, 10 Nov 2025 04:20:09 GMT  
		Size: 84.4 MB (84426553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b0492d65e15b12af28821f9217592654cff7714eaa6738f169c154c7929292`  
		Last Modified: Mon, 10 Nov 2025 04:20:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15995cf148cc1596857c774e0d9e68faf1eddc91d9b6f03aa087bdd6e2340e8`  
		Last Modified: Mon, 10 Nov 2025 04:20:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eabdda8c99e38d70b708f15c90df6fa1c80ada9e4d054c22c87f0c032ca90c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b50eca349c45e82bf9da5a10f1852163938e372a612ec00f09de75270a58f5c`

```dockerfile
```

-	Layers:
	-	`sha256:9c44329370a29c86084849dc09d5707f7ac57b41698ace625cf57943fc11a40d`  
		Last Modified: Mon, 10 Nov 2025 07:36:45 GMT  
		Size: 7.5 MB (7457916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e8a3802a22d9f5fdae2c94330619569c002a253dee7d03a507f3bb67ee5e96`  
		Last Modified: Mon, 10 Nov 2025 07:36:46 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:19e708457baebf82c5f27deb3021318ee08929c4e4fc532822bcaddcce5bbce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282931673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccaeda8039eff6de22c00a712e5170bb232fdc377a2298fd02f9a24c1fbed27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:00:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:00:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:00:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:00:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 01:00:06 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:02:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:02:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:02:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:02:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:02:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f61465f3fdbb3923a28f1755c9191bead554b0aaa1919ab4d89fc9130dde133`  
		Last Modified: Fri, 14 Nov 2025 01:00:45 GMT  
		Size: 147.1 MB (147069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5ba9516e3b25fdd0395304f7e2a4bc461978f2bb44edc8377ff23e5f8f3c86`  
		Last Modified: Fri, 14 Nov 2025 01:02:57 GMT  
		Size: 86.5 MB (86508502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07146e89992e9323ea1520ffc3eb7b265b460a2ad3115a2060d2251f29d57320`  
		Last Modified: Fri, 14 Nov 2025 01:02:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb347ac221689350d8cc9625c783bc427cd4ae2c835dde982ed6418de4065f9c`  
		Last Modified: Fri, 14 Nov 2025 01:02:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bfeb1a135acf17c0d81f617a91ce9de49c10579785b6c65e5e1ba5dcdcc2c54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ec8bff32f275b355212c6ce6ee9d89ed120bba784846a8a5e7a6f3be62aba5`

```dockerfile
```

-	Layers:
	-	`sha256:d2af0290af33c2ebc2b727dff013f5e270dd26970a4fc2b2665bc879f18dc478`  
		Last Modified: Fri, 14 Nov 2025 01:46:28 GMT  
		Size: 7.5 MB (7465925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7852d060c84f3b53370205d554ace4e858914b9802b9df04dc79115df83043c9`  
		Last Modified: Fri, 14 Nov 2025 01:46:29 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
