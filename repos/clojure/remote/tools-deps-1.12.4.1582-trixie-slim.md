## `clojure:tools-deps-1.12.4.1582-trixie-slim`

```console
$ docker pull clojure@sha256:5b2a52f2f5fad748ac6ef2fdb9cfa09f8fe035f3e84f8d76f8b07d02bbc1b4f1
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

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:551732c748b34e10ddc9bf26a9c92b35b21efadd66f1717bc56320f042f58e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193813495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d058b11eb22419ed6bef59e8c0801edabf8a2ee7df9c881db0a4bf072e259ed3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:41:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:41:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:41:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:41:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:41:04 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:41:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:41:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:41:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:41:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:41:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8320b953fd4b3414c32fd4f0ec7857b2b17eaad644380e5319b497ffb61610`  
		Last Modified: Tue, 13 Jan 2026 03:41:58 GMT  
		Size: 92.0 MB (92045294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72963bf9be20f1865084e31863b79ea7494230900214ed971697b8eaf773a574`  
		Last Modified: Tue, 13 Jan 2026 03:41:54 GMT  
		Size: 72.0 MB (71993475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2a802aaf555ec628f07e1f7a5e99e8ff83de7c6e7b8e807ccd242a20495cbd`  
		Last Modified: Tue, 13 Jan 2026 03:41:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cab030c17994511bf1be7854835f5edd869f6d664295d30d7b32c2e2381ec4e`  
		Last Modified: Tue, 13 Jan 2026 03:41:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32783403bf6af89940db77753fc33ed1947b938f19ddd3fe4740e975af81d788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb4935d85a3dc7dc1c8fa838197f6422e1ff4d8f97838f26b10d17321ca56c6`

```dockerfile
```

-	Layers:
	-	`sha256:e6f65b23e22efe8d0874605976ff1bf4de1681928cae52d0e5fc117e93819f82`  
		Last Modified: Tue, 13 Jan 2026 07:47:01 GMT  
		Size: 5.2 MB (5207647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6b23ef3300a3f809ed0b06744c536497d205af000d856ea13705aee1310399`  
		Last Modified: Tue, 13 Jan 2026 07:47:02 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65da79ff6900b3662e4ed8569d09fd50bfaf90a758294699e2d3c7b65f46b93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192994060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9630b36281569414b404715efb3c9a01e49e0355e0911724f47a0ac81ffbee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:44:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:44:18 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:44:18 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:44:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:44:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:44:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:44:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:44:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924a41032f752224da75ed75e18a90a4fd215e3569f1d2b64da5cb2179a7e203`  
		Last Modified: Tue, 13 Jan 2026 03:45:22 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f9fcba02bd9c1b66c32b19714abcfea59180f74cc101431108c0502d88a6d8`  
		Last Modified: Tue, 13 Jan 2026 03:45:18 GMT  
		Size: 71.8 MB (71806464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a25a99ac3960f51f87874bfc4f1ad67d56f9cbf1f2c8cc11423f670380ec7b0`  
		Last Modified: Tue, 13 Jan 2026 03:45:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9e9f6a99ec13e8d8cfb142ae0fe722d591f6aba10075613663d60e828fad28`  
		Last Modified: Tue, 13 Jan 2026 03:45:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28b41ccad6fe1ec80ed4a4cc2366937f654030be50331fa50274245bc265b338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9685bc9df5a3a461f3b398b0e51d22cf9ea11e7531a04be15d31cf2a86f9f96`

```dockerfile
```

-	Layers:
	-	`sha256:97ac903f34582e4c05477a969b240324d0baf8d02f9b20297f352d0ec09fdd16`  
		Last Modified: Tue, 13 Jan 2026 07:47:07 GMT  
		Size: 5.2 MB (5213437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11914002f539af4902edb3cf778c07a7d46d25136825675b5791ec07eb85083`  
		Last Modified: Tue, 13 Jan 2026 07:47:08 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:22ab819ac9026159183a3e6b1fdbbc9529320c8a046d189fcb644fc0138066a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202597533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540cd939be8435791da01fbc8a52b9d3662f36bc4e4af566bc54ef4bde8cadec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:50:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:50:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:50:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:50:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:50:42 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:53:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:53:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:53:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:53:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:53:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c0cb0513db188945a72749dd6a780b91b0fa6d24c747bb4737feab787c2e02`  
		Last Modified: Tue, 13 Jan 2026 05:52:32 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15f3b833577f16a999883622f0330a86bbca0bfa337745b1ec1c4782fc26a84`  
		Last Modified: Tue, 13 Jan 2026 05:54:30 GMT  
		Size: 77.4 MB (77390102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0aed4e0b45be83288cd0e19e7375d873a8efd42dc6f53514a2748a058e6e48`  
		Last Modified: Tue, 13 Jan 2026 05:54:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83831770167f9e062feecd847ceb385995957913fc3f1124690d835fde93003b`  
		Last Modified: Tue, 13 Jan 2026 05:54:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:142f78ac845494a662ee7c2e8e398c55c327141946100b971c7c8fb651f1b54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ccd45e6362b5b37c577a7d8d546e5fe7cc1e570902bff0d242a01baf49858d`

```dockerfile
```

-	Layers:
	-	`sha256:e381dc138b54e5095e256973d9352b1335baea6b819367f582e69c30ab4c97c5`  
		Last Modified: Tue, 13 Jan 2026 07:47:17 GMT  
		Size: 5.2 MB (5213328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e698e75c8ed119d80f5f7f078a58101ca7c6667e3cf47c623875548e5cb1a8b`  
		Last Modified: Tue, 13 Jan 2026 07:47:20 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:7b9a6f70c15ce8a0ed77c6a219aa22086c57b158890d7e746382f2d7fa4ecaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189905222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0408e1be2270a55d6fe492399670ac51e64748ff92f37feeebdad4dc3c8c4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:30:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:30:35 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 07:30:35 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:46:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 07:46:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 07:46:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:46:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:46:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a09886da888ac7f39c6c9f60f721941a5a3cc3ed273e4d20352388b50fb5af`  
		Last Modified: Thu, 01 Jan 2026 07:36:11 GMT  
		Size: 90.8 MB (90752859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f29e962c3ce468fee80884f84e0e25b9966874f1edf46a5044c862747b3d5a`  
		Last Modified: Thu, 01 Jan 2026 07:50:10 GMT  
		Size: 70.9 MB (70878193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c6574fdd10ae483ad86633fc5f993b26cd6f419f95b38a57a5c7d4a6b3e97`  
		Last Modified: Thu, 01 Jan 2026 07:50:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39a339f8bfa423ba9852f4e89be072d3605e36655d966442965d034dff36731`  
		Last Modified: Thu, 01 Jan 2026 07:50:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3c744b7d701a10112adce7516fcce9ba5692bb604aa43b819c8889839e5b2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43151399744720c71df19a84ca4474a9f75c19e6d3fc9208fba222b56cb3b6d0`

```dockerfile
```

-	Layers:
	-	`sha256:c685b39c0ddca6613af1b66f9df625a0841732a3a669638c8347ba6d683e571a`  
		Last Modified: Thu, 01 Jan 2026 10:38:09 GMT  
		Size: 5.2 MB (5197022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7d77cf6ecda82afa927324bc17bbcbb52a30a7de577e016161b10a1c71a0be`  
		Last Modified: Thu, 01 Jan 2026 10:38:10 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:97e0503b889ca7c0d624611647950a786d535d32e3021cd33cf556e4e6c64629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190997126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9829fadbba71e6f09b276c43758ba42277bf7989f629f30d8bd02229f2ce1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:38:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 15:38:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 15:38:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 15:38:07 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 15:38:07 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 15:38:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 15:38:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 15:38:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 15:38:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 15:38:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9d0f00d98411b4c6d9ca64f30fef57910377717ef1ec565bf947c6901bbc2`  
		Last Modified: Tue, 13 Jan 2026 15:39:02 GMT  
		Size: 88.2 MB (88210704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5022000bd3caf2238eb8b3dd477cf83ec9025c579db87e9bf2fcb4a6ee07a3db`  
		Last Modified: Tue, 13 Jan 2026 15:39:37 GMT  
		Size: 73.0 MB (72951970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f73b3a826e71d421c76b6b82a20509c617aa37c12c371e5eb63b0c9b176b76`  
		Last Modified: Tue, 13 Jan 2026 15:39:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80232d28f0c54af1ff2fbb8d9f7caefb5ba547a10a58483f39513743863b3560`  
		Last Modified: Tue, 13 Jan 2026 15:39:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7ac13632163f31c7fb6f60cde1b3822606703b42ef7bc2115d6621f158f9bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9866b928b1982a11eccfb925df6542f577b95b1b545a525aee8fd337fa9ca3a0`

```dockerfile
```

-	Layers:
	-	`sha256:17258a5fb4651457c540f1040e6c1604a7141fb0f3cdc43e69ebb9a0e4448b63`  
		Last Modified: Tue, 13 Jan 2026 15:39:19 GMT  
		Size: 5.2 MB (5206119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75267446ae151fac9481429a79972751705ecfc43aedb2018c603cbb9d2f2e92`  
		Last Modified: Tue, 13 Jan 2026 15:39:19 GMT  
		Size: 15.7 KB (15694 bytes)  
		MIME: application/vnd.in-toto+json
