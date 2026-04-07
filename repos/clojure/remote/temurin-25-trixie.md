## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:2c65f96e1e5e11e4545e8bf45a33d362266fceef39de471eca54690c9af6252b
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

### `clojure:temurin-25-trixie` - linux; amd64

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

### `clojure:temurin-25-trixie` - unknown; unknown

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

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-25-trixie` - unknown; unknown

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

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0b5ab1cc319e6b2439345bf63724e4b26485a6f68923c0612568b7f76b3406dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235739541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2175f3a5e616090bf2c3c39bd33341a314316c3d55dbf15c01c18e3f8ee001`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:45:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:45:54 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:49:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:49:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:49:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:49:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:49:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dcd2e20d0ba59a0ceda7d174daf8edc831e31e2d722a352fbe87f7cac9ae5d`  
		Last Modified: Tue, 17 Mar 2026 18:47:13 GMT  
		Size: 91.6 MB (91632901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff570b5bd4d35345136fe3a7f4b0f92660b5136d7a78252a07add026939c0790`  
		Last Modified: Tue, 17 Mar 2026 18:50:33 GMT  
		Size: 91.0 MB (90987249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a86d804ae81a1f3467f8fce0b9e74d1faa371e19a0a54b4a928141ad416754d`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9646354984498369ef694275cff4ae186e8fb32edd3559d02f37167dbcc709b2`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e18fd0f32d1df0ce441ba38a41a56c6c0ee83e10cd8103eb57e37c9e325b212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfda12ea8f04e798948ab48c1ce437b3568e322d3714de443f99b13665b727f`

```dockerfile
```

-	Layers:
	-	`sha256:1598f5265f1be750d6b7eaa5504fde2e0607f80583ebeb3d78a1ec9421350758`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 7.4 MB (7426478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6360e3f27370fb58635c1577c36a55e16c7b27332cc45063b98fb555c7343a33`  
		Last Modified: Tue, 17 Mar 2026 18:50:30 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:0c45e3379dcf97d01e07855b923a25328232d08123623786c12797a4a8114b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223026063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa8ac674fce7982fa2ea5c31a102c92d3dd41b89feb13799a49db13e761459b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 19:27:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 19:27:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 19:27:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 19:27:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 19:27:57 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:48:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 19:48:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 19:48:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:48:53 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:48:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45c9549b3fd22069333772ff17a0ac1235b4853c85fca137130bf290f6f49b1`  
		Last Modified: Sun, 22 Mar 2026 19:33:35 GMT  
		Size: 90.8 MB (90773420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e249826f4cce91d8a894c38b01ca4d7e16a06e713f44aad175b55e8199c052`  
		Last Modified: Sun, 22 Mar 2026 19:53:06 GMT  
		Size: 84.5 MB (84459274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2e259ca44aea194ade01945666f5052c9c8b89d05631eed129b3d2e495eb74`  
		Last Modified: Sun, 22 Mar 2026 19:52:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0844e62782f30095faa53fcd5116d9583f81d4d4ee31ba5b0771b1db9c9357d9`  
		Last Modified: Sun, 22 Mar 2026 19:52:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0c91829b31f3fea119b02b02bc7857017c2d1ca94a4a347ab0aed15d76429002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591ee5f0edc923842a7a6c73244f919358f4eba786a011e1d2cc195c3de89f8`

```dockerfile
```

-	Layers:
	-	`sha256:0e75635d7d827a9c428da5edf1f1787f0ce7717fee283e30f8679211c53a9093`  
		Last Modified: Sun, 22 Mar 2026 19:52:55 GMT  
		Size: 7.4 MB (7408671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c4500d5d2bebb0e29e3eb95d9abdb33015431d32b9161ad5c38757e0ee22d1`  
		Last Modified: Sun, 22 Mar 2026 19:52:52 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

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

### `clojure:temurin-25-trixie` - unknown; unknown

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
