## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:cc723d34c7621e8eb26348029d3b6cafdadcc47c8e28fae819701611e58830e2
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6fd302ecfefd537b841a91f5df96135ce205c633552b9c1ccade307c392cd040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280824604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e2a62bec10ccdfee9735227337067350819cea7631d9f9179d8bde463cd9ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:59:10 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109fd49aa4bfacdaeae0f68b962a3a0ff088710278fb4d60c2c7616efd3c8484`  
		Last Modified: Tue, 19 May 2026 23:59:49 GMT  
		Size: 145.9 MB (145905476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d44c16ec3e658368dbcf9f0d080a08de9786763c8c53e6d7dc49af91ff77b6`  
		Last Modified: Tue, 19 May 2026 23:59:48 GMT  
		Size: 85.6 MB (85607463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f558a831ccabf9de81e3761a25a234da59177c7e20c6c2bb0563511a77b6338`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfde21397b7d08e48215cb6d74398ee6134a9142d4a14ce9613dadde6846aa3`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:155618b9bcd6bfc522f7a71532a1fcaed9dbf572266de296d1068325b90b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5962cd15240d337905f17c70b3faf78ff7a7419dd73479500836dd5d0916d0`

```dockerfile
```

-	Layers:
	-	`sha256:ab6a578b498ae1b6c7b80e6a10bb659ce3517b2871c592099c2297007386eda4`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 7.5 MB (7471496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57e0e1c6ba66e8ad28cf4004b02fd553f0b50bdaba8c68c09cb3dc9597b15ed`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df14d1dd6e25996a3c2bd879a0a9822426976fa36dbcbfe2310dd6cc6896288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279829634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d38f6039edbfe057886aafbe5fc5318e6f86c26654f2b47e9a7b0ece501b6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:06:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:06:15 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:06:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:06:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934929ff9f16f89563fafd9fac6adc194b6543d7e750222b702c18d8be093859`  
		Last Modified: Wed, 20 May 2026 00:06:50 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3727efaab637984e5eb7943aa519aa9a29d34eda4bdeda35777ab6d086d56f53`  
		Last Modified: Wed, 20 May 2026 00:06:56 GMT  
		Size: 85.4 MB (85432039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f5cfb8dbd68d9c4d963127554ad70010557d66e784e83c13e17c2cb535b06`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92fc21253dcf377c7fbcdb40ff627129b205a06a8dfe9a9a4ac6de1746e7ae9`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6a0de984340463dff08fc2723b8165a8764f06560c3aa7e67ee79456e9e0b676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13edd7e533de8612a2b2d76fe02624a9ff76196cb636ad4af3f3a2dd73dbd52`

```dockerfile
```

-	Layers:
	-	`sha256:f535eaa8e6194c927c27685583e2247c9bc4d0ced2dd2e09113a434bd47edd57`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 7.5 MB (7477889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5495be2dca635037eb245df204853c2026fa8de4ce6e74e4ac37ee2b205c9f93`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fd1b166de2644d5ed3c6835d0f642b5e7c78888489f919d32e4ba9b7d01b6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289897796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7301adb29f4f724794d4a7b2a3aff2b88f8caf6f60f4dd6a957ec11d4dc051a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:31:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:31:41 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:25:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:25:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:25:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:25:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:25:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06742bfd6f3a4c91a065b055265b2edf944919541ee9c7934bc1931edc1dd4ae`  
		Last Modified: Sat, 09 May 2026 02:32:54 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0ccf94ed9c721debdc00b76ccec5da1cba8395fc372135d831e8998d0ba9f3`  
		Last Modified: Fri, 15 May 2026 20:26:14 GMT  
		Size: 91.0 MB (91007478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea1eeeebf3761a9db0fb3908bffa85c297631425d1c2de6825ccf1dddfe5f2e`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0e1f2d2a5888f158da0e1efa8eeec94a13386aacdf0020ee336424265d6e6e`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a01dd3b2f741666130b5566668de94e901977d38dbeee28bcde9a770aa63d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e548152f25be0b2104fff154a45fe49a539e89d83564c0127390c808e07a373`

```dockerfile
```

-	Layers:
	-	`sha256:da460a52e7e2635f180c562d2c32868b101d7d45bf419c7877724c60c8c0db54`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 7.5 MB (7475803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d87e49d7f5eefde215a1a2d2da4af678606d72920b11213dcc32376e07b8972`  
		Last Modified: Fri, 15 May 2026 20:26:09 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4ac307590d8305424885d9122628de11f18cf8d1958d8ed3a0e196b7b387af49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271881787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78743fa5c6b482f4603f7af64a5aa997cf507e7d2e6010589c89ab45b437b54a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:43:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:43:42 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:43:42 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:44:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:44:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:44:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:44:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:44:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e6aeaf690365e231d191405438cab335606f7f662847488b61ec9fe50ce0af`  
		Last Modified: Wed, 20 May 2026 01:44:23 GMT  
		Size: 135.9 MB (135910432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e15eb3a53f1dad651c0d89ed341e1da21d7e793607a848f0e80a67b8e80ce3`  
		Last Modified: Wed, 20 May 2026 01:45:24 GMT  
		Size: 86.6 MB (86590535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adae7326f127151aae2b1e77bd2e9aa1b7ca62ccf185834a5fd65ee3c41c30a0`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be613211315e837afac3e808945febf5049b912e0600a38398e86a7b0244a8ab`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:58cf925ad565d480b49b2bcf18f5c15fede828d934a301cd48fc1c12f7bca8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4f06eb43e854638a3337a14536cf3f13a4e0dde09dadb81778bbdd02fd3e0f`

```dockerfile
```

-	Layers:
	-	`sha256:4cf5e2d2108e5076ff0a97ffbab418012489140919cd2dc91179d356db1d19e8`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 7.5 MB (7467418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bca84af8215c14c4aa800fa3023e5231d480daa57a94568e109fd277469411`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 15.0 KB (14953 bytes)  
		MIME: application/vnd.in-toto+json
