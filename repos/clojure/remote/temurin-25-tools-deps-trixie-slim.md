## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:620e17ed79003ea5e75ee1ac5c50bca0d551a36f125527c10c51c56b6a20b8a2
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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; amd64

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

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b8877158fb6bf1f469ff5095d1b94e6d6fc0bc10cc6a7f6374753ad220af004e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.9 MB (202941252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdad5745df24bc071d927ff2d7ffa936ae13c061421a1457231088463649ed3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:43:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:43:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:43:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:43:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:43:32 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:46:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:46:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:46:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:46:42 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:46:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac28bbda9cf605f0d239dc381ad9eec484e7e0bec93b2a70b5e743abff1b6d9`  
		Last Modified: Sat, 09 May 2026 02:44:39 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03e91061e63ffca15e96106cf8feb4124f0623859c703afd6be18183e0f2a7`  
		Last Modified: Sat, 09 May 2026 02:47:13 GMT  
		Size: 77.4 MB (77428113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f607c3344c2481710b2a5cd3ae44b76a33b2a0018d39e2242110d01b3e786285`  
		Last Modified: Sat, 09 May 2026 02:47:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55730b8e3bc746784127888229362b88847bcec76b0e8aba5f5f4762737e90d7`  
		Last Modified: Sat, 09 May 2026 02:47:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f96a466ae56d4cf0f283bb1c227436583ab8b30173c26c297069ac5df1d798cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc54cf916e3ff0e4a080e9422212249c1052b82ee3e9fd6467c14a59ab598b01`

```dockerfile
```

-	Layers:
	-	`sha256:23c8b79a412cd86fd6d60d41be0949645a14753bea3e5b5e775a8f1844bb5b44`  
		Last Modified: Sat, 09 May 2026 02:47:11 GMT  
		Size: 5.2 MB (5215596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ab5d1b3e34b77b751d77c4ccd9a0f31f2d0390b31d8a10199e7a42f5231b2a`  
		Last Modified: Sat, 09 May 2026 02:47:11 GMT  
		Size: 16.7 KB (16707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

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

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

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
