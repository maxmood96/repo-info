## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:fcd12ce8b5e67aaa88e0ffb8165807aec2c33b419e677b41a76e6672c37d1a09
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ae445d38b582ce996001a7f0290074d45e434bb72d5419a03536d40c8ce506cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292692966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8c5ab3c618e0629e453a916c6641679f208ec7ffecfd09bdfc4d8a01cb074f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:44:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:59 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c1a55ab34205ae5495f8f348322ce0ba3ec86333ca36c7a95cea7b5c2ae37`  
		Last Modified: Tue, 17 Feb 2026 21:45:42 GMT  
		Size: 157.9 MB (157857085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4077cecc28b5e3adcd43af3146b17a9abc4965bb294734593e7f607bb307a80`  
		Last Modified: Tue, 17 Feb 2026 21:45:41 GMT  
		Size: 85.5 MB (85541887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d796ed44c21cf96bc782790dff08b6e0955079e9bf16229422f387d74b496eef`  
		Last Modified: Tue, 17 Feb 2026 21:45:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cd2028459ba2654e3258108f4d80f312203bb9aa45b9c5deac638c7231e0e7`  
		Last Modified: Tue, 17 Feb 2026 21:45:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6fb1a9b715b4c71d97cf9415abcd3f88afdf8c06d22eeef022554650b828b004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44812175c7b8c196c1dbc8a5f23250bc97e638430d5a381502900ce426ba324`

```dockerfile
```

-	Layers:
	-	`sha256:dbb92abb0206d95b31555e44fc2187238bd0f8184aca667afd8470c1d2e4188b`  
		Last Modified: Tue, 17 Feb 2026 21:45:38 GMT  
		Size: 7.5 MB (7470932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20df9eeb9945fe53839e262154cf34800b4208bdf11568796250798644806f3b`  
		Last Modified: Tue, 17 Feb 2026 21:45:37 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26d3b48edd2e20ccdf7d8facc9500ff5194c2d4c166d2ecbaf11f19323fcfc14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291147277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6fc0295b46878e1f5de15770710548cee1755037332adc4faf85e67a97ff17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:46 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b622708f07ce656be673ea8c4bef6f61418863a7a4307cf5f08622c21beccbe`  
		Last Modified: Tue, 17 Feb 2026 21:45:31 GMT  
		Size: 156.1 MB (156133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83711532aafe05cf7c90b3f95af1a3e6261e207e18ebf6f2e8a7b182ca18df6a`  
		Last Modified: Tue, 17 Feb 2026 21:45:30 GMT  
		Size: 85.4 MB (85361146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeab2e2a2f374cb7c0a0230e18a6da9c8e2a4585363f3666399cb8c2b16a807`  
		Last Modified: Tue, 17 Feb 2026 21:45:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb20c1fd12dcc10d4f915ae1f4f79b6a8ab121311364bc5f9a7ae9e90d8e31`  
		Last Modified: Tue, 17 Feb 2026 21:45:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:575b6d046304e92c4884cde408c3605b7b305c82421be96265fcad8b10e00235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c27458a8e675f99cdc5f2fbafb4fbd84d538131e8a7939558015a51a168ec`

```dockerfile
```

-	Layers:
	-	`sha256:df304451d5ddcbe1a1c4a5b85ebf77bbff5085702fb30ab6a3b73d797b0d47c0`  
		Last Modified: Tue, 17 Feb 2026 21:45:27 GMT  
		Size: 7.5 MB (7477962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f5ad47f0a8afbae74a0e8d4a6fffa021c432a7022d99429b72a0b5509c0c32`  
		Last Modified: Tue, 17 Feb 2026 21:45:27 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:93dd1aff66ac5aa40ae09f93e3e35acbb84a6acfa42ca56afacf48347f488cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302038027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82a57bea12cbdba22ad9eebc6883858057284b7d95aa352a5ced68173dd5ff3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:37:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:37:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:37:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:37:56 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:44:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:45:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:45:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d803d46010c6f6fae7ea82f881a836bc9d2bf4afad631cfb7ffd52616e4eec`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658dc509fba83dc2db068bc8e8fc1b00a423baa6138f80c8f6e1ef787c8cc2a1`  
		Last Modified: Fri, 06 Feb 2026 00:45:56 GMT  
		Size: 90.9 MB (90947375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57375455d750ea82383acda1d01ccb215922e56b701bcee8390cb6e0bb6555a`  
		Last Modified: Fri, 06 Feb 2026 00:45:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d14c407954658464ba427b45e5d4df4f7bfb10593481a4ecd3e42d9773d07ca`  
		Last Modified: Fri, 06 Feb 2026 00:45:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7fbee5c91ca31321eabec98b288968c211fcb8dd3489b77d2e0bedefc66f4922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554a8693136c1fcf5a1bdeccd5dc62872729e0006c78c6ef5b3b7e914196c71e`

```dockerfile
```

-	Layers:
	-	`sha256:68ec770ea5ab1089c664baebcd118fdf8ddeacd9cf8eccad16d2c6b4f2f1be29`  
		Last Modified: Wed, 18 Feb 2026 00:03:08 GMT  
		Size: 7.5 MB (7475353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad06f8f7f337dc20f8a056137fde312325b2b9c7661cb0fff1ae5a703f41d5a5`  
		Last Modified: Wed, 18 Feb 2026 00:03:07 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b0339bf294ddbfb6a88a78dca8d6a6dffcf673fc507323b70d850efa4e7f63da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289419723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191fead5ad8146ec1eb1b511f2ae402b229bfc285f7fc7327780ec7bc595c935`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 12:14:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 12:14:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 12:14:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 12:14:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Mon, 09 Feb 2026 12:14:12 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 12:37:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Feb 2026 12:37:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Feb 2026 12:37:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 12:37:19 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 12:37:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4679cba1526d236633941ffa3c6d13fad991fde42b4ce1329897774df20befca`  
		Last Modified: Mon, 09 Feb 2026 12:20:51 GMT  
		Size: 157.2 MB (157216869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755299cad569398a38aefd102518b8c5777eeb752a0a5a79ea3ba6e2d56181a2`  
		Last Modified: Mon, 09 Feb 2026 12:41:53 GMT  
		Size: 84.4 MB (84425046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63292f1de807ffff54d5e4f9b48a2948c538b46d1be9972e3580114133bcc8d`  
		Last Modified: Mon, 09 Feb 2026 12:41:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e272233738beb60e9445198971cee1bd980a905a71966322408a645b7a6fa6c7`  
		Last Modified: Mon, 09 Feb 2026 12:41:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:130dea22be247b6947d40a329d718d3a7b62298829103caa82dd18dc171124e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc8ccf30604c69033055b8394c6cf6b17b398579cc8f54318f6f4a2c06f6840`

```dockerfile
```

-	Layers:
	-	`sha256:fc4bfec44f19a66d45ca05d1a611c8257317e6105053641281e948558e3847d8`  
		Last Modified: Mon, 09 Feb 2026 12:41:41 GMT  
		Size: 7.5 MB (7458847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e131dcea963e92c901dc81d9c378cf5c39a19a5967eb402157bda84f5b56b11f`  
		Last Modified: Mon, 09 Feb 2026 12:41:39 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ad4efa0f1ff44e6b9ea8e50171133eceef3146e2f760ee245a8c10850470bfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282972725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68264605dc710696703803722acc2481540aae090a756b5844b3f8cc250d082`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:15:25 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:15:26 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:16:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:16:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:16:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:16:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:16:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd88f16461ec869373aa535dea49b1259a9763eec4582c81d77a5a9b41618a20`  
		Last Modified: Tue, 17 Feb 2026 22:16:51 GMT  
		Size: 147.1 MB (147105301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2fa87c06f082dea70f8ced0c3d49807ddcd2a8bf157d199a04c8197ad09b01`  
		Last Modified: Tue, 17 Feb 2026 22:16:51 GMT  
		Size: 86.5 MB (86511999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b69c3ba2a5e6911169cdcaa6e4e409a2b4ed75594a0bab0dc3aa1185adbbc`  
		Last Modified: Tue, 17 Feb 2026 22:16:47 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0db70671bc3f64a0a7184007696890cc3176064785e412732ce1024d0d0481`  
		Last Modified: Tue, 17 Feb 2026 22:16:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:30dce606b8c9d7a45f893271259d45912fedaae8903a95a1f73bbdd0f2edb3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d02f1e72e5b087d1064a13b43a6912fd3ee54fa3f11531299a6e296b0c8f1f`

```dockerfile
```

-	Layers:
	-	`sha256:a07e42a7f64213dcfc7f7fce3ab6e7cfdaa3de083b3e79957f56d0d38b85fe55`  
		Last Modified: Tue, 17 Feb 2026 22:16:48 GMT  
		Size: 7.5 MB (7466854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a7396317ceac0dba16ed684660e824da523b7e69b47dceb7999676018a5e57`  
		Last Modified: Tue, 17 Feb 2026 22:16:47 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
