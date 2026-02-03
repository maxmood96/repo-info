## `clojure:tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:455f3dee9ebd7a2b970b12bd03a64e63ee87fcb9be734a9709876e9184309add
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1602-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8866a4a0f5fe35e74f096381be5c64cc41fa37b176cf00b39682813f4958c57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221678251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc6f24a99e03b09474c5906af05865ff393f3edddf4cd290b24d725cb5fa1bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:22:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e604d36698b49d6ffdfc4ebf6b472e4b72903838c45ed8b8ce2125ac77b078db`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fc623b6cc4d614193b1a9e64c80e91feee6259f5cc3172a3d166a953ef38ab`  
		Last Modified: Tue, 03 Feb 2026 03:23:23 GMT  
		Size: 81.2 MB (81150408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc1a809877e6c17b26aaee1d4b75f5f69e4e22a682170ceae5cf43e8661f69d`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae7ec0c9a5b6b5724d904ad3b9f7a4127ef8eee0d308870bb297230fecfdc98`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fb2c444b7fc9f3a762657d20d376dc18c9573d177448f669478fa92e5a03dffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e20b83e83abaa85e86a93292992e35dc7d43e4183aa66da613a5c46cfd429d`

```dockerfile
```

-	Layers:
	-	`sha256:cf02cb98734aa2757facaf91b7e7c051fbb4b5d5df3e2ac71d55b0da6270a47c`  
		Last Modified: Tue, 03 Feb 2026 03:23:21 GMT  
		Size: 7.3 MB (7328199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48e1e2293f60cb76036a4f5e10087b348c41d6db20b24cc3b2e659d6212a2d3`  
		Last Modified: Tue, 03 Feb 2026 03:23:20 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab91764d20f9a9e20a9e0e52da13abad65efd9387171a41acf5bee3f6cd099c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220557454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565b19f2ef3b087bb21a14335ae9df066cab4789271181ae073e71b696e0b210`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:25:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:25:13 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:25:13 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:25:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:25:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:25:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5209cd1180975ed9b4cb5256a0e719f2eb5ba5c3c32b857be32712b7db7ae4d6`  
		Last Modified: Tue, 03 Feb 2026 03:25:51 GMT  
		Size: 91.1 MB (91052509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a113c2d259f8b5f6af8c385bac4e620d4a3905e37ab9256da74ea8c6d3f690b`  
		Last Modified: Tue, 03 Feb 2026 03:25:51 GMT  
		Size: 81.1 MB (81137946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba81b27bab3c910a62dbb04821f0d4f092816cb2dd1bdb36e91747f9d4fda93b`  
		Last Modified: Tue, 03 Feb 2026 03:25:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d21f1b2a893eb352fe98c94e06378a60109ddf8fc29b1033b9b2a343e774fb`  
		Last Modified: Tue, 03 Feb 2026 03:25:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4acb15b512c762ee648893e1bbc62ac17755d72ea95d69efb0776ce391cfeaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644d6d7008e46f4ca53ee108ece4b6428f7c9f74b3c212d202d190ab5c93c5ed`

```dockerfile
```

-	Layers:
	-	`sha256:2d15ed16cffbb447bddbc0cfc2045117cadd37366515df1f2049bb9638756c3e`  
		Last Modified: Tue, 03 Feb 2026 03:25:48 GMT  
		Size: 7.3 MB (7334031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e11aa9ef22e00c3967b6382ad334fd24ee783052413fc4f6ebd4512a1dd0a32`  
		Last Modified: Tue, 03 Feb 2026 03:25:47 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a13dc5d7b2c6e657d0ad08c11a4211a957a6cb1e80b7feaaa1154702123e2fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230925957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e331c103fcc81727b1b4a223be39c82b76f7a13789a92cac345fbc169f9eab42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:26:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:26:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:26:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:26:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:26:41 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:56:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:56:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:56:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:56:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:56:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f0540c2771fa9506db24965044fb39bf9f36f0c2c7623c568dcfe6110ba393`  
		Last Modified: Tue, 03 Feb 2026 09:28:50 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f615da224db1a3bf2138045feebadbc3619a6ac57d58a2a2f876c921b069b26`  
		Last Modified: Tue, 03 Feb 2026 09:56:44 GMT  
		Size: 87.0 MB (86986838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091e64c2402923af1d749cd3aad60c892d2cd2900f3ede1854df283788076e5`  
		Last Modified: Tue, 03 Feb 2026 09:56:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c860e7fbe2cb6824fd0069d55e9cde45f2822fb03be15d62b7ef8ea913438`  
		Last Modified: Tue, 03 Feb 2026 09:56:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c3c0f0a2495d0c949cdf72f5354facc09e62b9b4b53536bcfef90b981986878a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645dfd453bd9326b5d0cab44654b9db14caa499103859ec8c5a4accf112e41f9`

```dockerfile
```

-	Layers:
	-	`sha256:d80733aac3207e93bb5ff9e3aeadfbf228b250df06ab2ae128dabcbb58e68fae`  
		Last Modified: Tue, 03 Feb 2026 09:56:42 GMT  
		Size: 7.3 MB (7334749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07166d100686030f93d692c8f8224d521800e229e81ecaedbada56aa0d69915d`  
		Last Modified: Tue, 03 Feb 2026 09:56:42 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:07b670e58da8af1d9bf768bf32a1eca8de51af12bbee8ceca62de6edfd3895e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215312955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a07d3731df96f542823161490fa078e6b2c5d94f07f4eef614d0db8e6819e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:06:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:06:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:06:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:06:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:06:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:06:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:06:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:06:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:06:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fbcf9e62fed9a27010c243172583199c320889fe240163fa48c65ec281731e`  
		Last Modified: Tue, 03 Feb 2026 05:07:28 GMT  
		Size: 88.2 MB (88210680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c82570398ddbbb4d1d4689642187c8f3425c64185e830d7b5b407cd79c9f9cb`  
		Last Modified: Tue, 03 Feb 2026 05:07:28 GMT  
		Size: 80.0 MB (79962889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17055933c93fe4a12bf47e4896516bc9f9cf2ae99b28d422a7d6fd9034c5e9`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e4d369dc1f6ad8e7e1c64682e54c8c141eda912fe416eefcc1d5b8228a8493`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7ef54313aefc9bd7627a0dcd66d77612bf29374737cd0094d71853145d0652b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6eb5c8bab34444ccb0098228ed708476747c8b767ccf8896adf9c5d58ca4b`

```dockerfile
```

-	Layers:
	-	`sha256:3ba368cbe7fe1f686fa2aeff03d3fa12913cccb6c9d4318b5a6e253a94a1779d`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 7.3 MB (7322066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac05d94e64deef910cf0657913ade33d2ec7e515224e68e9b40020021c840fb2`  
		Last Modified: Tue, 03 Feb 2026 05:07:26 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
