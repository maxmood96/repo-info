## `clojure:temurin-25-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:d06d5d7aadbc9dd6c41ff9e507e2393655143867202ffea99c1ea8b9a5a88c42
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6b963e1847fd545746a4caa1c7a56a0be552e5ad354a6244d91d5dfb68a0d6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227448087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0559b35bcc65b5985f6639a223ffd561a677eee47b58e9b1fd58f28545eea06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:19:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:39 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3277349d5d4f24b7371559eb52a2673714f3bf0c2c99486038d455a81a1a9b4c`  
		Last Modified: Fri, 08 May 2026 20:20:17 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db6d0c0f55252f312acdc7f7df11040fcc55f9f52229671760c724c7b7976b0`  
		Last Modified: Fri, 08 May 2026 20:20:16 GMT  
		Size: 85.6 MB (85570129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3dafd2404ba9b006ba8a9fd15787e885c9a71e2fa4f10320285564959711e7`  
		Last Modified: Fri, 08 May 2026 20:20:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1268145e8bb34e061a02ac0e9ad5b5ead614919a2f7e8425925e90f832a76ef1`  
		Last Modified: Fri, 08 May 2026 20:20:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0b554f1375e072ff74bc014736c357ee77608984429d16ee13f0aec7a01300ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2eb068a384b6df495cd8d4f1c3e6080e5789ae142ead97889edc8b41a81528`

```dockerfile
```

-	Layers:
	-	`sha256:a074587a2ab96f1e2b408bfcec68cab4ec0328faf39626eb8399d3a0223c83e5`  
		Last Modified: Fri, 08 May 2026 20:20:11 GMT  
		Size: 7.4 MB (7439410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed05b29a055110cad9ff34a83b52f79ca2145a97f9171eef2d4dc4d532477a5`  
		Last Modified: Fri, 08 May 2026 20:20:10 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86ad02adda84eb1547507098e7b7232485ab8a6eaab2ea48578c7917b9087d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226596112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e934c2f2d7b165dd696e59eb8fccb475ac1364479345b4a08758c0a24c53f4`
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
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8773be6e6cabdfe6158b1baf9349b2be911ea19ddd2ffbc29884441c78353138`  
		Last Modified: Fri, 08 May 2026 20:24:42 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2665d2335243bd8c2ca3905b5c4b7f3926fc974827bd6af4e5151fcdd4aa22`  
		Last Modified: Fri, 08 May 2026 20:24:50 GMT  
		Size: 85.4 MB (85383359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c07ca086e32bb3bb371e52477cad61765ab1799cfe4b94480bddd292aa8b8e`  
		Last Modified: Fri, 08 May 2026 20:24:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa01621dc11d2eed112f9d0bb4ce5129366e31c4691dcaea503b333f61379c2`  
		Last Modified: Fri, 08 May 2026 20:24:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:03aac4290a3be9a22dd190670447fc71d2e4ee9ec1bd0ca1a35124d2ee5306bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f10f5435ffdd8a7ef327dd8d400381d28e6c506f86842a0f71bb7a82857bb4f`

```dockerfile
```

-	Layers:
	-	`sha256:e3804a76e6f720a4038685f38642b27d6fc0c72fa47df829940180cd7adb889e`  
		Last Modified: Fri, 08 May 2026 20:24:41 GMT  
		Size: 7.4 MB (7446461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a72d836c0f2b6dad2e462d5b594bd65e612f1011fbdbc3a8a3f0a303a9096307`  
		Last Modified: Fri, 08 May 2026 20:24:40 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fff126743735f3e030ef44a0f71e5b9aa1bbe08ad63c72b9c6673103fcb8cf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236024336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dc45acc995349f7e03946d16720941c7493d10370da37dad8cdc296cf4ad51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:44:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:44:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:44:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:44:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:48:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:48:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:48:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:48:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:48:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c0840b059b135fa7f7f221d2f316e4eeea1c12b50461d42b38e0a6be805d85`  
		Last Modified: Fri, 08 May 2026 01:45:19 GMT  
		Size: 91.9 MB (91914028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5397dec3296fc6bd3e45ec89950702ed3adff883fe89eca573ec0a1351ca897`  
		Last Modified: Fri, 08 May 2026 01:49:20 GMT  
		Size: 91.0 MB (90986286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083894e9db61acf8567e12b8191f0d09cec27cffaf5cdedc8302a2ecff617efb`  
		Last Modified: Fri, 08 May 2026 01:49:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc77b78d53e140ca0059c72e323c9e223b653457856486c6a6209c12b20e1e4`  
		Last Modified: Fri, 08 May 2026 01:49:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d91d784868fa0d3f2c49db1af756a8febbf3c0707dcb66c86ebf74bf09b3aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb75ef0c86f79d018d5f6bb8aac6bdba6c64482701861457fc0df12e8f7e788d`

```dockerfile
```

-	Layers:
	-	`sha256:7d1757647ff1af93f908ce51cc8071822ab2d781b4352ab198f67880a165e778`  
		Last Modified: Fri, 08 May 2026 01:49:18 GMT  
		Size: 7.4 MB (7427155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c7947180faf1944b751bb423c2c9f7abbdc709448701ba276990fd17461662`  
		Last Modified: Fri, 08 May 2026 01:49:17 GMT  
		Size: 16.6 KB (16627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9a0007e2a153006241a654c4b8ee0c8f88163625680fc7f26f1ef3d13e047ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223274071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934285164367c88eaeb9b8e69b6c785cd8cfe3f852f960064309a5f872e4146c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:11:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:11:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:11:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 01:11:16 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:32:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 01:32:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 01:32:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:32:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:32:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af697d12e7ce2f4ea84af1fb9a0a596fbf93eb7670e91abadfbefd74c762bc67`  
		Last Modified: Fri, 01 May 2026 01:16:52 GMT  
		Size: 91.0 MB (91014936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729740652b4cdbc2e6ee0c940fe6fe37b8ec7989bf2496b18e671869ad050db5`  
		Last Modified: Fri, 01 May 2026 01:36:54 GMT  
		Size: 84.5 MB (84459880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58db505e492a7bb0d48cca60146b61495e9ead3380a725f193a3a4d17d3f432`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e1f66b7ede5991fa02e70eae90c25e30431446b587ea7f4e3275b0607e8f64`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:504a26518932b2148c1bc15b84d3c62114c456887eb6644d891dd497910fee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddfd037d939382667b089d2ba0c82e0bf2e92fc617f4e59ed47dce6c6e1c863`

```dockerfile
```

-	Layers:
	-	`sha256:d8542829608a38f8b3b2340b5acafd7a072fba248a0fb37772a6874d018f47ea`  
		Last Modified: Fri, 01 May 2026 01:36:37 GMT  
		Size: 7.4 MB (7409348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d28545eb03c413f36a2e0b34d5ea5c6809bcd976e29717a20b1c33ad9a48e9`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7328f01b91a50c4b98534d0b0e5a21802727c8506c781489f3965ab2f1116755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224339012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526ef346d1f089b7dfa08b8fc3995bdb7d55f6f33f3ed2584758c0b20e96fced`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:19:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:19:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:19:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:19:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:19:24 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:20:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:20:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:20:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:20:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:20:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471b7103dad7afe52bf3fd88bcc3c26d834f21822aa6fcd3d73af3c901b4545a`  
		Last Modified: Fri, 08 May 2026 22:20:06 GMT  
		Size: 88.4 MB (88420329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deec59993da642a843f7c4d7a56c3a8519357548ddccd97da3bbbae94522b83b`  
		Last Modified: Fri, 08 May 2026 22:21:07 GMT  
		Size: 86.5 MB (86545338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5076f2066542d04b4c429e7facdf0974c4db9d45aac049c2afc3018aaa8fa2e4`  
		Last Modified: Fri, 08 May 2026 22:21:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66baf1b002005b6b68d113bf4e09dd8c9546fc6a3645577729406ef788221f26`  
		Last Modified: Fri, 08 May 2026 22:21:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:83671c467a439df04f9af89960272487c89ff6adb30eb494bbced78716fa2253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fac1a5bfaf7e1f197e5435a0ebf59783714908a91e9e3f450b5284e29d46425`

```dockerfile
```

-	Layers:
	-	`sha256:92a4660782f51f2a5af1c5e7795bc313bd473094eb86ef157f4cae44f80915ac`  
		Last Modified: Fri, 08 May 2026 22:21:05 GMT  
		Size: 7.4 MB (7419894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306faf0cbb556e87a8325715bdd121426f606c4197006d6a3693cbfed4940148`  
		Last Modified: Fri, 08 May 2026 22:21:05 GMT  
		Size: 15.6 KB (15614 bytes)  
		MIME: application/vnd.in-toto+json
