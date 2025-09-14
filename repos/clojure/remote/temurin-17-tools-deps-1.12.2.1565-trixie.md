## `clojure:temurin-17-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:c7052c6c07c32e4758d595232320ebe03f715f247d04e3f11feb7b19bd455801
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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:97fc8750e400658989b68abe6822422b599720f7b5f2c8c6932ebe4c44f80660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279507350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0139dae685207648c94980b72ce0770dbf40d2639b700aa6b209cbc1ef1c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750bd5f3a22be32fc81adf4bce128e32e4537f4514f76b56c4c2655fcef998e`  
		Last Modified: Tue, 09 Sep 2025 13:37:23 GMT  
		Size: 144.7 MB (144693322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83d0588ae3ffad300d34ccd7be4dd3344810645d944b807fa90174c2e6fb7ed`  
		Last Modified: Tue, 09 Sep 2025 13:37:23 GMT  
		Size: 85.5 MB (85533455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392930615aaabbe55bc7c19aa681c40bdbc3b5b133cf253f0b280c763717309`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764cf20fd8d03092ec87f1be961989a2beaed2adec370fcb2a5862d589b08634`  
		Last Modified: Mon, 08 Sep 2025 22:59:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:60e4b23da0fe257a39d0efebf23949ea79bd1d2e1e70a4b77d5e012910a69320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60fbe49bd821c029488852b36931f0a650c1fe7a69039ad21d0027045f78dd0`

```dockerfile
```

-	Layers:
	-	`sha256:fec296178075feff80196c0e8b74b9ad5527c2001d71af9da621e7de12f92c4b`  
		Last Modified: Tue, 09 Sep 2025 00:39:05 GMT  
		Size: 7.5 MB (7466845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446009ba92eea641d97ff1546a61db8ac7f9a939cb17cc884007d9981c4ea3f9`  
		Last Modified: Tue, 09 Sep 2025 00:39:07 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49a996d902e1a1a3fb1d35d776d0a987b5d74be731cda067c69ff49c0e13a2d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278545040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360d12add6de6bcadc276d23cf39d689bba4d493b20a728b0a8357ae8980c930`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25f1d43454a260dfda905cc1d4206fe8d2d799dcac783ec6b7b54d223684a14`  
		Last Modified: Wed, 10 Sep 2025 15:09:44 GMT  
		Size: 143.5 MB (143542205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489a751cad7ba3a157d0ac9770d2668a8bf1fc52073e2c74451420d12d6c431f`  
		Last Modified: Wed, 10 Sep 2025 15:09:47 GMT  
		Size: 85.4 MB (85358051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3258b508a1d8fa207944e3a2d286d7a7ff4a1d4c369e8e70daa49273d67bae79`  
		Last Modified: Tue, 09 Sep 2025 01:27:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a2f02bcb003b75f4ca405cd0ea992d556b262dc8aafe7027080c3c13f16e32`  
		Last Modified: Tue, 09 Sep 2025 01:27:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2fc166cb37d52a1e0dbf3bc687e718593d0063140131828ed6bc4770c57f9b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dcbd6545a86cd0bd62a70493605ce741648fe86aa1fccc71eb021ce1e75daa`

```dockerfile
```

-	Layers:
	-	`sha256:95159b2c69f88bb55ce3e8102b996b6f600919bb8a70e18cb4ec0fdcf1080785`  
		Last Modified: Tue, 09 Sep 2025 03:38:51 GMT  
		Size: 7.5 MB (7473875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c02dd43b0a82a942d3725e0fa25a1758fb7642fb87c012f7bd09a90003742837`  
		Last Modified: Tue, 09 Sep 2025 03:38:52 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:11cb2b468aa3471174883d0fa83a023e0edb3defc176966508496d9965db41d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288429470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550a0360753a2e856bed47cd84b33fb6bcc9a127e596c7256075489e398fd1c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2cb726e12fbe7055952138d18255d03d0609a6d3d02c47b3a40a5e71f49b3e`  
		Last Modified: Tue, 09 Sep 2025 12:22:51 GMT  
		Size: 144.4 MB (144372674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5e4f072ae1388265158f464d5abd55c5eb9de7d4c170e73e81c6b88f3784f6`  
		Last Modified: Tue, 09 Sep 2025 12:30:54 GMT  
		Size: 91.0 MB (90951323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3dded4cf94c54c61528d3a1a6b5fe6abc60eb8390883b43e13a9b9cdbf3754`  
		Last Modified: Tue, 09 Sep 2025 12:30:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc54c5c10eee4e24f06c811d04c8169e76e871cee61218a4080b4203d2dbb2ac`  
		Last Modified: Tue, 09 Sep 2025 12:30:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:50b6282690e775c197b12879dce55f6efbed95ecb63922d9eafd91b509010c45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3abd8e020a31cf6ce5dbbf6ab23a8cce29df64d0a0457557a6ab2a45dc6e45`

```dockerfile
```

-	Layers:
	-	`sha256:e60eafde109992beeba623a0908f36d4fb853019ded80593dd14827261d87873`  
		Last Modified: Tue, 09 Sep 2025 15:37:22 GMT  
		Size: 7.5 MB (7471264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:440ad233a6cd222a5d49eb195f516c04f0468113c9ab9299df32f42a8347c834`  
		Last Modified: Tue, 09 Sep 2025 15:37:23 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:23cb98792c885e61a49132b7969b8bc71e9b286b354edac5ba066774b138c016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270769439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd6d9e15963126916cfdf858cc84aebeebbd0612f729f3871cfdb9f7f29dde9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576de48387eae09e686401ecb3cdf77b9f0559251dd70fb4cffd760e43d9340b`  
		Last Modified: Sun, 14 Sep 2025 00:35:44 GMT  
		Size: 138.6 MB (138575690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b6be2f484d151c428b35270baa77ef8a6d2a928c2ae4ca8fe9fee06093b54d`  
		Last Modified: Sat, 13 Sep 2025 23:56:34 GMT  
		Size: 84.4 MB (84427260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b2bac421c9a255dd93352785ab9dff3308a4c505ee0e4d5a6e7e09ca3131e`  
		Last Modified: Sat, 13 Sep 2025 23:56:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea26d448f23257fc87db0082e64f4f62549ccca63ec4cbd0f630d1c0215ce6f`  
		Last Modified: Sat, 13 Sep 2025 23:56:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:67a8c4231e37b087e8b849cc9df7eea2520f162a8f18158ecf5fd6b280d9823c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51a478b146ff2521d6f7053807eee458be3b24e7c0b469b4b87df314d7f1866`

```dockerfile
```

-	Layers:
	-	`sha256:812eb21faf7064cb848c17be568d0b01a9dcc01348b0b00eaf32ea06188fa26e`  
		Last Modified: Sun, 14 Sep 2025 00:35:41 GMT  
		Size: 7.5 MB (7452839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8807d2eb02207f57b71f061d73afa5603bc93d66a32d2c20471e0fa170be9201`  
		Last Modified: Sun, 14 Sep 2025 00:35:42 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:584b024afc7af3a4b87947a79a842e08d93662333c0eff51f261cfb6297b4feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270577643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12d3845290e60ef3fdd36e1dedd8b5324029ef105992189728a36dd03d99c3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548ba50c221c72eba44905ce6df5a032b61f44113604ffe5fb673aad8855a32d`  
		Last Modified: Tue, 09 Sep 2025 05:36:54 GMT  
		Size: 134.7 MB (134724301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647e3eed3586fe0fbe423579bc8bff18acbc3d57204eedf32393644e0b8cf057`  
		Last Modified: Tue, 09 Sep 2025 05:41:31 GMT  
		Size: 86.5 MB (86505975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf22a0f0813de93e020d6b94c88e2097688d5f48034ad6c70f335df07c17c66`  
		Last Modified: Tue, 09 Sep 2025 06:18:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcc99cf9f6dfc11df6c6ad0ecce48f77f78e26a05b5196ad66cf7560bec2f1f`  
		Last Modified: Tue, 09 Sep 2025 06:18:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e12c0a53368e1b58b238cd8b62590b9efba6bc37855f3a0df6a1c3813b835d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d231020966eeadc0d88ca1ede1fcc8edc9d8b44cd532f680d1a6a5abf2553837`

```dockerfile
```

-	Layers:
	-	`sha256:f7ae4826d95ee9a4fef86edc284df9e8441027764aff436863a9078f80f69416`  
		Last Modified: Tue, 09 Sep 2025 06:37:50 GMT  
		Size: 7.5 MB (7462767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1158447bd6844b9eb068794645fdc9d286290f76880907d9c3ae52f0870cd6`  
		Last Modified: Tue, 09 Sep 2025 06:37:51 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json
