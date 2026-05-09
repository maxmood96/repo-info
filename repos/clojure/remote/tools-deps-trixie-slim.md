## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:a3bd85a282713a20aa795168c571b9f1227d355f8e7f5e649f371f94c4c15d36
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c930e24dfa72cc66c9d4afdb160f84dd9bd21adbbad10465c7b1d3e4107e0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194367315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d39adb948f408af89077f588435a2196e7a9562bb1cad7e2427be71bc5e26b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 19:42:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 19:42:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:42:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:07 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c932e6872b37fb626b9c05f0eddc412f9c275d7aa4f870bb5f174f0aaae9873`  
		Last Modified: Fri, 08 May 2026 19:43:20 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdce43d9ded5afcc94c10164442f451be7cea4820138ce8b35d5e2c1eeee834`  
		Last Modified: Fri, 08 May 2026 20:20:12 GMT  
		Size: 72.0 MB (72011448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ed9bac6eab8ed27aa22638687500b641cdf4a68a7373a5687e2f248bb2040`  
		Last Modified: Fri, 08 May 2026 20:20:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268fdca2d36d60660d77a434b4eec8a3219a2508585541ae0d9b7faf273617dd`  
		Last Modified: Fri, 08 May 2026 20:20:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d4a8eedcb82c222a707a96a40fe03741f24c4c9d1ab4426cb6be511532d299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7132489f32115e44b0582c83583244b24db071e92ba1ab4bd1dfb8d33a3bd2fd`

```dockerfile
```

-	Layers:
	-	`sha256:624e6b12a329eb5e29e4ae704ec811d9e4098dbdb119fe7c473a4acc40cf0764`  
		Last Modified: Fri, 08 May 2026 20:20:10 GMT  
		Size: 5.2 MB (5227901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59928a418107e6bd5e3f2a0d9c4f6785e4b1dc62c8677a30eaabaf274efae48`  
		Last Modified: Fri, 08 May 2026 20:20:10 GMT  
		Size: 15.7 KB (15693 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46a0b8914979d13a1d9218fabc3867824bdb697c0c2388311c4ff0c52841f112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193518410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6140abf5fa36a057d409631cb7c3569cd809a7a91f140693768fcd495cfb3463`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:24:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:24:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:24:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:24:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8773be6e6cabdfe6158b1baf9349b2be911ea19ddd2ffbc29884441c78353138`  
		Last Modified: Fri, 08 May 2026 20:24:42 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2859f2d6300a40835e4cef9490a5306d9d5ebe0a7379c22abe27a81f66138a66`  
		Last Modified: Fri, 08 May 2026 20:24:42 GMT  
		Size: 71.8 MB (71831460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c07ca086e32bb3bb371e52477cad61765ab1799cfe4b94480bddd292aa8b8e`  
		Last Modified: Fri, 08 May 2026 20:24:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa01621dc11d2eed112f9d0bb4ce5129366e31c4691dcaea503b333f61379c2`  
		Last Modified: Fri, 08 May 2026 20:24:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77fa0a265adbdc5da6c5054c3328431fc2a102ade02302637ffbe0bf3308faba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63207cde348dd3cd34995610cb4c31d4ebf80551140080f2cb02dce145616d0e`

```dockerfile
```

-	Layers:
	-	`sha256:a562afb6341c3b9b114ed1d743fcc9635ac3b74f120670cc06831f16bfd2c28a`  
		Last Modified: Fri, 08 May 2026 20:24:39 GMT  
		Size: 5.2 MB (5233691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4ed8fff546c9eb9016e339a83f2aa25628d958ad9f88006fcc0546dae634fe5`  
		Last Modified: Fri, 08 May 2026 20:24:39 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6ddca13275531b5a558b048cd887ce749fbe6e14d297ea5c69ca0aa042755744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202942056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbcf211994da88f2edea834a73c1e59a2e8e410900393edfde86a90c15d2363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:45:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:45:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:45:30 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:45:30 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:50:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:50:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:50:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:50:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:50:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50e227b32fab760ab734a722d523335c702357014ac0ce34693e4421965f3b9`  
		Last Modified: Fri, 08 May 2026 01:49:25 GMT  
		Size: 91.9 MB (91914037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b073b09e7c941cf14ee3cad0b02823b3f28209dc3d93108b91944e272aa1021c`  
		Last Modified: Fri, 08 May 2026 01:50:45 GMT  
		Size: 77.4 MB (77428947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e2125a0d36edaab906cb22c591dd50c82fa5558013f231c537dfd0b4c2cb26`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f241b78d96c9fe2e639e41ec9048e954c3f79519ee9915bd04238fd564ed1d33`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cedead179625d1415dee750f3b63275b4d148f02f4c90c357c5a9dbfa3de7bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a4b66b5cf6178eaa07208d97a383db7de8418e38d7aeb88cdb9296bf2899fe`

```dockerfile
```

-	Layers:
	-	`sha256:07b3cd3b41c80cfbc9e3271549197b57e2dd2678bc4d36ed696556d279aba8f8`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 5.2 MB (5215596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a111d1f27ef0cc694f7e15a48afdb8ba30460431030f025203187495dd29df13`  
		Last Modified: Fri, 08 May 2026 01:50:42 GMT  
		Size: 16.7 KB (16706 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:be89d0af9b54d14061ba4963cf632c0abdeebf260743bbc63cf55dc9852cfa3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190196910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa21e97ea281844cdcea1fbc02f616d0e17dcda82be06e225d98d1fcc0e91bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:17:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 01:17:25 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:40:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 01:40:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 01:40:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:40:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:40:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a463537893b115e8f6bf5847dfb28b93d1015ffeaba8f0acf52e10133dfcf3`  
		Last Modified: Fri, 01 May 2026 01:22:48 GMT  
		Size: 91.0 MB (91014937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189637ec0b992e6712b62b6fb4f7b70346d8d5bcb3ee094fd4aab889fff4c37f`  
		Last Modified: Fri, 01 May 2026 01:43:39 GMT  
		Size: 70.9 MB (70900737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79eaea740b68965c8fdc3649064b2c913832c335f630b9ba2a8384fb8106320d`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e977049073a11f7f44c386d34f63afc5a55ee22fb7bc04268acd8cc3aca264`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e91e0fd693ca996b99de0cbe7c0cd9858b0a648a250235e9c08fd4549071b198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6965907ae999b8e0337c662e8c9772925e92bfc1a659806cc6fa700e443fec`

```dockerfile
```

-	Layers:
	-	`sha256:cbd087a5706682fae7db02ce8143c7d1f9e49a1a746c6749c8ab1d763063d0f0`  
		Last Modified: Fri, 01 May 2026 01:43:29 GMT  
		Size: 5.2 MB (5199388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b976013de3d9592c571721b84f129ce8eee150012ccf55a24491e0511d7c0ff9`  
		Last Modified: Fri, 01 May 2026 01:43:28 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a0ec7e1c87ae76b9921a0445cae70d8b6cf781ea453e7c34481f7f18d6549c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191248657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dd1426ef6cdfb7c7055e40b32d4c6e9ba81ff4a63b29d7183c7c82e958dec1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:19:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:19:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:19:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:19:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:20:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:20:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:20:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:20:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:20:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e938f267ce0fd10a0af51ad69cff5393dd662d7cd6252b86c266d7de2c2375c`  
		Last Modified: Fri, 08 May 2026 22:20:26 GMT  
		Size: 88.4 MB (88420315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9536b8a935fb93920339b24d8e21eaa1e1c05624478049b22afea46cf9306dfa`  
		Last Modified: Fri, 08 May 2026 22:21:22 GMT  
		Size: 73.0 MB (72986953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1177eff728d50983019f6ff6cd0dbd7814d169f823b92c647676b9806eb7a41d`  
		Last Modified: Fri, 08 May 2026 22:21:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196063274951bf2b00db81b2e785bde1f4142ae20c2c00c51c2519ac28730d87`  
		Last Modified: Fri, 08 May 2026 22:21:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7414868b36c2e02821fde4955b925a62a0ce900473cf4ea70be648bb5513593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13365f4f44db6b045d0b05ee4e230132f6f90b517047bd8da78570256c5d495a`

```dockerfile
```

-	Layers:
	-	`sha256:966d354646d14444e58ac001f8f1c48a05a9f2dd746c1f8ad78363948ead10be`  
		Last Modified: Fri, 08 May 2026 22:21:21 GMT  
		Size: 5.2 MB (5208387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b46187e2f1fcdb3673e2a5c5d99fe49fa776cb97166eacb36a020be866f2d527`  
		Last Modified: Fri, 08 May 2026 22:21:20 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
