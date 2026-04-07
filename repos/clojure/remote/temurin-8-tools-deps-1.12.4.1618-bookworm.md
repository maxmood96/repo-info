## `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:8c92b05b378b65a97b4038bde7f812cea18dd06232e219c8e99ce130cc1f9511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:46c1960fc2d7cbba223211af5d39d0ab49b4d58f47a312b8080b8b18735fd490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184836974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cadbcb5dd8d21d645132f350a4c810166ffbf2c4dfea78408e8878cf6da72a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:12:46 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:13:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:13:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf02ca4bd39a528df5ff0638b6ead50753731bfd8537372b55d9fb37c747f94`  
		Last Modified: Tue, 07 Apr 2026 03:13:19 GMT  
		Size: 55.2 MB (55170189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bd0f0a80e3721863763b1b288c5473d8bd6b4c0b7a05721dd2eccebba5477d`  
		Last Modified: Tue, 07 Apr 2026 03:13:20 GMT  
		Size: 81.2 MB (81177317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a358a7022721ccffe58740c80904db4473530a8a35b6020d745622dc50ff4b0f`  
		Last Modified: Tue, 07 Apr 2026 03:13:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5ba2644461fdf0d4aa75b3922a5b3a8587a6b4412c556efd21c6380fed9e0756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b927d287a570552b23fc390c664d69c4d72c5881601d97a56407dc252efef6`

```dockerfile
```

-	Layers:
	-	`sha256:34ba1de9c3a2ab4713058dd2862ff11420c6fab435fbc4cda90c226a89f64b7f`  
		Last Modified: Tue, 07 Apr 2026 03:13:17 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1c2bdfa60d048deef9084bed3ebaba3b6a19c1a0a8d30ac78834f7c99779d4`  
		Last Modified: Tue, 07 Apr 2026 03:13:17 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0ab74479b241e4c5bb9b45b565f3da7b3bca470f234069033197fec768c82326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183784211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d4d25bd5408e42fda4695c2e66eb80858828c7651ed1cda87aef637b4e271f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:23:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:23:35 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:23:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:23:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff997ba05ac908303de6fe52bc5bc8d49c40c4318fa277115ca76c558424d9bc`  
		Last Modified: Tue, 07 Apr 2026 03:24:13 GMT  
		Size: 54.3 MB (54251627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36af253777603db5c68a86b350eea7873d72c6773cf95a72fd8f4aea2a6943`  
		Last Modified: Tue, 07 Apr 2026 03:24:14 GMT  
		Size: 81.2 MB (81158678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70d39614507922f742929b54f943e5dedd5de2c78b44fd3d4223f99c0d496f`  
		Last Modified: Tue, 07 Apr 2026 03:24:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3c7b73fac5c6647d83b258049c2fdf3b8f2cfd446b2e0d61e9a8ef49710dd3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595936cd0b971fde4a9515d4d208e0675f7a514e5760e510ac04e4162aa76b61`

```dockerfile
```

-	Layers:
	-	`sha256:6df071d385abf14fc981737fcaefd6c43558055ee43efaccdf78a7a0bdb2acd6`  
		Last Modified: Tue, 07 Apr 2026 03:24:11 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2639e3098c1d8b44ceaa9ac97f00012698fe2dd661c26f2a2b18a9d34c0f622`  
		Last Modified: Tue, 07 Apr 2026 03:24:11 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c941cf042053120c30fcd5f84b21c1e8aaa3540e7b2ddc4c0bab5ffecf0ca0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191987912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7e9629fe315e1c85d88088b5610ddbfd3bffc21c359ca5cc894dbd1d190adb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:05:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:05:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:05:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:05:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:05:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:11:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:11:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:11:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd8a512f09ca4bc519a670ed8fd28c926eabe017586c8482ba206fe3cdd0ed`  
		Last Modified: Tue, 17 Mar 2026 18:07:16 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e96b1d18752f802d8973a2e536042d78af6060e537182df695ea638bb907a3`  
		Last Modified: Tue, 17 Mar 2026 18:11:39 GMT  
		Size: 87.0 MB (87000175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cdb70a8cf08091d585cf88a8109f83a2667943f4a027bb7236ef83df855fd`  
		Last Modified: Tue, 17 Mar 2026 18:11:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:60c767484466430172af9bf8a33e0fce612bbaeb9a36421a26f8ebe2e1ce5236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2df117c55e3a6072263f26109db9e715047b15ed57551a432d3340560bc67d`

```dockerfile
```

-	Layers:
	-	`sha256:151cd86f17661e7d545b869dc904f91fc287c6676b33e49ae72e9870a97da79a`  
		Last Modified: Tue, 17 Mar 2026 18:11:37 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43949a1be44c5a028b6b3fcc19b8ba6c3a7e9a0f13e7a166838a5cb6c64afb0`  
		Last Modified: Tue, 17 Mar 2026 18:11:37 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
