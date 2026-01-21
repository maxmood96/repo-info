## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:2ff06160025560b5bce66923826be887d958f52ab87d6204c068e01085a2e110
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e6451872ef48322c6a8f4047ed02fcfe42a6ca9535391f7d012fec4e1d95ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259594523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c1e7549b4f366755b5dbb5c045ee599f8a41ea1d0a8e071d5ececdd35108a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:02:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:02:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:02:27 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:02:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:02:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:02:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:02:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:02:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a086156f2ef532793f0e3b9bf4c9882738bb14f62c893e15327c7e7c621fe9b6`  
		Last Modified: Fri, 16 Jan 2026 06:59:47 GMT  
		Size: 157.8 MB (157826001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1a79f8a195906bcbf4603d6831e5f3d8a2610b50ed059d10659340de7c1e8d`  
		Last Modified: Fri, 16 Jan 2026 02:03:22 GMT  
		Size: 72.0 MB (71993794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8986b748f6f5b6ced6fbf94dfab7d37ab33fdbafa07b37282d4572477194d546`  
		Last Modified: Fri, 16 Jan 2026 02:03:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2338d019bf6156e62962aec54f93163417af43da0cb6dd25438346fc2c7a42d2`  
		Last Modified: Fri, 16 Jan 2026 02:03:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab8fc65ad222021d6532f97069b7bc588710d75818d51ab11783577c2280768c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431429bc776ea4a0b9f43c78235140256801a5267a3102dfc66e247ebb47a023`

```dockerfile
```

-	Layers:
	-	`sha256:056981b1fa0f5d656c5c589543ce19e4f9e351be2f007be15b9d721684b39c6c`  
		Last Modified: Fri, 16 Jan 2026 04:48:40 GMT  
		Size: 5.3 MB (5259399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1572c1421e2ea4581d133e6019cb8726626325d99e676ac526cb1c5a8fbded9`  
		Last Modified: Fri, 16 Jan 2026 02:03:03 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:11dc34fae77a677d9c156710f37e6049b436e332ecdc34abfd9cc617381368ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258049014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190a83e2ffc8a7217b913c66a72692d10598724a01d64bd19398b6d5757c2784`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:07:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:07:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:07:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:07:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:07:19 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:07:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:07:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:07:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:07:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:07:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbb9d00a375c86c0cb8fa7d2de4c255bf32a256224ba315c2437ce6dd6a8250`  
		Last Modified: Fri, 16 Jan 2026 18:25:45 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724bd16145f8313d279905cae55199c958c45e860879ba09a74c3035ac6e287`  
		Last Modified: Fri, 16 Jan 2026 17:49:34 GMT  
		Size: 71.8 MB (71806295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5bc205f0f69b8f8bd502e1c2348e50d5178b0e7ab1ecbad7a660040a0b34f`  
		Last Modified: Fri, 16 Jan 2026 02:08:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0ab30fc88a937f93ded89afe3a5ea686f44ce55191b4cc6051dd8f3a1c4054`  
		Last Modified: Fri, 16 Jan 2026 02:07:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2242234d28f8b092d6c519ee07e835144da7ea7d4b25db11104e6ebc340cfa65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d6b7c216459093f304d6bfa3a14b9a363f86698fdce35dc5bb98f1ddb3f1f4`

```dockerfile
```

-	Layers:
	-	`sha256:6ae1e2cd3bd50544f4cab8066dafa9fd5818e95744df89a9c0ee7260c1312704`  
		Last Modified: Fri, 16 Jan 2026 02:07:58 GMT  
		Size: 5.3 MB (5265168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ef53e7f5d364948489df270891042efb87948f6be2cd6c4dd2cdfae733cad9`  
		Last Modified: Fri, 16 Jan 2026 04:48:48 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f265b3a2e47161d1201871d9520d8f8e8a98174594c98e6184a76d6595f46bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268929641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855e32c6545bcb8d75891a0b607e661c25773e0a07102f1abbe5f035ccf35692`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:32:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:32:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:32:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:32:35 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:32:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:40:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:40:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:40:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:40:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:40:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb8419d04d870182d92f9dd23172b44a59edb435e25623743b58a1807e6008`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 157.9 MB (157942967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10f235e9ebd92694735d8d9703675ecd6d4fa4d8632ad7bb5eda10f8898b47`  
		Last Modified: Fri, 16 Jan 2026 03:42:00 GMT  
		Size: 77.4 MB (77390031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81d70ab6a80b690419aac3f89a5d37bc0afe20c87d197f85cd1a6f514d3e286`  
		Last Modified: Fri, 16 Jan 2026 03:41:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86869df57bf7b1b6347afe66c4333cd437d025be575e47d22726303c401f56c`  
		Last Modified: Fri, 16 Jan 2026 03:41:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4278603153867c9d31dd24722044896cbd6b3931b03bf13efb5723814f10195a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ffebcd70779d4cacc763d9c558da42bc2dd5800de7eb5ba7dc2d889a161552`

```dockerfile
```

-	Layers:
	-	`sha256:763ab0cfa60e43dc3fc74662dad299057e52e3e64de272f38cef7b2ae1fde8c0`  
		Last Modified: Fri, 16 Jan 2026 04:48:54 GMT  
		Size: 5.3 MB (5263770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3eb2d1c7eb09b9d1f4018bcd036eadf3cc958e302a29344b611e92fb258b05e`  
		Last Modified: Fri, 16 Jan 2026 04:48:54 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:67cd579232b51203a3dc13b303cbe8615108f9c08fd30fcce37235fe31f04664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256346826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6e76c45c6ffb4623aa308d2eb2f7e058c36158f1eed21588323d911d91a44e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:02:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:02:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 07:02:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:19:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:19:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091162d898a2d4e7b50f7bb9588aeb36e7979c2a93097ad0bdcd2473aa01fb84`  
		Last Modified: Thu, 01 Jan 2026 07:09:19 GMT  
		Size: 157.2 MB (157194291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b596bea77b5945f1b112128096634da44c9318253db5c4a5d2e7e3264007b7`  
		Last Modified: Thu, 01 Jan 2026 07:24:11 GMT  
		Size: 70.9 MB (70878363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257729749f6b2bdc6b07d335123d519a150a21ec4fdb22e5857cec4645bac16`  
		Last Modified: Thu, 01 Jan 2026 07:24:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fd48c429a24d9fcabd2d239fc71b9f43db7daf050603101ce83ad55dbf3acf`  
		Last Modified: Thu, 01 Jan 2026 07:23:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb4bb828e91d6f09b34605193fdb1084fba497b4221692e904e76af7b9509fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80f7527c92c3b15b147ca02fb0d7ad7ab326bbe6fd2d318503e5585ad07a4bf`

```dockerfile
```

-	Layers:
	-	`sha256:88233960f8e761e594c8af3dbcbea20f0052acb9d6f2b64a3627a9d7ae7bb413`  
		Last Modified: Thu, 01 Jan 2026 10:37:13 GMT  
		Size: 5.2 MB (5248765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4090cd20b637de4d3b7f8f028f36df46f003c9b0bb4c0826e1836a0dff99b919`  
		Last Modified: Thu, 01 Jan 2026 10:37:14 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8ab75cf63ac72c6327b5eb6bc05580bac309ab878b58d0f9cfb0fe76ecb51d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249856490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbf5b11122b5b363ed7c40a11d39c1e95fd23366c62c54ebf5554c7cd611f4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:21:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:21:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:21:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:21:37 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:21:37 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:21:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:21:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:21:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:21:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:21:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eec9ce3fc2a673e8d96771fffec4be6e6af957571f1997cfa68e9decb51206`  
		Last Modified: Thu, 15 Jan 2026 23:22:23 GMT  
		Size: 147.1 MB (147069859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f604c1ede2cdf045fb5331a23318bb5a514e518f7937a37d54f8353b707898c0`  
		Last Modified: Thu, 15 Jan 2026 23:22:21 GMT  
		Size: 73.0 MB (72952178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcda83c2b6cf32a4aee0bdf58b9b82f9be8f936d52534a6d79e28e4c9986d05`  
		Last Modified: Thu, 15 Jan 2026 23:22:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddb643c5512f61ead33a889c4bf50b678ad2013b95ebfe0263093b152111692`  
		Last Modified: Thu, 15 Jan 2026 23:22:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:afc263d2480e3f27b54be97e7d5157c1b3774dea79edd6c39e7b22b116b9e62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0630ef53462a49cb63684705dd18fb3332d2141ddae2a06b5b8229b229426dd2`

```dockerfile
```

-	Layers:
	-	`sha256:30c1cde8d5b58854dc93534014cf2a0e2a65a748d204a6839fce85ed7a97a612`  
		Last Modified: Fri, 16 Jan 2026 01:43:18 GMT  
		Size: 5.3 MB (5255323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ef180e097289f9c75a5ff4be6133ab0ffb9a8ede0210ace3c87218f50347e0`  
		Last Modified: Fri, 16 Jan 2026 01:43:19 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
