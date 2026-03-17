## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:6faaace4b25233564ed48cdecab7083e58855c3f4889402e6e5d240a55ae894c
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a3b51e9341266105adb2fb8bd9f4cbc8a4bcade40b385a51f279e17dd228886d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247595439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c344b7dc2cdf93f5015c7354af472207d9521bcc84dfdf13a5a21d0ce0c20d8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:57:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:38 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5608634c2935e7934356895f3ae794066fea3be535b1554ce591d6ed30e4a39`  
		Last Modified: Tue, 17 Mar 2026 02:58:21 GMT  
		Size: 145.8 MB (145806912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02bd53ce531ca11e2f6b1038a0382ea138588cfb536930f9526431f1b61be1`  
		Last Modified: Tue, 17 Mar 2026 02:58:19 GMT  
		Size: 72.0 MB (72012383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874976330358fb05bb3ae2aacb1423247ccb1886c2c884e7ea8a58bc391edb52`  
		Last Modified: Tue, 17 Mar 2026 02:58:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f54b1331c15ebbad94a99a61af146b9e763455038bd2fe014dfe68180cc130c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bf0454f92c786aaea5dec9331ace8f4f0a86d9e7b74c9089054531f047fe9b`

```dockerfile
```

-	Layers:
	-	`sha256:af930f28cb786f2e86bc22fe366a611c3f348e7b71060f4875fbdc6f519bb303`  
		Last Modified: Tue, 17 Mar 2026 02:58:17 GMT  
		Size: 5.3 MB (5279279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fcbd386018aa65c9653ca08082b06f0d4342c260855249d429fc07d2057a2`  
		Last Modified: Tue, 17 Mar 2026 02:58:17 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:064d45e3124b2665a962be7c6f5e9561173f0660796e99de34aa40691479ab46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244470463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea7f1bdb0b4abfa77d3bf0421ddd6c76dfe48cee729951851084ea0cf3c2285`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:02:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:02:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:02:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:02:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:02:10 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:02:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:02:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c163612247ce9fd6f679f0c5dc6a860a98a193594087bd66b1c30e5840a5346`  
		Last Modified: Tue, 17 Mar 2026 03:02:55 GMT  
		Size: 142.5 MB (142500051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49927905650ab5f9dde5dde2a7dbc3eb7c11374575a3a5d09d18e67a61a5797`  
		Last Modified: Tue, 17 Mar 2026 03:02:52 GMT  
		Size: 71.8 MB (71831353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0e4347d0b09d6ecd09d8b5ce6875afde466916ea030365fd04751ac8f2b429`  
		Last Modified: Tue, 17 Mar 2026 03:02:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fdf800debdf41a171fad4e9581dbe7dbb14b67db60c66a1eb00fc20cb669e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ecc2291b725f771ddebfec965d519985aa7bea2836b2d429f012d9c51fc5b6`

```dockerfile
```

-	Layers:
	-	`sha256:1d5f5c3536f2b29eea84d4eb1f1aa70a3f1d691765b1b1768fcf37cb69840c05`  
		Last Modified: Tue, 17 Mar 2026 03:02:50 GMT  
		Size: 5.3 MB (5285666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055fe0812e8d4f8c32e0592241c750c7ea2054e10818197b43ceae4f4e606a0c`  
		Last Modified: Tue, 17 Mar 2026 03:02:49 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:80d936e6797cdde11df071306170fd0883a1f6a01e2437c2a902ba54e539b5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244027115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa6b07c9ccd74f65d9b1fd61ad0b6f26758c30091eae50d0dcb519e4c439b1d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:49:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:49:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:49:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:49:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:49:21 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:50:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:50:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:50:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0084ef3d4f785d8eed77e52e9b5c15bf9f044cf226f4f0f68abe64aa254ff1d3`  
		Last Modified: Mon, 09 Mar 2026 20:51:02 GMT  
		Size: 133.0 MB (132997823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bcadb16aaea6fa97d2247e88050e85658ecd962ae101b5d66046c14858eaaf`  
		Last Modified: Mon, 09 Mar 2026 20:51:01 GMT  
		Size: 77.4 MB (77428429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2ddd2dec7dfeae62af943793b99fb93af9651dd7190dd2434e943145f0269d`  
		Last Modified: Mon, 09 Mar 2026 20:50:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22189bbb021a548295bd552fa7cbf354402266d013dbf3bdd7c5b5b6de5515ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b166e3c5c84c260998c151ce28aa84a1d7a9ba16be2e044a571c4c42b78f6`

```dockerfile
```

-	Layers:
	-	`sha256:970439528749cbdd44811c3e6cc704e0556d932167a78f5083f33617d1cd4b39`  
		Last Modified: Mon, 09 Mar 2026 20:50:58 GMT  
		Size: 5.3 MB (5282961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbe9ca8a72baf4a6023771995092970dbeeeb31c074b26a07dcfd0b045fa2076`  
		Last Modified: Mon, 09 Mar 2026 20:50:57 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:20a826361d5d623d7b571d3d6f66b62304cc7c7cbbb5b827a7bac8e1d2239a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229384585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffc3a997e79d67072480ce91a2bf21620aebf3490149ca0fecfab48f0868f92`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:26 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f09f9a8868680d395a30962c68bac28d9405a659030c5d0f5c217028209b0db`  
		Last Modified: Mon, 09 Mar 2026 20:34:13 GMT  
		Size: 126.6 MB (126562037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b3c2d48ac51eb278695fc95b1e83fe5700e4c6803159eb52161e92b034ef0a`  
		Last Modified: Mon, 09 Mar 2026 20:34:12 GMT  
		Size: 73.0 MB (72983722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd2c7cc833e919ddb9a61a390588d271c1620f4b922b62d5fa3398b513d5c58`  
		Last Modified: Mon, 09 Mar 2026 20:34:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87c2eba0fcaf81101f9ba5d6ec506517a54df82abbde6ce967d615d6797409ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392e83d6493e6080bcad7c2c22ef0256e263177837b0328a88feb6c87aa85a4f`

```dockerfile
```

-	Layers:
	-	`sha256:1136c9ee30d1b82688e652bfe9a1b4dfbe15332f2968b771491d862332aa4bd6`  
		Last Modified: Mon, 09 Mar 2026 20:34:10 GMT  
		Size: 5.3 MB (5275133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e09333d939e277b631a579deb5226f73d34d3dae86a0fe6fc6e3194353b790`  
		Last Modified: Mon, 09 Mar 2026 20:34:10 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
