## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:b2ea05b189a811cb2d1a6467ed49987dbc2b4a9eeeac10cdb733e89ceeba5ba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e14520a70418df3a52b020aee8a31df41dfb6a7f8a5d398d594b33832a2bbae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189557722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b294e7e99abaf2def4ad8b0fa6483d94711119643799cc9a1cbb7cfb2944a21`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:29:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:29:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:29:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:58 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:29:58 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:30:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:30:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83451a89c64b14e75322f691f6056a80a5cf375e95e456fe2d70d8c7b202a02e`  
		Last Modified: Tue, 04 Nov 2025 04:30:47 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31954aeea07a175af8c2ec530092cc7e761fbc2e4e7c86681d23d1a5ac83724`  
		Last Modified: Tue, 04 Nov 2025 04:30:45 GMT  
		Size: 85.5 MB (85540158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfd4cb917783fcb67f55514a9920462d5b6f2de93da5e91fc2ae0dc8e2cb9f3`  
		Last Modified: Tue, 04 Nov 2025 04:30:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d65d42bf8f629e7b029e652ada9feac56f8b7edf839384af0a2e695b7186222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d177114a564ebfe59694b92b1e1420a20ed1b13000b22754841337ae5fbb51d5`

```dockerfile
```

-	Layers:
	-	`sha256:865c27abc3e35ceb6c99c2763f1d4768cfed36bcb3671065d7d4be6887d94199`  
		Last Modified: Tue, 04 Nov 2025 10:49:28 GMT  
		Size: 7.6 MB (7588509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d445f56b6ca8341f7167b27642a75e8d561a6775ce40fa0aba4bad5ecb019f01`  
		Last Modified: Tue, 04 Nov 2025 10:49:28 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a9546d50fba44892d2a6ee68b93f0110e1df6563a0f7c44c1725d2ca2101550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188850032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb51239120d662a40832868de1b8e2ea5ba6997cb9e2d57ee623562fe1db1dc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:43:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:43:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:43:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:43:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:43:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012cfff097586e0e345ff08545d54aad49cc1b7405c28acf74e13ba2aaef1ae4`  
		Last Modified: Tue, 04 Nov 2025 01:44:30 GMT  
		Size: 53.8 MB (53835630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962512242c36d05b976e7935ee3b00d7c13cecae688d52a1cb2a2782620b7bf8`  
		Last Modified: Tue, 04 Nov 2025 01:44:37 GMT  
		Size: 85.4 MB (85363328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fd133bdd3678529d87d6a792f4bc5e963808d20e45bff3b5559a209bde056a`  
		Last Modified: Tue, 04 Nov 2025 01:44:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dfba9379c0c33d6d3ded3d5c255d214319b8b73edb57ca48fb6fbc274688111a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c4b26e34b89c4b1e4aaab838263cb47da95178529a6cd16ca14f3db6a7f170`

```dockerfile
```

-	Layers:
	-	`sha256:98404a2ac06423d2185f9b199a7a732e2c31342e18bbc9e7a3c2ce22965014e4`  
		Last Modified: Tue, 04 Nov 2025 10:49:34 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db03c94b2430d7dd10647320724b3ad679de0efec9a56bf822389c5040bca8d8`  
		Last Modified: Tue, 04 Nov 2025 10:49:35 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d78e73a24ad5b252dd24bb999e80de24c6ef39dcaf18f5d2c823e5873fb08adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196224552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec46cb8776949cf290b777e1ba1b94977aa0e1f56daf1f8041c87e3663e3255f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdbe0b60fe16dbc11b505a333d9eca1bab3f0320dc1c61278729bec87a034af`  
		Last Modified: Tue, 21 Oct 2025 15:23:23 GMT  
		Size: 52.2 MB (52165398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135d62fabcf368ee8f6ad1c6330f38937978b0e3ae8cd36ea6a5125be58e1df`  
		Last Modified: Tue, 21 Oct 2025 15:30:07 GMT  
		Size: 90.9 MB (90949035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379db0b40c455fe6e8553bd3c86584973d8e41be1668249d1defa28bed760c6f`  
		Last Modified: Tue, 21 Oct 2025 15:29:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5bba7dd7d34a38bc32155f4bde511f60d25d602197ed23c94d4b4758640b78e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97915d177720fcdc765d21f9d50c0e1078dacb00b2f0b1faec19465dede5906e`

```dockerfile
```

-	Layers:
	-	`sha256:5e6c9fed0e5bc42128691a47a41a892c8150d917f71db99dd13d6fa7952b231f`  
		Last Modified: Tue, 21 Oct 2025 18:43:02 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5dace573a3d66e918c9b9cc0e686c240660138ba876c3c59726167e22901e9`  
		Last Modified: Tue, 21 Oct 2025 18:43:03 GMT  
		Size: 14.3 KB (14260 bytes)  
		MIME: application/vnd.in-toto+json
