## `clojure:tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:96e7cda0fcd49adc9854ee0d8fbc1b45d33acf695607f1f73a24c0d33def6fda
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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - linux; riscv64

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:79148ad057760bd3efe49162881f15039e9f4149e2ac26e8937fc17f16d9a16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249810692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1276b60817c5625d8824627b7d1dc14265f99465955d9ff9d3fb16d6c80eccc8`
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
	-	`sha256:ccb1da63a2e6ff87dd1df9af5da65d1cb06ecd89a53f42d9ef6f63cbdd40d75d`  
		Last Modified: Tue, 19 Aug 2025 18:06:35 GMT  
		Size: 147.0 MB (147026954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8595743e0b804f0e0c083367c08db88acdb55fe134a9aa40354da102527f369c`  
		Last Modified: Tue, 26 Aug 2025 18:41:54 GMT  
		Size: 72.9 MB (72949636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c890806ecd6f5cbd76acfdfb81d9fd5be640e2600e8d34d43ddb6cb98f5aaa7`  
		Last Modified: Tue, 26 Aug 2025 18:41:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271f728a59f0d91b70f261ff8f449331661981fe1679440deffff2004bf3066d`  
		Last Modified: Tue, 26 Aug 2025 18:41:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81c75efec8b0cf17d7b1c0cdda7e00813685a7c0f2ff063ac5ee2a5065e7d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f74103d87ee26bc5e956d65dc7d224ade79490de20afec018b1b2add598afbf`

```dockerfile
```

-	Layers:
	-	`sha256:31de046e8cb875b907d16d8d293bc989a98da5195a10175c9571cd5dd5f17da0`  
		Last Modified: Tue, 26 Aug 2025 21:37:45 GMT  
		Size: 5.3 MB (5254951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71093f311f6547b63321411c922566594e3ce14335a1669d68e8c81335955a01`  
		Last Modified: Tue, 26 Aug 2025 21:37:46 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
