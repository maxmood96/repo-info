## `clojure:tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:bb8ed068ef8c0848dce30ffce8cc2237f5d36ab3fb620967631a3aa9acef3222
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

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:be87e18fb2234b9cd2a557d729c3a07e1937a1256bfeefa49eb605559b53325b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227122701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019ae97b61f625d7e28f6b3b51ac2b7831b3e9ba5ef9411f84c09be1d1860ab3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:17:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:17:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:17:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:17:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:17:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:17:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:17:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:17:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:17:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cab201b381678406620a5f34284702d5185cd9d009db7052e221436520e299`  
		Last Modified: Tue, 07 Apr 2026 03:18:05 GMT  
		Size: 92.3 MB (92256277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00752ad52b379330676bef0f66ced0afaa22dba7f4eab8c0ba860bff98a0194e`  
		Last Modified: Tue, 07 Apr 2026 03:18:05 GMT  
		Size: 85.6 MB (85567549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b67af15c423d23c51d7ef8aa92d1a26d656fca503fb44ecfaf28a7bf3f36d8`  
		Last Modified: Tue, 07 Apr 2026 03:18:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f86da90b661bb1185dcd27c572bdf65e100eb6cb9681b77240a4a39228f600b`  
		Last Modified: Tue, 07 Apr 2026 03:18:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b88f2b01ec3867de1dba04b2483e740f25fbe845122e2b159201882570cf752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae797b52aa8971149d8d62de38556122f6a21d50e3b1663b050fc489d9ee7a`

```dockerfile
```

-	Layers:
	-	`sha256:5214da9cf850a0ec0e86cbf92b760bb8e323750abfe281bcd9084d4b9ef98d11`  
		Last Modified: Tue, 07 Apr 2026 03:18:02 GMT  
		Size: 7.4 MB (7438733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d22e7f3b2b50f8488b05c03a14cf069df3b7d620ea418dc7c543dc59265abb1`  
		Last Modified: Tue, 07 Apr 2026 03:18:02 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:29fadeadf78cccf4be9d76031b9f8c5ff248fed529559d9d3aacaed9a2871952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6990e0b8e7989e5862271419555d42003592e10c6900f653683fc6953494728b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:28:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:28:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:28:25 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:28:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:28:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a6ba5a33a04535868c1726e18e5910dde1dd67e7126d8ffbbce864a72c4cb4`  
		Last Modified: Tue, 07 Apr 2026 03:29:08 GMT  
		Size: 91.3 MB (91288266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ff1f6ca70a157b065f8e152ba5dcd1f431179091aca86c5da5290f88f2e61b`  
		Last Modified: Tue, 07 Apr 2026 03:29:09 GMT  
		Size: 85.4 MB (85382709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2879c53014e8e954767b9f62b59bfe464e18d48ba73e705bfab4b6f4c4ec6f8`  
		Last Modified: Tue, 07 Apr 2026 03:29:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4346340cec474398420fa84746bd67197298d649e28d2e92c4f8e16d331f00`  
		Last Modified: Tue, 07 Apr 2026 03:29:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9efa8bd9aef6a16a4ebb77579f4e3ed5ccb8f51579b5a22d4a565383634a7f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31cbf1cf86b1c01bd124b3a2b5dc863b8015420d2931019f219fe46793adf82`

```dockerfile
```

-	Layers:
	-	`sha256:6c4128e4702fe802b13e977799632f7e5dfdacaad14c785acf1cd77438989c33`  
		Last Modified: Tue, 07 Apr 2026 03:29:06 GMT  
		Size: 7.4 MB (7445784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4bbfaba5c60f9f0df21a951da837b1aa381c6c2060ccfb8a99026f23b4d798f`  
		Last Modified: Tue, 07 Apr 2026 03:29:05 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:284113d8cecdff9b9f36cc4c090c82a2b416fa5cb5c2b2e734e4bdd02f83fedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235739991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162aad16a10dab13dbbb53531d8b4b9898207db63bf0197bc31fa6b02ceb2bac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:55:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:55:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:55:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:55:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:55:46 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 15:04:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 15:04:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 15:04:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 15:04:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 15:04:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3326c6b4216bde98266a981f1f1fb92f86315b90e8c006d1aadb7310dd7d4f`  
		Last Modified: Tue, 07 Apr 2026 14:57:06 GMT  
		Size: 91.6 MB (91633006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb297b032dfbdeb3c71ea9d2dc209fbbc469cdf31a3c9f11decb23d0f38a671`  
		Last Modified: Tue, 07 Apr 2026 15:05:12 GMT  
		Size: 91.0 MB (90987273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bcfe38a127579e120e912c7146e457f3b072e45a9b8699159351a310759133`  
		Last Modified: Tue, 07 Apr 2026 15:05:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79cccbea034fa0947657f53f6e9666e8ef54770e0a8d2364b14a12a469d3ebf`  
		Last Modified: Tue, 07 Apr 2026 15:05:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f8ddd21e329dd7e3f5631c4d6774b56792d78b9f6af9c10012919d210703347b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a55b771e66e55a98c3442759b3ed1f38d4ab6635ad4b1a85ecff708ba9763d6`

```dockerfile
```

-	Layers:
	-	`sha256:953ed0f4c89e490b2be62f82db9d7d6c722833e1366e033c8104b47ae61ab552`  
		Last Modified: Tue, 07 Apr 2026 15:05:08 GMT  
		Size: 7.4 MB (7426478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bd9ac14591aeec452de78312dbed2164ae4505cfd4228c41f88c8442821551`  
		Last Modified: Tue, 07 Apr 2026 15:05:07 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:16dbcdb256413a0e35cddc00473b20f60a9c3555fdce77de5cfca4d78bec0dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226198230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef6207eb289ace11a770ff9d79caa4503c13ed1a1abe3624ca7958a26ab933b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:33:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:33:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:33:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:33:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 22:33:17 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 22:54:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 11 Apr 2026 22:54:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 22:54:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 22:54:17 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 22:54:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7224fd307fae2068f62ccce22d637a96c5204dea7af1d7b9116b5323460f86`  
		Last Modified: Sat, 11 Apr 2026 22:38:56 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3061d79d45d13e849fd2ba3d8ab81672b612b18beaf1453e73b0ab68dac30dc4`  
		Last Modified: Sat, 11 Apr 2026 22:58:38 GMT  
		Size: 87.6 MB (87631137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33af8cf7a012e5ccbf87239213a81cd18b3f824ebb5772486644af6eea4e649`  
		Last Modified: Sat, 11 Apr 2026 22:58:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9663454fc9d4992ab2a2c751f0b39ac78c1043d8fc2ad56f5c7cb6028670f21`  
		Last Modified: Sat, 11 Apr 2026 22:58:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bdaedcca0a7e71b1bc43c7840e91c9aecab907e8884f9af490680a7be372e119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2913771287854d7206b72e3570db354a0deab66c82d49ea1c2116b3c9a19667`

```dockerfile
```

-	Layers:
	-	`sha256:7dd33f10146989f0312c5678428192b3304ce2d1bf0ab6d2f0540fa82e5bb40f`  
		Last Modified: Sat, 11 Apr 2026 22:58:26 GMT  
		Size: 7.4 MB (7408671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9208211d8cc8b0c3f4cbd3aea9b26a554218a4814f474912114213a8cc51283e`  
		Last Modified: Sat, 11 Apr 2026 22:58:24 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4181fa1c20aa9183da634d89a88fc1282a1b6bd86923b11a33e0dee2c721aace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224144332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0868f61fd7c35ee944b96779965b97cc8e6ccaec7b244c42d6718740e02444bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:48:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:48:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:48:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:48:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:48:29 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:48:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:48:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:48:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:48:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:48:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050ec66516d617b0d16f07f94b76f55aee1ad77012aa835c8c93893944d4ffde`  
		Last Modified: Tue, 07 Apr 2026 05:49:14 GMT  
		Size: 88.2 MB (88233804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909d77a989c0a69d0cd721e306f83adb551defae531f1d017f7998b95de0ebe5`  
		Last Modified: Tue, 07 Apr 2026 05:49:15 GMT  
		Size: 86.5 MB (86544382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b3051c13be805e63aee5c1ace44458227deccd42fd3a464f4f5a290c7f4bb7`  
		Last Modified: Tue, 07 Apr 2026 05:49:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a00fd040e88e1cbb55ef407cc58aed825d71f9610eb5e3e587476d9dac9b266`  
		Last Modified: Tue, 07 Apr 2026 05:49:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0b7a9f10df0cdeb385a79381f823576ef0f72b05e78612e317c7f6002e02606c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a35dd34911aef277c5c77b8ec01d003cfebe877cbced69add79f2f2e00cd131`

```dockerfile
```

-	Layers:
	-	`sha256:f19d10a48d4d40a5545ed3515d214386cf6369a996a8697ff5609aabfb2e3840`  
		Last Modified: Tue, 07 Apr 2026 05:49:12 GMT  
		Size: 7.4 MB (7419217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c5bdecfb89374ea110b64bec471a8279589de14ba86e171a8541cb0eca65b52`  
		Last Modified: Tue, 07 Apr 2026 05:49:12 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
