## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:00e0ad25872e23e655f5414865b68398cde44e7395444ed497b66a11e8adb98c
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d4a13791741e755532d57e3483ca4222f7db210c3bd596330019be8e8720c50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279521398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb96915fac1cca4ab3fbcbf23168fe059376e62c023079b8cb0fe013e2e0770`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de186dc5db30d54fa39ad3ce7c7b448e4ac57f61ffa5c3e7640f82cd1aeeadd4`  
		Last Modified: Wed, 01 Oct 2025 16:10:58 GMT  
		Size: 144.7 MB (144693598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d9fccec4ee8e8f3d9b0fb4a10442310e774e50bb40304afce61eedb155d005`  
		Last Modified: Tue, 30 Sep 2025 00:54:42 GMT  
		Size: 85.5 MB (85542137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd8623692287be5ff98f6a5349b759412c89c978e8eb9dc79c480bfe44815c0`  
		Last Modified: Tue, 30 Sep 2025 00:54:32 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f330efb5d5991f34dd42bd6843c5d94343936aa21df148f40e8e8e42252b38`  
		Last Modified: Tue, 30 Sep 2025 00:54:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:06504dabbb22ca0b6f6ebf067a2569c0708305ad5be24ccf3acd8e7331451826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404fb22bec9979e4adf6ec94dcef141b8c9ae37ab1072bd2681564cb5b237237`

```dockerfile
```

-	Layers:
	-	`sha256:447526989b87d2af6a6f90b6405e911ab4fe067e5f8c07711e3f814d5f3a703a`  
		Last Modified: Wed, 01 Oct 2025 15:38:51 GMT  
		Size: 7.5 MB (7466845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9429a77c02e57a81e2aead4e6716866aeb032fa5699dc44125a06d4e2156418f`  
		Last Modified: Wed, 01 Oct 2025 15:38:52 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3abac3883d147cd2404b78e8549744084b4980033843f532e837229d03aceb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278550182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de2055b1bfbf9c2b7433ec411baad2b956aaa613a42fd222635fc24e8c869ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5739b0baed1d4f52f2b61dcfe062faefbff2f425eff584d153f43db39dd7dac`  
		Last Modified: Sat, 27 Sep 2025 01:56:38 GMT  
		Size: 143.5 MB (143542145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ccb6f95b9bec6654fdb4df437a43f1947cd06b6be9d7250203f16cf60054b9`  
		Last Modified: Fri, 26 Sep 2025 17:55:38 GMT  
		Size: 85.4 MB (85363248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d964f913b12520c8d9365200fe331f280478418d1e5d4bfc186c096defe604d`  
		Last Modified: Fri, 26 Sep 2025 17:55:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffb55dc96689fd5913b91e08104eb1f25c13c17b7696395df38697ca893e444`  
		Last Modified: Fri, 26 Sep 2025 17:55:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bac0ae516e27ac2ddbeb767b94c0e13d7853da69d322cf6cb29b859e8d7ac0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b75b5e1b6b8d2408e0396e2e0f6eb100f15dfb4a476f53924f6bcc90554cdd4`

```dockerfile
```

-	Layers:
	-	`sha256:4579360f8d9d52f97d27a700d65fb2698078a8d126da5c4a7ce4b1aaa7cca3a2`  
		Last Modified: Fri, 26 Sep 2025 18:40:15 GMT  
		Size: 7.5 MB (7473875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25420c3b9c28461e0785b6fc76c6f3762e71e4b9fb79b1c18bbeb66d7e198e46`  
		Last Modified: Fri, 26 Sep 2025 18:40:16 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9f92064a80ad0b228f53cc354afa6f659f86dfe7c541cc8d5901133a7efbaaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288426884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4ab664acd521f3399fd2d1ae68879eef96450cd236348d152f899331622ff4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb54706f2f05927428a0041fcedc3117382ccc66142d8f70433a114755ebe3cd`  
		Last Modified: Sat, 27 Sep 2025 20:04:42 GMT  
		Size: 144.4 MB (144372805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22397f7b088cf78e5930187a293893cc4cdaba8d29447c16e9f9df47126ea5f`  
		Last Modified: Fri, 26 Sep 2025 18:19:26 GMT  
		Size: 90.9 MB (90948602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260d61e91d526d952cbe1416532d1efc1577a65574153cb8dd0c2d4b5493451`  
		Last Modified: Fri, 26 Sep 2025 18:19:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5806aafe89117a61cddcd7ac9e93006e596385e625e7d826b453272b34b80349`  
		Last Modified: Fri, 26 Sep 2025 18:19:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa527e1ab7c940e7311264db9d36c34e4faad5c0bea3434beccc8cf6076665a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35009989c4fcb0a7d610f6f5211617fd8eaee61e78227be206e8bb849dd34bea`

```dockerfile
```

-	Layers:
	-	`sha256:39e4dc3d8edf6f48e013ea07e727d67e6932cd7fa68c141a7dfa59c1651177eb`  
		Last Modified: Fri, 26 Sep 2025 21:38:15 GMT  
		Size: 7.5 MB (7471264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66605a02f8868888cdd577a473f6f49227d40da303143851abf52c1e0e7075b5`  
		Last Modified: Fri, 26 Sep 2025 21:38:16 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9bef743fe826cb5bcb13d748e5d0cbf6a40528600ab1f0dec963ae10fc6c1278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270769519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7dabbfba138a493d060fdd1ba681d7f3d6dd39c9f1764af79175266e281a5b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ae21fa5b4d30371a66ca687e7c73e5de6887104c1d0ede9bca919214a08b0`  
		Last Modified: Thu, 18 Sep 2025 19:48:28 GMT  
		Size: 138.6 MB (138575662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75f3c1334ec9f5f2fd36b054d78ebc20154407af3e5f7d2d694d051b451cb90`  
		Last Modified: Sat, 27 Sep 2025 00:08:18 GMT  
		Size: 84.4 MB (84427371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc550d8cc9780fceb69b83065ad0643609f80310df572d392679e711672e617f`  
		Last Modified: Sat, 27 Sep 2025 00:08:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa7381e608293db80205c25fa3a086d8b9613bcc5bddfbb12262ef50b5f912`  
		Last Modified: Sat, 27 Sep 2025 00:08:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:878a81d52588ddd33519f1ea681d295c39d8d30a11b18afda8870c983439b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25855f9b085ff99342363ded60e25af798b7b906755f8cda680dd7c976be13da`

```dockerfile
```

-	Layers:
	-	`sha256:b9139750f527c5e80450cef0e47808390171aa75940a4c8fa6cf344640d58876`  
		Last Modified: Sat, 27 Sep 2025 03:35:44 GMT  
		Size: 7.5 MB (7452839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aef6cfcf647a05cbc192a7d513e9d1d0d9e2469118a02046e61c08a131b7995`  
		Last Modified: Sat, 27 Sep 2025 03:35:45 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1035fe4134fc5fb38d885019f1cb64cf3131ccd97a017b197f2f03f9783b7147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270577923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f161099abc1f024c2220c302d700b4caf09241c4394ffe20aea9837840e9c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a580b36c32962de0d4a859f955eb77bff1d748801c1852b551cdd808e428e`  
		Last Modified: Sat, 27 Sep 2025 20:14:19 GMT  
		Size: 134.7 MB (134724318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0a703b63cbac660fcf6df7ac3fa17cb8315ffd9053e7db66fa91e7726a3587`  
		Last Modified: Fri, 26 Sep 2025 19:20:19 GMT  
		Size: 86.5 MB (86506234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b703442339581249aa05c619597912e97b6f5d1aeb964d655865b0efc1db7197`  
		Last Modified: Fri, 26 Sep 2025 19:20:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6e4d1aadae55ac9b07892745d30055461becf0905f62ff0195d31d5cdf20b2`  
		Last Modified: Fri, 26 Sep 2025 19:20:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ffe0643d252c235ed606d8de9474c50fd1e4180a1011f0790d1c12eb0050502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4cb477b97f39678ef851b67b8c68e583473f9811cd6ebfcb89ebaec410a0b9`

```dockerfile
```

-	Layers:
	-	`sha256:dada3f1956cc1cd02a95a90946ffa1347b816d2f2c7206abb327c94f9bf1197c`  
		Last Modified: Fri, 26 Sep 2025 21:38:21 GMT  
		Size: 7.5 MB (7462767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31c7851b13527918a17fdd91fce57ad60cb705b2264b19b716bee388214042b`  
		Last Modified: Fri, 26 Sep 2025 21:38:22 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
