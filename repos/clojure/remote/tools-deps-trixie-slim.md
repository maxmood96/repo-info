## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:31d4ca998981eee08300ac24848926b5562693ff786defc8fe7f0a71076ffdcb
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
$ docker pull clojure@sha256:f84fe83e3f4f3db6aa33a29816cf80e976a2722c86da85d916ee13d14aa5ab70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259561914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9377053c57d8ebb2325b82d42876ce194968a28b3f77b1d16aebc0e8d01d81f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae3db26fe745784fbf14d062b71f2dbb69c06d9901615ba6a0ff2f512e657b0`  
		Last Modified: Tue, 02 Sep 2025 10:21:36 GMT  
		Size: 157.8 MB (157804795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542a530a070052c7996e9d024009b15f8208b52c5530da38358214b1ab9acee`  
		Last Modified: Tue, 02 Sep 2025 01:55:49 GMT  
		Size: 72.0 MB (71982788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a2860ab164a1713d506a73117729ab6799e2d3a606abcb80b13e612e064427`  
		Last Modified: Tue, 02 Sep 2025 01:01:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265f3b2ab7b3229042a524b669d37980866841fdb858564861c2053a1efcb1a9`  
		Last Modified: Tue, 02 Sep 2025 01:01:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b19fcb0016403a48cf89d6bf2ffd44686710c5998c0fdd20e5012ad5b3c6926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b2c820b5c28cf216fb58999e9f7361ea92c34ac87b31511c130d0c27f7d9e7`

```dockerfile
```

-	Layers:
	-	`sha256:6f82df14151c94924bce3d4f3c269b17c31d4d6fd7b0a862bbfcf9049c873ede`  
		Last Modified: Tue, 02 Sep 2025 03:42:34 GMT  
		Size: 5.3 MB (5259027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d189a2cc7e0d9950787cf428d6d9058278e53b492a78a7ca63e47f8df3c03a`  
		Last Modified: Tue, 02 Sep 2025 03:42:35 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:268b409c39a29a0106673fae29d9826af90f54affab1813e9a4798e2ebc83e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258021963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4e6f15e64ec245138d980fa8887d3e640c96d4986351c7e2e909a2ffd336e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1913fa5cb98ce7b837f56ac11f22aa19fdcf84476bb67cc1e33e50912005fc26`  
		Last Modified: Tue, 02 Sep 2025 08:15:10 GMT  
		Size: 156.1 MB (156081199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a784df1e40e515afb199edf1f6f269fde369eea8d5163bb62cbd477be10134`  
		Last Modified: Tue, 02 Sep 2025 08:21:30 GMT  
		Size: 71.8 MB (71803675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a3153332c55048876d884cdd17fe5364242e51246a8bcdc13aa7b4888b27c1`  
		Last Modified: Tue, 02 Sep 2025 08:21:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3916a675c9eba9376c980c207a33f71cf6946eb8570f105d94152547ff624aa`  
		Last Modified: Tue, 02 Sep 2025 08:21:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c75ed8bad1260bc4e04544190ecd55cb985c27382d629bd6334601badcd0209c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e263cb2b5f19ab0217858def5a9d235f471230fa4f658e9c327ed53db2481ff`

```dockerfile
```

-	Layers:
	-	`sha256:4909ea993a56aca90f1c2e3a3dcd2395af9753ab96588e122e310fc027415dcb`  
		Last Modified: Tue, 02 Sep 2025 09:42:05 GMT  
		Size: 5.3 MB (5264820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d894cfb36b27510a4de9d329ad8e9e663f1c7169b9dc06d03e36915fa92f749b`  
		Last Modified: Tue, 02 Sep 2025 09:42:06 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:78a77d0c4ee6b98beb6ac96caeed3f7e4225da0b453805a93daf30ca7e07f305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268947045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293e358ae827ce03f66b2a6271f418f821940b2eba461cb3064ff2cdf95c327a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7c959eacec6c619834131d38c38895328f95714d0440bb50ea7a7da6a19678`  
		Last Modified: Tue, 02 Sep 2025 09:00:02 GMT  
		Size: 158.0 MB (157963453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8bee27bbd321870fa86988cf57bacb2b9c25b394f8a4cd70d314176e4f3466`  
		Last Modified: Tue, 02 Sep 2025 09:09:59 GMT  
		Size: 77.4 MB (77388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c210e2d881b68613c2c6c820dd88b24535297540f692fd547192dc9e9d012376`  
		Last Modified: Tue, 02 Sep 2025 10:02:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae5e401c90f6d13cda5413026fb46a0f94e34bc3374498c39f05483a4ea3105`  
		Last Modified: Tue, 02 Sep 2025 10:02:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01ac8af68dd485965d971e36ba1eea799aba13972c113130fbaed969f01416b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ff188fc6473c45698409e980693a3af6878930432741874390ef70212a9ff4`

```dockerfile
```

-	Layers:
	-	`sha256:e793f3ae6e0ea3d98c4aaa72f854550e7abc9c80ec54c5c7da7f9e54ba5f7607`  
		Last Modified: Tue, 02 Sep 2025 12:36:23 GMT  
		Size: 5.3 MB (5263410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77436a8cd77f41e9a64369630be8d86203b990d1a7721c23a484e4aa3822d0d0`  
		Last Modified: Tue, 02 Sep 2025 12:36:24 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:bce6ff393cd4a25f397cc048cec4e34f4b236c9675c05d13a326c9c4c0f9db99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252741876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50416048f24f4ec5f5a027bff834fcad3ef9e8ee9b133304e374db8e7b62677b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe2da26b449cd4abe7fa8bad995c0e0c0915c353e520affaa5802c88313163e`  
		Last Modified: Sun, 24 Aug 2025 00:17:52 GMT  
		Size: 153.6 MB (153593524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd945d183ce66f94963c2716db5fcdec1acaeae8801b7800d02af80b56b5b43`  
		Last Modified: Wed, 27 Aug 2025 09:34:26 GMT  
		Size: 70.9 MB (70875683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5c009241c410a34b2d1f36a467c002886428412bf244c736d1872095e5540`  
		Last Modified: Wed, 27 Aug 2025 09:34:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0c79cd2589471d20eee484a9e7fba3f43c0ab547a7eeec880da5915bf0314a`  
		Last Modified: Wed, 27 Aug 2025 09:34:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c172a1b373ececb27b90c6dc04b8a96a298cc82a6f26010cd418c811f7be22f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a6d1c39313db805a36406c485bc75d5520cef295fc4b6dd195fdd854f31e7a`

```dockerfile
```

-	Layers:
	-	`sha256:c93edfaf9f3eeace9903d672d71c52ceb0e47eb75beb8ef7fddd9ff223654150`  
		Last Modified: Wed, 27 Aug 2025 12:36:40 GMT  
		Size: 5.2 MB (5248503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae3743f7c0131f2d26533065f7f915cf25d5aa6b83886e0782b9fbaf2be43d2`  
		Last Modified: Wed, 27 Aug 2025 12:36:41 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ba05e2ca7a310727f278c15ca482d19b7c0276d9122f4fdcd7062c0f6736d063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249810587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a414504bcf25eb7903565b0af8b06fd28492d4c6d2a2666ecad345c5612c1908`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e20decd026ec2d813c6f436cf3752ed0782cc0032343faebcd362020c760d06`  
		Last Modified: Tue, 02 Sep 2025 02:14:12 GMT  
		Size: 147.0 MB (147026956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6bf7faa43d61460c1a33d9d30c9dd0b9ed20b73ed4e72db8c3abf347b85ca`  
		Last Modified: Tue, 02 Sep 2025 02:20:21 GMT  
		Size: 72.9 MB (72949533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6bbbbba45068bb76c0d8767d3a34d9c96dcd4d2f0c52b6599a97f465be6616`  
		Last Modified: Tue, 02 Sep 2025 02:20:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce88c269efedd7c95473e79f4e650d3c43a4216303525122bbbf39cacde1cda8`  
		Last Modified: Tue, 02 Sep 2025 02:20:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ad5dcc20c67d47827156e6232f3cb1a6ff58753f200f67fad943491b158a8a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc50aeeb119556a50aa22849d302612a1e28f69367875583aab577386a6ed60`

```dockerfile
```

-	Layers:
	-	`sha256:21f006818f287e9bbff983ce6164fb53cc63f7afb0bfbb0fa3e25b8a07bfbf35`  
		Last Modified: Tue, 02 Sep 2025 03:42:56 GMT  
		Size: 5.3 MB (5254951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b94fbb4672b4615e267bc4d477df733df925b8df4cc03882124539c9cf02e18`  
		Last Modified: Tue, 02 Sep 2025 03:42:57 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
