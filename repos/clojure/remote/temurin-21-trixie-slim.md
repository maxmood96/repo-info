## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:4825fe4dad997592089a5c2f689258d3f7688e55beb7fc07dc4a5cbf860eb635
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b0f8bf5e42c2a265b8af0120a72e8d06acd1840b69481f17625ffbfa968f3275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259561988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f06c3c4146e787c7771e847316920bf2e644435ca15a7cbb0d40238dcdbba4`
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
	-	`sha256:6064f4f5254f6a00caf4b34e2df8daf0a6a5bff71afab72002ae2d53e3e625b9`  
		Last Modified: Tue, 26 Aug 2025 19:07:21 GMT  
		Size: 157.8 MB (157804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1cb4f5133c3354e4e3454f3ac40e7dd4b96c56c8dadae4472da978eaf2f5ec`  
		Last Modified: Tue, 26 Aug 2025 17:28:29 GMT  
		Size: 72.0 MB (71982888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7cded1d74692f085fd6cff91fb4c5b73a709b4abf7da8ae8b3ef90456e101d`  
		Last Modified: Tue, 26 Aug 2025 17:28:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0b5a698da972e02dd76687246af201df6c7850f296d9e1126252043fbfcc1d`  
		Last Modified: Tue, 26 Aug 2025 17:28:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd4c708f8b960c1ee41cd2ea10057ad24b759b3ace4e494bb77a0fd99537d7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae229c11176820f6aa85bfd94f3eb539216a8530021439862f76aeff28f83ae6`

```dockerfile
```

-	Layers:
	-	`sha256:b191486db5463c714432bdc4c303305bc39946059880f3f5e2108af2bf6b442a`  
		Last Modified: Tue, 26 Aug 2025 18:41:13 GMT  
		Size: 5.3 MB (5259027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ca477c98c6a1e6dcf56e2f56f560c31026c484a5a48b8b2d828bb6d8067c36`  
		Last Modified: Tue, 26 Aug 2025 18:41:15 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:477dbe11ef340252649723f5c5ef2be2a75082a79b611b41a339fdf4649298ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268848693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856b14fa2b36bcdcaa4cc0513c9c9ee6547c80951c4d0477e939d9ee459bceeb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
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
	-	`sha256:f1fe20c3590179dea93033a43edd140d5e8c47921d36adf1fa7ebf3de0413b4e`  
		Last Modified: Mon, 18 Aug 2025 17:33:58 GMT  
		Size: 77.3 MB (77289979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b208509fae9dc5077ae1462db574ea3ce3db2d87eb67bd025562a15a323394d`  
		Last Modified: Mon, 18 Aug 2025 17:33:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8140e1385a3a47f0891daaa3ec5afffb0532c11bdaa062d93abb3294c6450d37`  
		Last Modified: Mon, 18 Aug 2025 17:33:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ce53354a98b7648703e79d674b73bffc89a4cb8764e2e18122639b1b59bbcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a5ac281dc96deca0659317eefd3fdfa027fe0c5d7b08a0152fcfcb54efbf05`

```dockerfile
```

-	Layers:
	-	`sha256:7faf4c829f8ac3c3084fd3370c006448d2143b8f9b067f064f128b61c562a6f9`  
		Last Modified: Mon, 18 Aug 2025 18:42:02 GMT  
		Size: 5.3 MB (5263410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e58add7882e45c69a2fe38d0d5882a4363e9e0259db5c8fadbf5c72c9438142`  
		Last Modified: Mon, 18 Aug 2025 18:42:03 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:1474f52ebd1ff711c0ee32d0b48e21e0c937c9a5295e0e03f6a9bca3399c27a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252646482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c994a4860d925c9fce64f0ad2797d98cf7aae9fe9b886dc8fb688fd7f04458`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
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
	-	`sha256:3d9e1b3d89b6225825671ea9a5be73be68f247087fae6e061b3885b46f467a29`  
		Last Modified: Fri, 22 Aug 2025 00:59:07 GMT  
		Size: 70.8 MB (70780289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7d7e9629b149bfa099b8386ab4b814b285e0916a1fc594108f55e1939b5e6d`  
		Last Modified: Fri, 22 Aug 2025 00:58:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2b4d2e82b26405cf2e3683bf9551988461055113d6c3877a63023ba0d85efa`  
		Last Modified: Fri, 22 Aug 2025 00:58:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:253b31153f93f7a2f65297e13718eaeb43c2c155d563629e00b2fd9b8aeed258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918b6103adb2d78a02af3e6ab81bcac69d623168af5268ccef9f1c82258328bd`

```dockerfile
```

-	Layers:
	-	`sha256:b38c875de753ec50c36584f90cf66d7352cfbbce0fc55c72bf60497707a8ad6e`  
		Last Modified: Fri, 22 Aug 2025 03:36:52 GMT  
		Size: 5.2 MB (5248503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cac3688d6f6eb1bb4509c889dc61536d8a1b8e503fd50f55978cbd97a5bf082`  
		Last Modified: Fri, 22 Aug 2025 03:36:52 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2a8bc8157702575ec8bd3eec97a6996c2a4ec6e5484a0071cbde2776128c3355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249711157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41caf566661ed6b0be22a023a3cda22f3a624e16c349ec95b12c9b2f2581c6e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb1da63a2e6ff87dd1df9af5da65d1cb06ecd89a53f42d9ef6f63cbdd40d75d`  
		Last Modified: Tue, 19 Aug 2025 18:06:35 GMT  
		Size: 147.0 MB (147026954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2e6545ffb49e9b0eeaf372c6fb8d4e1078c041737576f288b1cd2fe5bd41ab`  
		Last Modified: Mon, 18 Aug 2025 18:01:09 GMT  
		Size: 72.9 MB (72850100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c6c7a99491cfb30fdc3c386db656726b6fcfd825179c9b39b85e8ee3c5ee8`  
		Last Modified: Mon, 18 Aug 2025 18:00:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2889d4fa36c0ac22472052bbba58e51e46c38d3493f53384b45c36f11a95cf`  
		Last Modified: Mon, 18 Aug 2025 18:00:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ff0764985222746d42e5b32e265f4a4149043b12b78dfa1441756db50b9abe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89317330074fd257265ef623496eba61eaea10e953b4ef247c7b3e277dd6c1e0`

```dockerfile
```

-	Layers:
	-	`sha256:c3af127d0e70f55bdcda4decf698bf54ece65da4fa076a9e329ecf52d43fc51a`  
		Last Modified: Mon, 18 Aug 2025 18:42:08 GMT  
		Size: 5.3 MB (5254951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30104aabfc3a6b2acfc1c52b15a86947614a64480d884e2d2c8e4b445a8c1112`  
		Last Modified: Mon, 18 Aug 2025 18:42:09 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
