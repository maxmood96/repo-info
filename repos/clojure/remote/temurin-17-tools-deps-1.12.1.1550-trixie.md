## `clojure:temurin-17-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:cd1b529c721993856a09fbca30a2a7016c10285b42d1293609f5eff608add908
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

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1e854d69339376a1f5073a1c33182ba0c847c73206306ae2a4a6c61a75eb8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282089907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f96897a83f73f37d48dab8011158a8bc6689d55988cd22842cf9a477a46083`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e513432e22464bd7da0f7fcd93fdb45bb58bee3d06b2c36bf82260f9706122`  
		Last Modified: Mon, 09 Jun 2025 19:34:41 GMT  
		Size: 144.6 MB (144634949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4a8c26311bf388a240f70cd353266e6b2a863f302b41c9db99b51fe8f471c`  
		Last Modified: Mon, 09 Jun 2025 19:35:32 GMT  
		Size: 88.2 MB (88207009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c00823f4be82f5f959b95855c3f34b95cf01920f03405199dd3ede0882bfbd`  
		Last Modified: Mon, 09 Jun 2025 19:35:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b316b9c213c8f33a5959bc43dbc7e0159d9a7e2a18a91e05c32f87f30f75b556`  
		Last Modified: Mon, 09 Jun 2025 19:35:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:67cdc78880bf8a8c2a504bb1aab31b0eb6c04bb769ccdfe8e45709611ba81e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120206ec7204b4fcaa377493977c0a4f60bb95e4a8b8f4a3b589bd9bbd791047`

```dockerfile
```

-	Layers:
	-	`sha256:68e0a798ecb8455ee429a4f807b5593826b455d4508cdb8b67c94d762f65d34a`  
		Last Modified: Mon, 09 Jun 2025 18:38:19 GMT  
		Size: 7.5 MB (7458635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8a1ad929f49b58414a16db4a8f67e7ee61046abf9045b9d27dc1aa51ccd6dd`  
		Last Modified: Mon, 09 Jun 2025 18:38:20 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04bb6716f76b16bf6841bc9f18efcd9242a45c4342b8f69e04f6809304e3fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281643151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e71c64fd94b15a30ec1563d767712e1d8ea558be3713c879d4d7abd9bd611c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716c0c482281cd83847775856a8d2b5dd899b670a27f613e6c9f63273d5d058`  
		Last Modified: Fri, 06 Jun 2025 12:50:12 GMT  
		Size: 143.5 MB (143512625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b20f106202c77c1226f8e33ccae56ec009989ab360ad9e78cc99a5d4b2a32ee`  
		Last Modified: Mon, 09 Jun 2025 17:50:21 GMT  
		Size: 88.5 MB (88511193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90f199128bc83ec050fbc662c91877c7af5995082fff9033bb3d02413e7e5a`  
		Last Modified: Mon, 09 Jun 2025 17:50:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07d627a61b498b34c942e540c7ab53ec7da5945558446168fa8eb0ef7948db`  
		Last Modified: Mon, 09 Jun 2025 17:50:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fbe14280fc10e3d7659cb15c758eb8e6f74b8519e0976f39e32787fb5acda473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0772b79940a12e59532346638d31b3f42236ae2e98147997bf51f5ebe2a601`

```dockerfile
```

-	Layers:
	-	`sha256:1c4c08c8bede2f4275a8b7478dcd3745eca9d8438e92a90debb20c3e3c4ad55c`  
		Last Modified: Mon, 09 Jun 2025 18:38:29 GMT  
		Size: 7.5 MB (7465665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f684e5a16efac745911be855112a1fc964ea04503a863b79b280fd33cad677c9`  
		Last Modified: Mon, 09 Jun 2025 18:38:30 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d7abb0ab69b5bd1cdad10fb99128a3fd4bcf550168b1125ec0bc7dfdc77accd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291312527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a039f60cd2e78095c23638642ecb0c762d057de32e88a17d6268adf36e630379`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fd7f4fc1007a30b1949050f0ba69932c1032b69ee73e8eb4d85a1f11db273`  
		Last Modified: Tue, 03 Jun 2025 08:51:10 GMT  
		Size: 144.3 MB (144280585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ab73ab8b7bbe5fbff7bca9e0b133e1cecf5700bbb054c0354eff7182b6dd9e`  
		Last Modified: Mon, 09 Jun 2025 18:08:14 GMT  
		Size: 94.0 MB (93950359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2635915ddfeacab2aa4e90fbc53c31fc0912d6160c5b3c1aff1221c16af2ee`  
		Last Modified: Mon, 09 Jun 2025 18:08:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f4ed29a6c6e344d1394ad9638b333645869bac8a92a17c058261abf57be916`  
		Last Modified: Mon, 09 Jun 2025 18:08:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2ad98ea53e53062e61ed208f13734a1564c85a5de41659c90f40e6a6bfd013ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2645e9392c91acb13509a3f2de91c074a894985c9daecacfffb2656495a0d9f3`

```dockerfile
```

-	Layers:
	-	`sha256:81a3ba817b2dd2b48405fc8dc04b1a8864c17e46b172e3625c58847d55bf6619`  
		Last Modified: Mon, 09 Jun 2025 21:36:53 GMT  
		Size: 7.5 MB (7463052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588f54bf5a47145ad368cd81e568311c4462277ef4eaa463e21d6911752900ae`  
		Last Modified: Mon, 09 Jun 2025 21:36:54 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f08faf15bf51b9270e7ca42f585ffa06254bc3125117fcc997a876708fbd26d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273080201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abd0b2d00660ce3db704955e3b9a0fe867da7b683ea9e9468746a9cbfac4151`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
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
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23085f00cc2fab5db834062a7c0906b2e2764d3635d1f0a0795de617ce89767`  
		Last Modified: Tue, 03 Jun 2025 08:54:41 GMT  
		Size: 138.5 MB (138492460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd942a8fe8f2d48901e54143b27da87962b7c856585b2aee408c8d0a74c1ef8`  
		Last Modified: Mon, 09 Jun 2025 18:54:22 GMT  
		Size: 86.9 MB (86855289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ec969b8b28683b4405a88ef175a45784cdec0a5e95e53674119ee479f7c790`  
		Last Modified: Mon, 09 Jun 2025 18:54:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31ce50cb1366a83edb237d928f6656b227e0d0a3e924635fe68ff4ab3084302`  
		Last Modified: Mon, 09 Jun 2025 18:54:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7bd639f2059891f574305977059fb0e195406f760814938bf94212c07204a109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c84582ed14c0ef1ccd544ca3609d909e9bf3677ac0518d99d475b4a449fc82`

```dockerfile
```

-	Layers:
	-	`sha256:fb925713b42c19e4afb0f61c688850e15218c9df3dccdea8ed41db1d6dfb4fb9`  
		Last Modified: Mon, 09 Jun 2025 21:37:00 GMT  
		Size: 7.4 MB (7444627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d02beb58d0af373f236c2970828f127a261407347091693dcb1553358e93252`  
		Last Modified: Mon, 09 Jun 2025 21:37:01 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:18686838ef9c1dfd8e59b78d37e06e42d1ee52412a12e739c63a6b99cf8d703c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.0 MB (272951950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d31e4287ec0d38bbe6110dca27310e65356c4a62ee632a2295b7a2646bf1d80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
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
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3774d10487b032eb1a2167ed2afb6c687158159ce2ed561584cd53595528c`  
		Last Modified: Tue, 03 Jun 2025 06:16:20 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0fe01cf18c236995910a59de61e5ad765572bb044a30f3786e135e0c864268`  
		Last Modified: Mon, 09 Jun 2025 18:50:13 GMT  
		Size: 89.0 MB (88955133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b7362ffc1dc3019deabb5092293dbfaacf0c29975321ca7b7870bb275d4023`  
		Last Modified: Mon, 09 Jun 2025 18:50:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e757c1fa5dc4310b1b68e23dcbb399ede9b15fa8769c0a32c77811ea449243c`  
		Last Modified: Mon, 09 Jun 2025 18:50:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:446b375829e77408f4289620f2cfa55327ecbb628dcd2e9c7bda714ab62f15d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee535542a785478a4796ef682301268c97c9598c2db4932a42da6ab3e591cf6f`

```dockerfile
```

-	Layers:
	-	`sha256:fca2e1b06bcc3005eb1198ac45f92189e3c436da94cebceaba0918dc1ebfa095`  
		Last Modified: Mon, 09 Jun 2025 21:37:07 GMT  
		Size: 7.5 MB (7454557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b640feffba417c110ece286069ae8c2aa81357dd852b3068e82365804230cb1`  
		Last Modified: Mon, 09 Jun 2025 21:37:07 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
