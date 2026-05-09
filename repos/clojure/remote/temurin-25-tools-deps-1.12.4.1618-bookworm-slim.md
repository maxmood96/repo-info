## `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:ca0602d5e72c7b7eb6f53cf82f5566a4c2de1a9271e0e72f9faf690de04db254
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:638b980f5b1e89366aea34635b907e935b4fbe5a5b9428ab78437efd9c3c4c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190510986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737e00aa6ad89a6db880265a4f64f719c49f166ce1eac0568a91c023061b437`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:15 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:15 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5171b16c6248e77001e393093a9cd822f4f3ded4f0efe7ebd69d7ca32e78a39`  
		Last Modified: Fri, 08 May 2026 20:19:52 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3628aee67ff7d95ca154003b92f5a9a30b9908bc8147b1432024c22df7f92de6`  
		Last Modified: Fri, 08 May 2026 20:19:51 GMT  
		Size: 69.7 MB (69699071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5ba244d53ea964773d6b936b00d6e9b252d1d222aecb68289cdc262dc5a15c`  
		Last Modified: Fri, 08 May 2026 20:19:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3b9190913da913bbf05e759db248fcda1a3e97e167f1efb7940ecc10c5ad31`  
		Last Modified: Fri, 08 May 2026 20:19:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a820222b0875ed76dce22fab11b03450f33fdd3425c7bb0e0c5c82334b3255ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdec8e75e9a9477466dbf44b5601896ae071cbebb4dfb23eaec8c8a33ede9b1`

```dockerfile
```

-	Layers:
	-	`sha256:e5bb2c9cb3a0607ec139279929bdc4beeace50f8186bd21037f37bb8d76c873d`  
		Last Modified: Fri, 08 May 2026 20:19:48 GMT  
		Size: 5.1 MB (5084884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa813c9c89228b4e37c72ff2ec01df1f0e3dd56184b8d37a5ea047ae24374d64`  
		Last Modified: Fri, 08 May 2026 20:19:48 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87ae064b9754b475d547b34dda0d2c9e17a892a566ce12b687380128c9838403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189352098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b34dd5b735c72cb5ced0c8c9ec974508c1c19258b068a4973a4c45c244b2fdf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:22:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:23:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:23:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31052a2c6c7a34e6b9841ad35dab1dfaa0c49a562e795b25b45ad29662637d1e`  
		Last Modified: Fri, 08 May 2026 20:23:31 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c45e82ec83d7d8f8374b5e5fb6493a9131a6072156df8058f0b9f9fa8169263`  
		Last Modified: Fri, 08 May 2026 20:24:08 GMT  
		Size: 69.7 MB (69692623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1b0f7ef1b3138e1e06132aa33534bab8349ad461d68b5ee515e85dc20506d`  
		Last Modified: Fri, 08 May 2026 20:24:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a877f10f3dbe9b0b7b80a3b86d7abb6b583a1fa7f1df27ff78dbdbbc748e468`  
		Last Modified: Fri, 08 May 2026 20:24:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6aabcd123851b2bc80c06825d551f28065c617448644b80f7a2e530cbffbf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a040cc27c201076437334123dd5ec06cdeaabdfe8cb779456cef3d79c3dbbeb9`

```dockerfile
```

-	Layers:
	-	`sha256:79fe08bdae24a3f2494970457299eb949bfbd17bc88c3901eebfb1797abba1bf`  
		Last Modified: Fri, 08 May 2026 20:24:06 GMT  
		Size: 5.1 MB (5090666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58dab8656c44cca96b575c5d721838399a1cfcadd49f473c4e4182654921a2e4`  
		Last Modified: Fri, 08 May 2026 20:24:06 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1655a0ca5700d8640b9b01d429e2d22c9b97ebf4d67a9f363eeab33890c15518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199523023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03700fc2fe936b1d9a1b5c6612e4d83473ce479e8f118ff945aa6f741e914fef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:43:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:43:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:43:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:47:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:47:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:47:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:47:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:47:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de1619367effbb8009b986da2ea9fbc4fb9ea6adb3d628cb1ec99649f247618`  
		Last Modified: Fri, 08 May 2026 01:45:16 GMT  
		Size: 91.9 MB (91914008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b5037534acb8777b09766551c6cbd39fb6328aae92ebf265485fe20f3b450c`  
		Last Modified: Fri, 08 May 2026 01:47:54 GMT  
		Size: 75.5 MB (75529577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fcda60bf46d033eab9fc328233a32c3c1fe2d67ce1a7b4208cb85b04462ac7`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ece27773f94ea5f988d5e1d2427a2fe821f2a5be4a59552114c15cb7e93f84`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:acf5935cef5128f53dd4f95187c13c7de6789a81546a4dada69deb1277d1b4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5090104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32290085162ab3feee23f8be6432b33e25dc706c89c70021db0dd9760ae3da03`

```dockerfile
```

-	Layers:
	-	`sha256:b8bf4c229e4a95bcbe5560d0f40f321c564a2afdb78eaad458bb17574bf74bc7`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 5.1 MB (5073366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ed4a0649f26725bb2fd3e3cfce891c32a81e38064399f93d559015de4c36e4`  
		Last Modified: Fri, 08 May 2026 01:47:52 GMT  
		Size: 16.7 KB (16738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a364ddd8e82309d9b5c94ffb370af2a3b03be2d12e8b39e31e0b5e859213e616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183825687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2927635e2c3e35dc4bc5f2e0079abf9ae8301a91b51192da02d34c58c7cbc8b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:18:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:18:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:18:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:18:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:20:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:20:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:20:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:20:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:20:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2a98e90054a6c9a3c4e497f6656030195d43c38235d9e7c561af6ea94fc09`  
		Last Modified: Fri, 08 May 2026 22:19:35 GMT  
		Size: 88.4 MB (88420316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a6c0e69e6aedaa35ebb6e2a5cab4859ff44254b5d0944466e12adfa68348c8`  
		Last Modified: Fri, 08 May 2026 22:20:29 GMT  
		Size: 68.5 MB (68512729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0001d697e6602d02dff956ec326d57652e30bd0d067e75bca88fde77a25946a6`  
		Last Modified: Fri, 08 May 2026 22:20:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f570a989b1abc7ebf5871a06cf648d35a6731500fdf5788cdb4ea24e7c95b1a7`  
		Last Modified: Fri, 08 May 2026 22:20:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4aa4b3487c21bba070d5a60cac46bd2808935abe850470e898c5b937bc537dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2671b2a1ea7b9161c204b60dbad66f188d607ee7d466bc9270a23527107823b`

```dockerfile
```

-	Layers:
	-	`sha256:29c3d367b713cd73a6f8d6252cb03506cb504d2e0cb7d4bc2782b6c45890c2e8`  
		Last Modified: Fri, 08 May 2026 22:20:28 GMT  
		Size: 5.1 MB (5060767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fd825891f1a694ec5276f4017d1c799427ce34b478092955f840f9e0a5936fe`  
		Last Modified: Fri, 08 May 2026 22:20:27 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json
