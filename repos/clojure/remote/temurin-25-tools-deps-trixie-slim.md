## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:3bb683c911593bccdf1ce886055f66212a8519d4bfc1e48ed8e9c78b73a65c86
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
		Last Modified: Tue, 04 Nov 2025 01:46:37 GMT  
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
$ docker pull clojure@sha256:08914256cfd1dbf2626eb3d93a29be066cf9e8a6c34165725f0a480899362f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202595406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58cebb9282c344bb09e246a0e13a135477807903f9244033c8e50652faff151`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673d315aed8718d3c9a70f343a38b3eaf84c29764337879eea3fcbfeccc112a2`  
		Last Modified: Tue, 21 Oct 2025 16:21:40 GMT  
		Size: 91.6 MB (91601696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db47e5443dffcad53e863401182e3a1e1c119f9403c542ffb57118a18931ff4b`  
		Last Modified: Tue, 21 Oct 2025 16:28:58 GMT  
		Size: 77.4 MB (77394152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36ecda0d65946ce30e3772af6337323fe50e82e055257b430ae77f1d23d9e6`  
		Last Modified: Tue, 21 Oct 2025 16:28:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940734b0e9409244da0825349969fe52698b7a77b2076407798db1ae8c315724`  
		Last Modified: Tue, 21 Oct 2025 16:28:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35bc2e7f1defb2b15ab2a76f9e65b63dc514baa26fc3e1163565fa152a900bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8652b24ff765791563d7c6af09ebd5b97b0055132a9866b10ab278eaee71e98d`

```dockerfile
```

-	Layers:
	-	`sha256:4eef40ed6e07086544cbf2998cebc6410e8e4e6272a9bf9fa77b1b0740db8b45`  
		Last Modified: Tue, 21 Oct 2025 18:41:32 GMT  
		Size: 5.2 MB (5213186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc089c8e43149ca55bf1ed6aa19d7faa88aed276cbab762df706cdcd9b66026`  
		Last Modified: Tue, 21 Oct 2025 18:41:33 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:ca2c1be36e40ac23c06402ef7564e034908148d35dc5a1c683def65eadaecf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189909898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d943413c46be3342c38ae76db67bce7c8d4dc9bcacbbcf1c63dbde18d75a5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53fc93bda80dae073528732bad9e8e1acb822c43439b51f960edb79889a4e7b`  
		Last Modified: Fri, 24 Oct 2025 04:09:46 GMT  
		Size: 90.8 MB (90752383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62914483b431d360c4a666a4bc27198127adc3c059249e1f8acdde83b6758aeb`  
		Last Modified: Fri, 24 Oct 2025 04:47:27 GMT  
		Size: 70.9 MB (70880821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639109eab78c8d4cb1050ed5218b64220ed05bdf6e3aa909d48ae6f1a2788da5`  
		Last Modified: Fri, 24 Oct 2025 04:47:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ef14db00eccbebef54d2f5eae27b67389e5f9de0b140fc24e69a6b193636b2`  
		Last Modified: Fri, 24 Oct 2025 04:47:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd442ea4887a9f7830d048468a3dda5f43239d4380660adf6ede8c0d257c49d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2789179032dbc3420494b92e6c959f1a8fb3737b49ff6f215d6a88a03d0271f4`

```dockerfile
```

-	Layers:
	-	`sha256:ee4f3c89b776d691cda40c369af4b09be5d1df825c79cee41cc5a89dd38e2541`  
		Last Modified: Fri, 24 Oct 2025 06:37:41 GMT  
		Size: 5.2 MB (5196978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dd081c002c1d723379dc14d89e8cfa8dd67ffe1b45df8963885871283a7eafe`  
		Last Modified: Fri, 24 Oct 2025 06:37:42 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:33a4dc9b7c97797793862a1607edb20e13b9b660395076b039cca42f77b899ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190998182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1527b5f05ca0006996d308a72f6dd06d706b96f84bb8c7cc9e715587b1f754`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29722a94c5326270eeba3670d3d5df4e7037067570c7bfae78a5379a8a598fd1`  
		Last Modified: Tue, 21 Oct 2025 22:44:56 GMT  
		Size: 88.2 MB (88206399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe37c950714791ee06c1390847a6fe128cef11316cb96a5e0fe39483055f1bbf`  
		Last Modified: Tue, 21 Oct 2025 22:49:28 GMT  
		Size: 73.0 MB (72953485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76169bb5b949a6c3dc0c33af9825ad5dad8bad22d6939e3bc1ed2eb5b290a156`  
		Last Modified: Tue, 21 Oct 2025 22:49:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3312ce13b7c6a9655b9f315af1ebfe5047e31bd1829537200d5b69079b57cb9`  
		Last Modified: Tue, 21 Oct 2025 22:49:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e74c940923f6d7a6ca6b9e1ce7150ea17658c320bb8e082e1393278a8907742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0fd367f39ad55d28725c3e0e149a21d7509517de68c18a6ccd6408d603f733`

```dockerfile
```

-	Layers:
	-	`sha256:f5f49008ddaf2a1f7d300135b40f2eb237fb78a7e483b6f764f08fffadde8abe`  
		Last Modified: Wed, 22 Oct 2025 00:41:24 GMT  
		Size: 5.2 MB (5205977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ee1d1e5593df43ea59ff318bab15ecf71df80847a471d9e0fcd9a988e5675b`  
		Last Modified: Wed, 22 Oct 2025 00:41:25 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json
