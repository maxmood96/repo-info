## `clojure:temurin-25-tools-deps-trixie`

```console
$ docker pull clojure@sha256:736db389ceed1537d7a02969f4f55d794f34d1f423722944b2dd537a958d670a
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

### `clojure:temurin-25-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:116c9eb3c2594ab0376fa62320afbf1eaa36558d3bc889c53fcb33c11a0549c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226874977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc48838e88ca1bfb9d4167bcb1ae01e7d59b416f56aa409d0adcc2cc3ead49dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:40:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:40:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:40:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:40:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:40:14 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:40:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:40:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:40:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:40:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:40:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845372137aec38e3d4008df00ea81adf837c8bf4fdf5feb3d4ef5c8fa3c4c2fc`  
		Last Modified: Tue, 13 Jan 2026 03:41:14 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83a73a984e0dbde1e1cb792190391dc92ad5fcf43127fbf0cdc5990d4fd8b97`  
		Last Modified: Tue, 13 Jan 2026 03:41:08 GMT  
		Size: 85.5 MB (85543018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4e4d6e06a932b1221bebf6f457c5fef6d788a7078dbabe56740c9919a54ebd`  
		Last Modified: Tue, 13 Jan 2026 03:41:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe648a394cb5c0c375a6d2fcc10ac8985195d38ddac36c3954d313ec4cadbc`  
		Last Modified: Tue, 13 Jan 2026 03:41:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8dc9c450dbe60f4bc922a20fc9b7ed0a68194be68dcd563aa80c5b9fd36360cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70812a9ecdc5e579696cb6bf69747289c3855fd63dff5d8b5427377d11df44f8`

```dockerfile
```

-	Layers:
	-	`sha256:458e36cc6f12a001b4317dd746a946ad7dc51c7a042bc8391ad45c0eccbf6ee7`  
		Last Modified: Tue, 13 Jan 2026 07:46:49 GMT  
		Size: 7.4 MB (7419156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2661172fdebeb5a39f33132faa64684c8e9e63224b4297b873d9f5059dd47c6b`  
		Last Modified: Tue, 13 Jan 2026 07:46:50 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:67fd35701e485ed8f1f8de80400f46e5cd2484b3ed8ae0989ea9bfa2f64ed806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226062785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769e8704474981ec3505eb859feddfc5f8a4f51fe5183fe6af63de9f9f151e72`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:44:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:44:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:44:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:44:09 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:44:09 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:44:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:44:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:44:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:44:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:44:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2871aab229b6a7d96e1d7d159632f958da71cd10b4f7825ae0f51f284a0d970d`  
		Last Modified: Tue, 13 Jan 2026 03:45:18 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f87cddd41c44eda753d557f9334ce7c2ef047ec238fdfa6a319e7e12319f5a`  
		Last Modified: Tue, 13 Jan 2026 03:45:16 GMT  
		Size: 85.4 MB (85361180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e66faf55ab9f9f2bc12542750da6f28b48c11f76ab9fe78e99046b53dc5c784`  
		Last Modified: Tue, 13 Jan 2026 03:44:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e5924d6a0defa19e3f0d00acc07de0118a22cdb845325fa3c12cac15bc3c56`  
		Last Modified: Tue, 13 Jan 2026 03:44:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2cd8698e4c3bb5d75225fe63449e4543c8db00dea21a3b81eb93756a74c22cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e64acdb2506a926d426fbc40063ebe00ed6b5623b4954d317e6d10a73d4ae`

```dockerfile
```

-	Layers:
	-	`sha256:3f7b0abba4713fa287b24274582299fceda3ea4fddc81fa0b88cac1e5f69ddf0`  
		Last Modified: Tue, 13 Jan 2026 07:46:58 GMT  
		Size: 7.4 MB (7426207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44a6cd55bbb8661ab97894f3773ec3f7b3fbf0ad983e872a8894d0531fd8006`  
		Last Modified: Tue, 13 Jan 2026 07:46:59 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c76078c7fa403786c362c26065e134b18e91a107ddccbd1d0d4b7f02bbfc846d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235665032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1063205c2d8c19fd5bf0f0e89ba0c4dcad982ecb3ad6894cf4364a7b235073c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:29:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:29:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:29:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:29:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:29:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:32:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:32:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:32:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:32:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:32:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b337200b6e61d16776f5501182cfaee70700993bebbb12367907868e271e3`  
		Last Modified: Tue, 30 Dec 2025 05:30:49 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b60e94c27c72e8acf4978d1cf59249b52f71215c6c75e4eff8c221d805b04e6`  
		Last Modified: Tue, 30 Dec 2025 05:33:52 GMT  
		Size: 90.9 MB (90944708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4985330ddf3abea48c8f0cc9a4918e1e1ec5cf3f39d140e52d8dbc0bc17a1`  
		Last Modified: Tue, 30 Dec 2025 05:33:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bd36e438e7305d95daf4994c9eefbb14f68ea5ab8f43ad03204e844f7f21a1`  
		Last Modified: Tue, 30 Dec 2025 05:33:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3f6c27b7c77cab39d9f9d2f26c1df690f43518fd6a85f002320cca317a7634e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c2ca2f3affffb2e950d0d5ea1f70215478c64a41889ecdb83557b23b9ced0f`

```dockerfile
```

-	Layers:
	-	`sha256:0b37192238dbb555bc381193d8f70b26013f9cf11affac94ab7861b59b9cf221`  
		Last Modified: Tue, 30 Dec 2025 07:39:16 GMT  
		Size: 7.4 MB (7423990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398005e9532e74560ce57ae34d8134882524493bdbe93261e7a5fb54eacc8c99`  
		Last Modified: Tue, 30 Dec 2025 07:39:17 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:a6a5d0f98c26e631bb4334e9e880310aeff370d05ad75046e588eec56618680b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222949113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09972d1ef764c77912b88691c0005f4e7633bd4da7b808bfb412094d41ebabb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:24:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:24:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 07:24:27 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:38:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 07:38:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 07:38:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:38:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:38:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e72db194620f93f57207f61aa544e094761861bb8fbdbf65160d1e1594a9c91`  
		Last Modified: Thu, 01 Jan 2026 07:30:30 GMT  
		Size: 90.8 MB (90752893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcbe9fed58bbc38ac063c5ed091bd1d2c011f14d2040d7f23f5f7a00a577204`  
		Last Modified: Thu, 01 Jan 2026 07:43:29 GMT  
		Size: 84.4 MB (84424021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd9e1ebe2c1d294a974e9167b1fcd28f1c864b86822aabe277361a2c2666917`  
		Last Modified: Thu, 01 Jan 2026 07:43:25 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780b6c87508d36f5c3312f1ba3e4f71c54a8ecd9fbe887c563d50a42f6aeb0c8`  
		Last Modified: Thu, 01 Jan 2026 07:43:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5e78f243e2193bd66297be8360ab94345507f179dbbc2530472e6f6c3956c112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed80a35ff71b408c1bb2745a157d2ca33450766546b2b8aa8c579a8a74c3112`

```dockerfile
```

-	Layers:
	-	`sha256:ce769fecab3af4f1003225079c4abca8f41f2510f1f71e1f83922668c9748791`  
		Last Modified: Thu, 01 Jan 2026 10:38:09 GMT  
		Size: 7.4 MB (7406183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749924ae04839adb99dc146b0d9e4a589ff1b416e87fcb8ee21cf5e96ef9d3d6`  
		Last Modified: Thu, 01 Jan 2026 10:38:10 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ce15c1e904ea37a9ed4db8fbe1c323fe4c202cf6a7ad6eab6c8db13bd8101300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224068914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3a49b8878d0ae98bacb5c759699a035cf14b7beeb01e6a36be778b63f75dc2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:09:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:09:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:09:44 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:09:44 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:10:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:10:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:10:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:10:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:10:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06d0c500393ca05f022001c7cac7833a66b1f1a6a14f31278838f427df44b03`  
		Last Modified: Tue, 13 Jan 2026 03:10:43 GMT  
		Size: 88.2 MB (88210715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3604048f55c34c63675a4f9353a95bf1a908c496404c4f11260c68b4b65fb0`  
		Last Modified: Tue, 13 Jan 2026 03:10:42 GMT  
		Size: 86.5 MB (86508454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7654cfcc198df5db2541a8b607c982baaf52d130257de420f6b0ff794cc5ff9d`  
		Last Modified: Tue, 13 Jan 2026 03:10:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc76e1a4184c9abc96703b534f6328253743b2882bfe1baeb9034c5f22979d0`  
		Last Modified: Tue, 13 Jan 2026 03:10:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2eb93dd43ae8bc96436beff9a51dc259d49a83d9b6f22109e1aeceaa20fc5e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f93fe351a96fcc83ea4436529ff21247195db5c02d8d2dfca2d7f30acd969f`

```dockerfile
```

-	Layers:
	-	`sha256:26ab1ca02bb87136f03c17eec15c2155b751caf4f6f01581fe4f2f48deb2bd0e`  
		Last Modified: Tue, 13 Jan 2026 04:41:17 GMT  
		Size: 7.4 MB (7417626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c268c31ce4da6771a09d73f85210cc0d4bb1f3271697cbec63d1ce57bf9ff61`  
		Last Modified: Tue, 13 Jan 2026 04:41:21 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
