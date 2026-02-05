## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:6806cea2567d572e363e7439c48381f78c783e2c11004afa3b71c1f3882e4d3e
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f54a96cdf5bf239591cd1b4b44e9a3722bf05425a8d1952129c7c5ed98114b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259601474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2823a4b6e3d276655fcca788752a48618e1c306083fc2f216912817ecf7fe11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483296f9719872eaa4ef3d1826e98b176a7c8ff2f5ea87a1a8d3f294bb180027`  
		Last Modified: Tue, 03 Feb 2026 03:22:41 GMT  
		Size: 157.8 MB (157826034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1cf1bea7b2676e1e6a27354096ea807bcbde653f06d30af63bcf75e39df39d`  
		Last Modified: Tue, 03 Feb 2026 03:22:39 GMT  
		Size: 72.0 MB (71995800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3a8e35a1e3edd570a21990bb50e963e8007cbc47ab28a70b2865740bb9439`  
		Last Modified: Tue, 03 Feb 2026 03:22:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3ae4f2b7ffdae39a80f29a740a064767e46be59c211077a6e9b89d773000f`  
		Last Modified: Tue, 03 Feb 2026 03:22:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1945cc3a586c0fbc0e304b364bc40a3fd1b69ad824a652359b6beed93fce7cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04de16012246aada5b0c0ab174880fed2e1102873b14f917784a899ebff99550`

```dockerfile
```

-	Layers:
	-	`sha256:9b8c90b0907f0ced79d3f648a156a0e8c14b3c6a454c346979848f72bdd81cc6`  
		Last Modified: Tue, 03 Feb 2026 03:22:37 GMT  
		Size: 5.3 MB (5259401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1b6acc7848151bfde746c44b29e6c5ed40218afa42242786b4429cea8bb353`  
		Last Modified: Tue, 03 Feb 2026 03:22:36 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:240b53cb10053f966e2a55f7fd877cb15e8427a402f2cd7ae0ef23b12b366d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258055240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b898e119ba8af8faf4b3629fbcde00af86c94ef4f5f8506503498fc8ac87814`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:29 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:29 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833e80b106cac26e6497d2006087a64c627272be142bcc3768915f028d7a2d6e`  
		Last Modified: Tue, 03 Feb 2026 03:25:10 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c8c6b6b4529dcbf6af26be4b3a5286a4e20ccd85c00fdfdafded4b2190e6f1`  
		Last Modified: Tue, 03 Feb 2026 03:25:08 GMT  
		Size: 71.8 MB (71806553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da13a8e5d4159cd6a85550c2614130f915c19f9f8e883483d0a084ec7338b36e`  
		Last Modified: Tue, 03 Feb 2026 03:25:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e4b47f5e6cdfc33f6179dffe2b1250afe428d37c0657bc0ffad53d2121de9f`  
		Last Modified: Tue, 03 Feb 2026 03:25:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd7488f9aa75c718ad95dc16eecb7fca71cf21899fdd96b59687b9d39f2da39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e812a6bb1b4d8badd05f4969c9be3831d089b436e95dfed001d5f600243b6377`

```dockerfile
```

-	Layers:
	-	`sha256:a1a79de2928e4e779ca9024542263c9d9aa4362f2a17cc964775489415139f0f`  
		Last Modified: Tue, 03 Feb 2026 03:25:06 GMT  
		Size: 5.3 MB (5265170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4610aee64bfa210160320476f478749da85cb5cbaa660cbd7eef46302abcf19a`  
		Last Modified: Tue, 03 Feb 2026 03:25:05 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ae5e449cf37f4a7829e20c707e42c7f5e782add71549e5e8e60e65a8daa2f832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268932889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca5803daf5b85725fc1dfaf51cecf2b3cbd147d684268de0374976cf704ace6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:48:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:48:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:48:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:48:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:48:58 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:52:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:52:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:52:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:52:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:52:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ba07059713648627137e8de0f61be244826f8880fb66d4f5420970ab2b0066`  
		Last Modified: Tue, 03 Feb 2026 09:50:30 GMT  
		Size: 157.9 MB (157942944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5f2beb0191d7f580ccb4a2c6a895ff2634f47918fae425c895399e14013832`  
		Last Modified: Tue, 03 Feb 2026 09:53:30 GMT  
		Size: 77.4 MB (77388717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28ee3f2f73aa212acda23c942e089a59e5dd12a35f579124c03d190810613ea`  
		Last Modified: Tue, 03 Feb 2026 09:53:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286421d45d08fa30ac4fdafb6ae8a7943889d2ddd5a7631f3354384b6c7ad63d`  
		Last Modified: Tue, 03 Feb 2026 09:53:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e2ad808d5ea5d5ec677e2cff16750332a09a2c3e8f135d423ab5d301dec4933d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84070b62ee1c769f4a91e387121b0b1f4db67a53a6df6032fc0f76084feb6adc`

```dockerfile
```

-	Layers:
	-	`sha256:617f456c9f7ae6359bf64bf99dd88ed08ae39b1fba29c1777fa25849df9b07b5`  
		Last Modified: Tue, 03 Feb 2026 09:53:28 GMT  
		Size: 5.3 MB (5263772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ce5ea33deac93b4e36d65fb7ca799d41ae6e97945d95ba64c39611bbf236b6`  
		Last Modified: Tue, 03 Feb 2026 09:53:28 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:2446e5b896ea2cdf62132abe239d4d5bdaf103ad5a6c2db5e9ee551f579000df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256350917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b09515d829d663d53c9562dba739a2fa7f5dc394982064722d7ad1f9da246b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:50:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:50:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:50:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:50:06 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 20:50:06 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 21:07:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 21:07:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 21:07:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 21:07:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 21:07:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080871d584089d7c07fc75a8f84b6f61cae2c9a7204a550f8b8dcad13b49c423`  
		Last Modified: Thu, 05 Feb 2026 20:56:46 GMT  
		Size: 157.2 MB (157194292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346ee878cdf42cb464edc491dc5e0d64d0f9de09df3e571c4188935353e7f02c`  
		Last Modified: Thu, 05 Feb 2026 21:11:34 GMT  
		Size: 70.9 MB (70879189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e97538da92def49be7476848e779ea76103ab7fc72a5856a62063189822c22f`  
		Last Modified: Thu, 05 Feb 2026 21:11:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8dfc424548cf665622dc62b2a61b302d9c5261dae641848e04270ccddaaeec`  
		Last Modified: Thu, 05 Feb 2026 21:11:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c63f0a79fc5a6d959d0a03c6cb5cf9d77d0a393ed4740170960c60636f3cf6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd4fdc4b93833a20f603141916f8c2b19d83028b2973cd7129f4e5c4bdf9d9c`

```dockerfile
```

-	Layers:
	-	`sha256:ade1ecda0245d282b7cee0e96b03b1410f40f6e082a305610f0e8d3f76314a94`  
		Last Modified: Thu, 05 Feb 2026 21:11:24 GMT  
		Size: 5.2 MB (5248865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf0ab1aa122b621b57e257c44cc81d8ed74fb57d1904ff1f12feb9a17db42692`  
		Last Modified: Thu, 05 Feb 2026 21:11:23 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1671d07847d361f056d476ea067d8484e6200e2a8a1e07f80a0d227cbdcf8931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249861963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f57ea2e18f52b58fb2216119a238b54620f45f07509bbdfbb292340e67331`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:04:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:04:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:04:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:04:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:04:50 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:06:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:06:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:06:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:06:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:06:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ddacf145453dafd4beb96b06bd9815ba82a596f69a0b76695fe62e6eb186ba`  
		Last Modified: Tue, 03 Feb 2026 05:05:30 GMT  
		Size: 147.1 MB (147069811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44272bef96edab1725da6d1c0c6b5debcb613fcc8907b69d560017aa60578c99`  
		Last Modified: Tue, 03 Feb 2026 05:06:28 GMT  
		Size: 73.0 MB (72952962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f3e7b7498b4be51f3fe20adadef4c5c87e045548366d772fbaed9837c0eb60`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceadabd8b75a3a6784823323246701ad2c70aacb54cd976bfcbdc6d6f8cba45`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13acbfb84559262bc4b3cc6d832592379d472acab1ad1c71197438b9494c446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ac3f7e33f8797567bcc9b76ce8c0b546bf3ca3e11e081d2e49b1c3cdd85a86`

```dockerfile
```

-	Layers:
	-	`sha256:97c66c5081218fe15fdd610c6dfecfacf7aa9966f18e6e1e150f91a8ecf1825f`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 5.3 MB (5255325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16b250399a90f1fbe5ba279ca90c115c6ee7d7049bad20d4503348b5fac7512`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
