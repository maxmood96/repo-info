## `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:ba05dd5ee508aab771ee7016639ad61f6bbc05f36bc736da804dbb466e53c3a0
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e5fbfae80ea63de84591c1101ee2da5901f93cfd20b2585a6b1b1aa5c45a12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250560806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3cc777137fbd9c151eb50f8150b0ea652b13420a5c6722e04d12b0890300f5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:03:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:03:08 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2370006d61322e9317a583479da6057565d4805d8e5a6c756d42dc6815f6f610`  
		Last Modified: Wed, 15 Apr 2026 22:03:46 GMT  
		Size: 145.8 MB (145806793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf02e5524e7655e67c73f2cad45b86c8cddba7247e2e31be77a1a837a4da7f5`  
		Last Modified: Wed, 15 Apr 2026 22:03:45 GMT  
		Size: 75.0 MB (74977726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e64c32e43ce3545230fbf90d844745f407d22198fb2d8fdc65c33677b8a7d9`  
		Last Modified: Wed, 15 Apr 2026 22:03:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:371c078080ba426f30fceeaa0699e38013a523e1e49c8aac46a875f755562b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6aabe48b70ce77b2b1eeb724d30d5dd8a3c13e4f3d85113ec4c2de8aed88cec`

```dockerfile
```

-	Layers:
	-	`sha256:5e629beef0a7f756910d9f64dbc22a7ae194dcb589a5a365e6cb902b37c02530`  
		Last Modified: Wed, 15 Apr 2026 22:03:41 GMT  
		Size: 5.3 MB (5279279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389751c6fdedc8842888bc6614ac037ebf2108e857679303a9213613806c5812`  
		Last Modified: Wed, 15 Apr 2026 22:03:41 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77418b964f2c3a9807cd25803a2c39f48d808ddba994ddf85e2af4ccac5a2a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244470986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a63de7852638c2b0a8d81bae8e0e679a93be4d87fa092fb21928c711539d39`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:24:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:25:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bec000b8c51d641ad70625e6709b178a1f342640b122744f30dc2de641fda`  
		Last Modified: Tue, 07 Apr 2026 03:24:49 GMT  
		Size: 142.5 MB (142500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0916d1eaa5d7f03412a723c0122d78dad7c3bb6aa8064fd66fb6f385fda2d3c4`  
		Last Modified: Tue, 07 Apr 2026 03:25:31 GMT  
		Size: 71.8 MB (71831719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9868b4226bd186817e2533231479fecd2d00f2d09ed92b106533d262fe0b5760`  
		Last Modified: Tue, 07 Apr 2026 03:25:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b43dbe9362ba7818984a5b0ac482c5881bf2b17cb7cab3dee2a2057c4638273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa21f6e8ded323640541a1e0afa31c7ca49569be4178bad211d231b6d3a303fd`

```dockerfile
```

-	Layers:
	-	`sha256:cd8473fe7ef88b11260c3d5827c99665073f07346d52a2c0f251dbad96dec78c`  
		Last Modified: Tue, 07 Apr 2026 03:25:29 GMT  
		Size: 5.3 MB (5285666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d284e454a5096d8d1b79317f19d4c221af4a339175acf580abac698880ab0dab`  
		Last Modified: Tue, 07 Apr 2026 03:25:29 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:129122f95eeef78b0b2f1a78f6e3cf07b318c728a89f016d476e7e361b44e152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244021016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2455f9e629067c91e48f8e1bca1725c766fdf83e97a99947c03142a97987a5bd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:31:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:31:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:31:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:31:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:31:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:36:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:36:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:36:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e26676b8fc5a07c40bb71da4c5066413b10ef71e116aefba94d4275fc936247`  
		Last Modified: Tue, 07 Apr 2026 14:33:19 GMT  
		Size: 133.0 MB (132997689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c99f3b5a97050d1314359ce71b9cc4e078b9df063bbc78feabd2ed9f9cfa0`  
		Last Modified: Tue, 07 Apr 2026 14:37:29 GMT  
		Size: 77.4 MB (77429666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b10f6205c9f832d2ec8d079dbd4b14f8a382170fea582617ded3bf2ebf9d61a`  
		Last Modified: Tue, 07 Apr 2026 14:37:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1819446fc0d32351af23abafd45db4099269c023910bf3a719dd6e919860a4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cacdfb41afb6e9fdd5f18ac3c518da5f922897cc1e59d51c76edf7f624069e`

```dockerfile
```

-	Layers:
	-	`sha256:3c337323f580707878b1997d2c877bbcdffb8eb1163710dd0b77ce5e5d9d7db9`  
		Last Modified: Tue, 07 Apr 2026 14:37:27 GMT  
		Size: 5.3 MB (5283035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a8f98917823a65e12f45b3d4779bd7b7b083772582f4384650a34f6506b1b91`  
		Last Modified: Tue, 07 Apr 2026 14:37:27 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:934ad825c9862e5bfc9bf2c9ae7b397de871ddd429bb362547841b2834cbfd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229385369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a8901136fa55f5b7dc4fca7111128daf48f1a4132f3d56a4139c00ce871417`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:41:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:41:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:41:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:41:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:41:14 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:41:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:41:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:41:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3bd3257f5995d825c3c93d6c134675d2a96ca8e8bc241408714637624b064b`  
		Last Modified: Tue, 07 Apr 2026 05:42:00 GMT  
		Size: 126.6 MB (126562194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7784992323bc39557d6fdc023185e05f8bf46d81784d747e6c573971ed86ad`  
		Last Modified: Tue, 07 Apr 2026 05:41:59 GMT  
		Size: 73.0 MB (72987113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6df84d8535f86c910d5dcbb4568390a4dfb11295f495e197d1c2d941557a579`  
		Last Modified: Tue, 07 Apr 2026 05:41:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e61da64dbe8c5e8dbd93a0a5451dedbfb19e26137c68094e882e60ac8d09bbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed5d6e3fac87e0e9a1f9849ea1be93a6bcca0574ad0c60355058c8fff3b10ca`

```dockerfile
```

-	Layers:
	-	`sha256:a0619a7855b5053c5ed9355864981de5486da3245652799c7492a4ed69e41c17`  
		Last Modified: Tue, 07 Apr 2026 05:41:57 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136df1a679d87b6de25cc3dcad46493e123e77c5a185ad67ff28a24bdcf8662b`  
		Last Modified: Tue, 07 Apr 2026 05:41:57 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
