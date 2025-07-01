## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:441cec2055ebcfdf5b49b3a9221c5b331e81d29c768980f65b6a0f199e34680d
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:fe8beacf8cbf2724ced3ecdf163f1889172e5adb6192bb64663005493841fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274123404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e772f4dcc3a66a8eaff6488f0e9db151476ec3f522af096b3a0a850b03e551`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a116818255357b7dd3d76ded595d163278d5ddf2f47dfbadb60968edcfac93ed`  
		Last Modified: Tue, 01 Jul 2025 06:41:29 GMT  
		Size: 144.6 MB (144635030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebad7ab3e15f8c9c8fe6607887309a47fe180b81ec8b287d6a9188b4e0de205`  
		Last Modified: Tue, 01 Jul 2025 02:39:47 GMT  
		Size: 81.0 MB (80993051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562307fbaa34e7c0e9a7c52e8330d062242995fc009c0dca4445dc23609b94a5`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c3fb9fa5eaf8fdee7d79c0fdf4fd8d2801ec213051868c8730c94269388753`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:328fed263bd346c4a3d39a8ebdbb9628ea41a55ba4e34a7f987a902e2ff9bc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7384089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fed66bee5ca46be6b81d028911f53551fe9f127e6f38d7c692cb57478732cb`

```dockerfile
```

-	Layers:
	-	`sha256:db4999db796795f9267d7b803dd814cb1bb2cb2ca4929ad00eba6db86852c340`  
		Last Modified: Tue, 01 Jul 2025 06:36:55 GMT  
		Size: 7.4 MB (7368268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30debac2bf5934ae33c12b971e9618140f6f7c57d7f64344bd139219d3a6b293`  
		Last Modified: Tue, 01 Jul 2025 06:36:56 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d03684f183ea2ba9d8e2dcc579feec03bfbbb7dfa9520ab7b1c912dc95cd6969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272701259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38ce7eae363fe19eca97a206ec83a6ec5cf41c7ad8b85507f02a19918c82f9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63bfbd0e8254ebcfeb8c130af328be36cfb0ef9e0e10b1979b6cb2e14c5e410`  
		Last Modified: Wed, 11 Jun 2025 11:47:34 GMT  
		Size: 143.5 MB (143512635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1493a0093f3f93740462f87cb3aafdc87598ee07a95ce280025c8443b5c208f1`  
		Last Modified: Wed, 11 Jun 2025 08:29:57 GMT  
		Size: 80.8 MB (80848732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b5a12a3d8cad316071eb338b43f1d958582d4c435afcc84e7a5a017e30999a`  
		Last Modified: Wed, 11 Jun 2025 08:29:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5274e712a07035c378ac815fbcb869de87f632f394a1cfa197253c72d28eff`  
		Last Modified: Wed, 11 Jun 2025 08:29:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:109a76931bff1db78761096d620125b623d67adefb1110b1aa03a11421c3e4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0287691cff8a5412feecbc1596054fa12458bc620a084cf86b29745d6da039c`

```dockerfile
```

-	Layers:
	-	`sha256:8edbc43bdf505bd5ae6faccd7eaee2e104fe5a6cbb7a2efb8c6f151323132e03`  
		Last Modified: Wed, 11 Jun 2025 09:37:19 GMT  
		Size: 7.4 MB (7372675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3df1b66b9740b1bc321d27b56f637491d4bfc2d567e523fdfb8d3acaef7cad`  
		Last Modified: Wed, 11 Jun 2025 09:37:20 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ca6edd601338825e625e5d3e77532e74d126dec616f05c359dc3082b73f0744e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283438548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39df04465132a0dc3776c1fa77fafb00c926d27bc8ea25f8f1834b3f54850f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0ea4b882af434d42baa78fc13182c3a0199b5d594cadfa32f9327ef20526df`  
		Last Modified: Tue, 01 Jul 2025 13:31:29 GMT  
		Size: 144.3 MB (144280581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284618a6436e8bbd703c261050d98b9e81d1665747803d3262165edb7351f522`  
		Last Modified: Tue, 01 Jul 2025 13:31:50 GMT  
		Size: 86.8 MB (86819683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0843a9d902868ec208cd0c2603362a1806b220f0ee743aaf3400c88053e5f114`  
		Last Modified: Tue, 01 Jul 2025 08:49:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b120ad3fea26833ba30438c445d6b0e56f7602392103b3a6bc4f330c5ae44d0`  
		Last Modified: Tue, 01 Jul 2025 08:49:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c4c8d71523a81e4ef12c61eb898398dae91dac1281d87b6d0317a6222227132f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f32871ca1efb0f89117bd44701d9fd1ee46b78b212ab9a5a3c74abf58eb133`

```dockerfile
```

-	Layers:
	-	`sha256:cb6b6a8277642841167c138da5697ff8312f93c0c540aa2ff246aecd7f328f71`  
		Last Modified: Tue, 01 Jul 2025 09:37:16 GMT  
		Size: 7.4 MB (7373472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146e6e696da319399471d66238f4b0b1251b03944bd176d349f6678c5f0464a0`  
		Last Modified: Tue, 01 Jul 2025 09:37:17 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a7cad4215f7529fb2ec4084ce355a40c8cd87db43d9653b75e3e0a6f53d469fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261623444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fab161b2d2c63896fc4a58fc06c83d3cd827ddb68c0bfc1b3ac66c51af5c05c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b6103eea7647ec4468d79df7063299de38b8cf13abe06fcd434a70d2ee5c8`  
		Last Modified: Tue, 01 Jul 2025 13:31:28 GMT  
		Size: 134.7 MB (134673550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecb9c88a9641c14bae8e408c1c21b95307e8375db46debc454cb3b71902fae2`  
		Last Modified: Tue, 01 Jul 2025 08:14:32 GMT  
		Size: 79.8 MB (79799569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a482345e587111875f0bcaa071e3445e4b0696a039ce983a71560f642e7c8e0d`  
		Last Modified: Tue, 01 Jul 2025 08:14:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda24dbb65667b42d5c4cf2f74b4c4b8e9f5e5f41223f5c116fcb3ac1c49be2`  
		Last Modified: Tue, 01 Jul 2025 08:14:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e072fbab492e11325014d324d8916895f0c2e899da2b636dfb29097296545e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72ec1f963de6af2bf0fb3145a1a58ae9e6c6387afd0748ac0e748f574eeeac3`

```dockerfile
```

-	Layers:
	-	`sha256:21b78f0c8d83c1edde5ab32749c8e74444a649b24415c2dc268a4b5e2173028a`  
		Last Modified: Tue, 01 Jul 2025 09:37:23 GMT  
		Size: 7.4 MB (7359587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849440634fcf0b105288f74fd17d78603a97d03e9ab923ec21cb2a65a3735838`  
		Last Modified: Tue, 01 Jul 2025 09:37:24 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
