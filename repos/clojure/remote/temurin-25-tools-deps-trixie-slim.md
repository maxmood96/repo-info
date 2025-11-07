## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:85d967e9301d67191de4278929c657e49c992e8d330a7174b79540211671f836
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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9cf281d5c8e258d5a699bca347005e85fa8dcf2758541f773a86418cadb74cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193809885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f0e3cb02e60381a00533a64f6aa79b7a8a9973361d4b4b05c5408043c82c79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:31:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:31:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:31:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:31:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:31:39 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:31:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:31:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ec5297ae368391213c8102a6643375ba96acd3ed2886daa49690b6df1a7e40`  
		Last Modified: Tue, 04 Nov 2025 04:32:35 GMT  
		Size: 92.0 MB (92036036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e26b2aa127e28fa38b888c5729b436ccdab51fe13553f4daead563c9723392c`  
		Last Modified: Tue, 04 Nov 2025 04:32:33 GMT  
		Size: 72.0 MB (71994704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cceb5e108df5588d589275ccee34f336e99dbe16143c5f35d41c8404fdcc24`  
		Last Modified: Tue, 04 Nov 2025 04:32:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69321e50b66478e9259fd6e72a4fab366b37b44e8f96d418efefb0ed499e6ec0`  
		Last Modified: Tue, 04 Nov 2025 04:32:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5cfa9ceaf1fac9cec134041c70e6b2edb522358f884a10336c2054c24622f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a76f53f0e30af6b0285287f7549478e97e992f3767ea4e950870e541d61790b`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ad3235ad2ec788c7de7e92a804b296055c69b83f78d9cf171192f388af71e`  
		Last Modified: Tue, 04 Nov 2025 10:47:02 GMT  
		Size: 5.2 MB (5207505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1789ff34a689945ba641901b7c0fb50316ef6143e013283b7bb2c1e23445f52`  
		Last Modified: Tue, 04 Nov 2025 10:47:03 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ca6f42d3919af14a63c89dfcb5924a4b4a2fc60a3b04c94650ed699f79575d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192997011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bafadbec545338cdc4698f1a7d70e4222c55523e8af307879fc6dd850c3fb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:45:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:45:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:45:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:45:58 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:45:58 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:46:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:46:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:46:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:46:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:46:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f850b42f325a71ec60e8660fe47fc8cc4d658c187f99255f442aa395c70adb6b`  
		Last Modified: Tue, 04 Nov 2025 17:57:02 GMT  
		Size: 91.0 MB (91045235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af5a4ad15a4d18cfd857a3b6d4ef1ab58ef2f2945cc4ec76ddb173eaa52744a`  
		Last Modified: Tue, 04 Nov 2025 01:46:51 GMT  
		Size: 71.8 MB (71808442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18686e354bea60bc717e294299f78abce09a5f9ef66a652ea1096fdc32d1c1b`  
		Last Modified: Tue, 04 Nov 2025 01:46:42 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a781df38693a31484bd33ba605cf0fd7e0b48fa2fdb627b7531a1ad2005c9e9`  
		Last Modified: Tue, 04 Nov 2025 01:46:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bca9e5126f88af6efc526a4cb8496ea667d93d2b806b80a089c0425d505f4761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f8826adcfae5b6c4488d80ad4192e03988516824f896b527509b77aae4eef9`

```dockerfile
```

-	Layers:
	-	`sha256:fc1f416bde11f00a0314a08060e97d63f778fab1fb7b4e94caafdf6ecb063fc5`  
		Last Modified: Tue, 04 Nov 2025 10:47:08 GMT  
		Size: 5.2 MB (5213295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc164d0241a9d5311a4b071523ca474544c61865958b621d008eb043b545f2a`  
		Last Modified: Tue, 04 Nov 2025 10:47:09 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d6e9b725bd36fd9a6f3a28ca081bfeb4b77596d8b0dc22aeddc59ea15ce53ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202598687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6800689145390b40117a16620ea36b6b023787568637422c9bf149c83761a7fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:49:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:49:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:49:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:49:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:49:29 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:56:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:56:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:56:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:56:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:56:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381b92a126244fa7202b2b35fbdb728d2cc6b80af4d981c0cc72c9488e740a18`  
		Last Modified: Tue, 04 Nov 2025 13:51:07 GMT  
		Size: 91.6 MB (91601718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643fd712f2b6059cc59fcef1b3fe9332576fe8cc1a6929c48b7e8b8d07ae55fe`  
		Last Modified: Tue, 04 Nov 2025 13:57:19 GMT  
		Size: 77.4 MB (77397282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db257d42b47a9c762ee83cb129d1380f79c71b1abce372ba0449c4ea24534f3e`  
		Last Modified: Tue, 04 Nov 2025 13:57:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021a56f30e8f36c9ec6aeb93ddd7bfe86fc3f4ef7b10e648e34caf850a841fc7`  
		Last Modified: Tue, 04 Nov 2025 13:57:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c60dfc94a2991aa50bdd9dca25c7ddee65822dc2d8665036b345e2f59edc512b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f3a861fe2f6bbcc111f5048ff3b3f19c08b64a27fa1025116dec96fd8c6c21`

```dockerfile
```

-	Layers:
	-	`sha256:5584c72f0005905b30c7bd4fb9640bd844d26e4615a0c80d02da14ed536aa57a`  
		Last Modified: Tue, 04 Nov 2025 16:40:23 GMT  
		Size: 5.2 MB (5213186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce33f0222e7be5de9279307b6ccaaf30bcb4653e75e86656fb29e4c4902c4b6b`  
		Last Modified: Tue, 04 Nov 2025 16:40:24 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:cf22ab37ce74316b736e0428db6f2c1ac8e34346ac0798338cc3b8e1a263d1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189910123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b264c0f1ef60d9e5abc9ef9f5c36b799f2cf05c4feea8a3a91a88938e266a92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 07:06:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 07:06:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 07:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 07:06:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 07 Nov 2025 07:06:38 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 07:22:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 07 Nov 2025 07:22:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 07 Nov 2025 07:22:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 07:22:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 07:22:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b43db7c4a1d787e387c72aaa92b0496c45b522bc0b3dbb0a44428976e33faeb`  
		Last Modified: Fri, 07 Nov 2025 07:11:59 GMT  
		Size: 90.8 MB (90752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ff6bd85869c3df12b641443cbaabb4a72345071f483be18c11f872abb4f26`  
		Last Modified: Fri, 07 Nov 2025 07:26:39 GMT  
		Size: 70.9 MB (70880888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6de7d72b109a2e58e8d105b7acebf45c71970b410422480298d127488a0e28a`  
		Last Modified: Fri, 07 Nov 2025 07:26:25 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0959160f0913651ea65834499aa476ca21e7f1352335337a91f406380d2792c8`  
		Last Modified: Fri, 07 Nov 2025 07:26:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b12661fb149f0d768f79789c0a7aebe71f8fc1ea5159ad7500459c285e152e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e120387e837cc2a56f2d2d9bd89a212787f8bb783ba6828dd3725a671982be4a`

```dockerfile
```

-	Layers:
	-	`sha256:8263ae64b57b8646a3df97ab71a8d5d3f573eddcfcfc8be6c0dcad290dc7150d`  
		Last Modified: Fri, 07 Nov 2025 10:38:25 GMT  
		Size: 5.2 MB (5196978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef43ec468bff6dcfa4d2b5d0ae798d72ef44e1dbd3fa352d92988227ced07492`  
		Last Modified: Fri, 07 Nov 2025 10:38:25 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:646a1a8517c2d7a9e6943168acbcd3b5182b459ddee604bc9d83a6cad80c7dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190998632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91bc2082302e8ca7d61c4e7d5ff384591782afc97cf4d302a33122f0026f368`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:09:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:09:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:09:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:09:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:09:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:11:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:11:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:11:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:11:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:11:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c4c179cf7ee65cd5ee87d24c970630bc589eb3a014f8015022541b7f8c6ff2`  
		Last Modified: Tue, 04 Nov 2025 13:10:33 GMT  
		Size: 88.2 MB (88206460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82416bd1eb40c134c598770d4d915124db8614926c1a150d845183de2491bec`  
		Last Modified: Tue, 04 Nov 2025 13:12:27 GMT  
		Size: 73.0 MB (72953738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0979d345b7e5c9aed67c3bc8b262e7afd066c81377e8a78db7fc0735c8aa877`  
		Last Modified: Tue, 04 Nov 2025 13:12:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac367681675364cca9c1d9c1fb5eec43f939577772b46c451143d239f575b1b`  
		Last Modified: Tue, 04 Nov 2025 13:12:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ca43390a79ad55e9f3a10e2f5b61e896979d88fb7f4cd9e13440d504204d078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cefaa8bc8fb402dcdd2c774ab8684d3bc6c56741da8dd862f7ff9d6f7d18bd3`

```dockerfile
```

-	Layers:
	-	`sha256:6988bd4b106510ba3e934263aeeead043369c93ad40db790e575261d4f6e8dc4`  
		Last Modified: Tue, 04 Nov 2025 16:40:33 GMT  
		Size: 5.2 MB (5205977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65652072e0e0c2a2d3ff50b23de9658f4ed586a06a5c051601ce7960a4c01f25`  
		Last Modified: Tue, 04 Nov 2025 16:40:34 GMT  
		Size: 15.7 KB (15694 bytes)  
		MIME: application/vnd.in-toto+json
