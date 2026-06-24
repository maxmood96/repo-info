## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:f768cc38101a0bcc5dcf373d0ba5f514bb92b27b73fe382ee848437c4bc2e69a
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3abfa93645062e9177aba70d024e2de7f5f6ce0c3dd2765af53acc90ae8ac0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290004764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7211b09584054f3d556ccd429b239ec6e76ef3bc3a6c7b02d62dc635d427a203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:20:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:31 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:20:31 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02630573b9f74ad2005ea8c3b3531cc756ba764e1c1cf67c9b602c00e840d5eb`  
		Last Modified: Wed, 24 Jun 2026 02:21:13 GMT  
		Size: 158.2 MB (158166915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b59d5db273ab25840471d64accee65afa259a067f42e110b229c351ae67ec`  
		Last Modified: Wed, 24 Jun 2026 02:21:12 GMT  
		Size: 82.5 MB (82519551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df49ae55bb0c8a48d8c4a67f30f3c43f3c3f178a046e54ec822934cef1de984e`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fb94fea7bedd9cb3aa8911f9868dbb5cb5f1777bb7d72414d10373c19ec49`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:be372e72db464cc7249ff5fab7d0e413485edd5fafd50713cac796135ea5132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3706986703420b8215fe7149bfb3ebc31947a4c141cab59d4909f326a6986b`

```dockerfile
```

-	Layers:
	-	`sha256:69c9275f14d7a078e42fb9357ad01df06db49dbd6daad1d36f44a4cf178aae21`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 7.5 MB (7470623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3f3da2a1045504bfc20b3551c2d7b3796ed107017dc3f38f16931e098392a`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1b0663d1581ace513be34ac64a30e660784e2f4a877fe021bf17a88a2884a4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288479177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8595393381af6c870bc91d8280bd63295f63af9dd2a1236a5e9d837d491aca08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:27:00 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:27:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:27:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681b265d72733ee19523ddc7904af3b86def35b92baa81d57f4d39027caf3c64`  
		Last Modified: Wed, 24 Jun 2026 02:27:42 GMT  
		Size: 156.5 MB (156461252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b65ec255c5d0ca2e9bb880c7d8e9441ba1848358b9ad336ba96832c3b42256`  
		Last Modified: Wed, 24 Jun 2026 02:27:41 GMT  
		Size: 82.3 MB (82338487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9cd35e8de03237d1d818d586f6487f7789fda208d0c8dbd56292791f2710a0`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26172dd42da065021c5d88b2f7a0d26a7f0350755d0508105d43eb37cbc93806`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c5dc8f698f5651b678873896d876f6b2f917e8c28b99a7a2f74ca263d86040c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14867694662859ec38648731f9f99c7f0b8e428c6f76c1db63dba8c9dff966fd`

```dockerfile
```

-	Layers:
	-	`sha256:09a4b8e6e32d6ddf49260347ef9dabe1361d83c647aa8e02b8ac445072246381`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 7.5 MB (7477016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3c7eb9fc67a5dca0fe046d438bfd1c0088ed2c05adaabe66308270c9961976`  
		Last Modified: Wed, 24 Jun 2026 02:27:38 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b965aaf60c1a0e5bf5ad011a45ca72a7c9e85cac56c93a195264f26b6bed2b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299420806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82ec9920098a67359cb225ce4735fb1a330ca59b82a85a3cb36d136463992d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:58:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:58:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:58:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:58:45 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:52:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:52:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:52:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:52:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:52:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb31c7f870ef8ec8aee6455f55c7a957b94017aabba051fbeec8aa80bef9255`  
		Last Modified: Wed, 17 Jun 2026 00:02:33 GMT  
		Size: 158.3 MB (158343224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d5d0235fd16d40608b3186087d69ce25cc2cbbb480e5865b7a5f1882ffdd64`  
		Last Modified: Fri, 19 Jun 2026 02:53:31 GMT  
		Size: 87.9 MB (87938605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92ce4ebae61ccd63ed9b2c04de007b9fd395fc289557d9c182123b9ce73d413`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492a9fae25a8080a352035d00d315acb56c2eca86e98ab94e5dc659472c2c44e`  
		Last Modified: Fri, 19 Jun 2026 02:53:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:de6285dc3fa1bfe085462f69451707d7687a096d723f7def4a0925ca31f54c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735696cbbb6b63f6d55f55510d7a9c64602a3d5b4bf065148c4aadd466db6eaa`

```dockerfile
```

-	Layers:
	-	`sha256:83dbc31bb9bc2c127ec197d6936b24d9aea5377da90168e30f05743090229d69`  
		Last Modified: Fri, 19 Jun 2026 02:53:29 GMT  
		Size: 7.5 MB (7475044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1524369aed5658e95d33eb9a3726b3d9c1c2693d2938595405b368b7c31af379`  
		Last Modified: Fri, 19 Jun 2026 02:53:28 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8198d8beab89323d42362f2f9ed19b6ed387a693731c7d8a8bddf5323cd8eacd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280277559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec49c50d778b982790e3d56b4003852a3f2e342070045117aa53a6930ca7102a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:38:00 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c55ae26073105dbb12b878ce93ae33f8d0835ba25a28114c5d1f6b6e4fbfe51`  
		Last Modified: Tue, 16 Jun 2026 23:39:40 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a365f16057f8f0104e425b38decce4c8868b6eb0ad39712a690895e1432ce5c8`  
		Last Modified: Fri, 19 Jun 2026 02:20:57 GMT  
		Size: 83.5 MB (83502275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a21b1a4208cece9079f3bb95cd2de6e00a4a9dd0298d8d9f8981fa718609a6`  
		Last Modified: Fri, 19 Jun 2026 02:20:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961efa857c9c03a081ad890cabb2dc65d062e97555ab14358cba6555879536a4`  
		Last Modified: Fri, 19 Jun 2026 02:20:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f065951a1f821a66a0d6f527e2329a6cfaea8d12ecb02c927820225bb4ce38d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fb13d0492f09902fcc13c92af4a42b90d86183436d1b073f4d6d21ec133ebb`

```dockerfile
```

-	Layers:
	-	`sha256:c8709b358ce9100c286796a158163c424e141cc205a342c5c3720d73d281f2fc`  
		Last Modified: Fri, 19 Jun 2026 02:20:56 GMT  
		Size: 7.5 MB (7466545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c0992c91d8646f8a220765f1e142ae0b095541856a6ad0a2a76901fe31ed5b2`  
		Last Modified: Fri, 19 Jun 2026 02:20:56 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
