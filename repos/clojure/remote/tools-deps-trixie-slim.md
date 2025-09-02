## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:30d9c1f0b2e937a87e7c1fbd8232e1dd4f7cff8be48264e91c76a8b2b93a5801
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
		Last Modified: Tue, 02 Sep 2025 00:18:19 GMT  
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
$ docker pull clojure@sha256:5f1313ef42649cd840de664e0bd7d102080393cf94ed0d575a36c8f3c3ecc1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258022084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c43617bf712fe9a3033c5d83057a3feb001dd6a593c2c16c14ba70f4c68f19`
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
	-	`sha256:56a56322ce1b94f29786d8f76971f53596ba74b5abd690c1219b73a7ffedee07`  
		Last Modified: Tue, 19 Aug 2025 01:33:36 GMT  
		Size: 156.1 MB (156081245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96714c8480f45f0a7caf3f9e4ca5b41099b96e7a6e1495cec71886a2af508f7c`  
		Last Modified: Tue, 26 Aug 2025 17:53:19 GMT  
		Size: 71.8 MB (71803752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11abcd13d4dae1aa6e6dd6e760c06ee1b24571966266ab0eaf68cb57a271fa0b`  
		Last Modified: Tue, 26 Aug 2025 17:53:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0d55206ace0c0a52c3f7f272db1bf330e9c26fd96e5fec1578e79d04ae92b8`  
		Last Modified: Tue, 26 Aug 2025 17:53:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6543a7875c2a07fdfe947b8de151a36c70b84d78e30b03081655bce0d3ad49b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00d5d073ba18bf9bfa39c172505151d530a0bd393a98ce78da1a680b5859e19`

```dockerfile
```

-	Layers:
	-	`sha256:a61de1383119def08b0016b6f6bcf931f223b0c65a72f38e6481e25b631539e5`  
		Last Modified: Tue, 26 Aug 2025 18:41:19 GMT  
		Size: 5.3 MB (5264820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bafd101508611c7b0590d66866a8937e87a88e3bc75b9441a2091fcba46f1d6`  
		Last Modified: Tue, 26 Aug 2025 18:41:20 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cc81b40f6f48c7889c89c43a9cd9088aa9556bf65c14aa9b63baf663711f7fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268947571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5acedf0b7cc2f1f221f9b211011c6eff5f498e8a153b605d701de7df5fc63dd4`
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
	-	`sha256:76db67347c5c0e38954b6134693282ff85f1bc2687c9bcbf31e1561216ec1730`  
		Last Modified: Tue, 19 Aug 2025 18:06:49 GMT  
		Size: 158.0 MB (157963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1aee4c10f4807e9441d72d9cc140508e1162d1c87c9cb2ac4b895b734d1a6a`  
		Last Modified: Tue, 26 Aug 2025 18:14:26 GMT  
		Size: 77.4 MB (77388851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec08758e9f5e43a3d09066a3a80fd0d8247a6cc92746092fb377185b47d4a910`  
		Last Modified: Tue, 26 Aug 2025 18:14:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca91163d0d04272abc3716df8689d849b73430d601cf2b6d107656b9ae9e67d`  
		Last Modified: Tue, 26 Aug 2025 18:14:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:162f0fa940c20f95383ee4489981750d9e8b88a67924b54da36eff3f6f685a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de594406d30aa17ba62f80655e62cceeeaadd317f53ef6aa05b912b2f4aa6a0a`

```dockerfile
```

-	Layers:
	-	`sha256:2c829015c802057ab09d92f1aeba3a4f11cf57d97d945778487f0c86b1b3e69d`  
		Last Modified: Tue, 26 Aug 2025 21:37:39 GMT  
		Size: 5.3 MB (5263410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1faeeffcfa426b149b453f47ac8432863e0c114a7d2b55b486b823377c3f710`  
		Last Modified: Tue, 26 Aug 2025 21:37:40 GMT  
		Size: 16.6 KB (16603 bytes)  
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
