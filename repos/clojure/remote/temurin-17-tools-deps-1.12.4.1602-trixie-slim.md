## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:30165a09701a458b2fa16416056f8dac68095c48c51e26a5dca8e359ff2ef554
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0f6ca230c5681c7fea30c4bd67033335ec45b9f627b9c0b42e48234ad8d91b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246623453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639f449bcc12007c395b7cc16917c2332ff6458b435954ad00c8f8935272ac17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:56 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13751002ea93c7f5d9471794f7c72a340559d518586756f0f8bb47a014eedac7`  
		Last Modified: Tue, 03 Feb 2026 03:21:37 GMT  
		Size: 144.8 MB (144847923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72371970a21f9faa974851298cea88d920bb4f8e329b6f5814d4b737767722d6`  
		Last Modified: Tue, 03 Feb 2026 03:21:35 GMT  
		Size: 72.0 MB (71995891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d921436da1fe01a2eeade94980682fc291c4ade8027b5e681c9cd256dbadba`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a2d44842f4ed358e144c04e683582204bdbc84a73c890539abd28b72783c1`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a6a3ce3f84bab79e1737456b0abe5be8fc12e11b1e2f39e93e25f81ad41d7121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f063048f36d277d4ac297f5d819acc2218da0860924261f75e9dfa4a6785db3`

```dockerfile
```

-	Layers:
	-	`sha256:3c95bc33f14af38988ed0955d57a34b2f6af67ff834b1e07d1d5a08972b6a214`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 5.3 MB (5256299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6328061c634cd3a4214b2962bb0d50b2738e95cd2e0a90d025cdbc21bb48c7f1`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e71b57e7c76c7a9d6b4b3d0bcb34964c944eac7a30399306db1379cbbb74074c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245627505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7312c24de04e27ac6aa692248c7b9708eb8cb9d0ab6927e4fbfbdfc853567188`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:35 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9decbf06df2ed49493df0faa0cb65fbda5284c41076ede3493bc5ab70fa96934`  
		Last Modified: Tue, 03 Feb 2026 03:24:14 GMT  
		Size: 143.7 MB (143679921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3485f74eb68e1d9ddad3b1ae5abe91cd74d9e5cfa4632b27d791e22eb3345c41`  
		Last Modified: Tue, 03 Feb 2026 03:24:13 GMT  
		Size: 71.8 MB (71806478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cec3c89ad5c4d5f40a1cab9bb66681582f38c9dcce6818c93b3f7d6a1f61c42`  
		Last Modified: Tue, 03 Feb 2026 03:24:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b168b6807d88e03b6fa3f8329befd10423fa2e640cbf5a14d9e3f0469820f913`  
		Last Modified: Tue, 03 Feb 2026 03:24:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d5ce921d442918548d266b9efa264e5e9868487935a0a6e282361165b2fce0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a7ba543d245dd2def69b96e29df9ec93336cc83fa1063bf605333bb37b7bed`

```dockerfile
```

-	Layers:
	-	`sha256:7471540fa7322a95bd6355bfd0a108d58ddf0d7c40ec9baea9a49c1a0494701b`  
		Last Modified: Tue, 03 Feb 2026 03:24:10 GMT  
		Size: 5.3 MB (5262068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d27b7e281c24328db5e6305607dd8d98f1cb536cee424cd999b8bf128aa7bca`  
		Last Modified: Tue, 03 Feb 2026 03:24:09 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b072c36a0f752d91f65d56949d138b46c5990c82700c88386eb32f9aa4e1c3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255515915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840416ab3e6334299638d3a1169031848d3aa12694bb9802d95cc836c7ddc3d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:42:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:42:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:42:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:42:28 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:46:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:46:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:46:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:46:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:46:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd3b14e91afb7d1a557cbd0c33d16bb6f700da576b129e4f3f003ca408cae61`  
		Last Modified: Tue, 03 Feb 2026 09:43:53 GMT  
		Size: 144.5 MB (144524725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cc6b5cb097dd0980be8bc47fe4f220f998c3c480bbffa3977430e36966de75`  
		Last Modified: Tue, 03 Feb 2026 09:47:33 GMT  
		Size: 77.4 MB (77389958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579506e12dc34bfead1bb2620e984b7158b037dac974593462871de0f7e11e74`  
		Last Modified: Tue, 03 Feb 2026 09:47:31 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14842c0c8560b9f0de01adad92884221e169b44a27f5b24d55fb8c143fbea9e2`  
		Last Modified: Tue, 03 Feb 2026 09:47:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6a59af507318fb9dcb4e848d917f679c141c590f9cc505c498a09ea87007a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcda30fa180223f17fdf633eec88ba0a64d494cbd7db8f297610ed4cb61a2e6`

```dockerfile
```

-	Layers:
	-	`sha256:a255f35d9d434ddb8d792cb306a78f49911f869032b46f9d3ab2e2f38dd8cd09`  
		Last Modified: Tue, 03 Feb 2026 09:47:32 GMT  
		Size: 5.3 MB (5260670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60769a4c68f6f6baadb525ee0f579de2cf92628137e1691195c9d1d64adddba`  
		Last Modified: Tue, 03 Feb 2026 09:47:31 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:f4ef81d85dbb59413eee11c8bdd711e62f35bd8f407694393f1be0920dccbe78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241046164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c99d33386092315ef16bd54fab740a2facad06929e77b8555103266df68d304`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:21:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:21:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:21:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 20:21:12 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:38:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 20:38:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 20:38:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 20:38:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 20:38:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37b86b79863af50599316c3a3436311cf8411ecea8381a02bba71598ef65c4b`  
		Last Modified: Thu, 05 Feb 2026 20:27:16 GMT  
		Size: 141.9 MB (141889583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bf43e298e4ccd5a7b53a8e400aa6581ce4b153aa423fdd6b95ef78992f7a5e`  
		Last Modified: Thu, 05 Feb 2026 20:41:46 GMT  
		Size: 70.9 MB (70879147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40f623b10483648312fbf51e435c8680b9d3ef7f6e93d379afcbd505549629f`  
		Last Modified: Thu, 05 Feb 2026 20:41:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7bee8f9c1f1f67c14d0800e81f32677d4b81d0a09790fcd610426b3abce540`  
		Last Modified: Thu, 05 Feb 2026 20:41:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6250edd7c7539e0c4abeeb1b0bdce279fb8f81a491b27dcd377f2cc22d8fd432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303e54791f0f617adedbdd8b533a4f84e8b13311bcff76b95ee9a3efbc49f523`

```dockerfile
```

-	Layers:
	-	`sha256:c1ab79426c257edc36fe88492c1bec614f67fa346e470a3e95c5d965ebea2736`  
		Last Modified: Thu, 05 Feb 2026 20:41:36 GMT  
		Size: 5.2 MB (5243844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea98f7dbd0ac6c689edd1d68d4a3438eeb324086fbf8be743e71343ca075740`  
		Last Modified: Thu, 05 Feb 2026 20:41:35 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2fb2ad760c0d164a7f21808dcb461fd6e9e81fb66a7eeb49753c525763ff50e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237651889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f2094ce4e78c1f13383e9a8ff15f58abc5fb91b58d212c6c92fe0c327ec469`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:03:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:03:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:03:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:03:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:03:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:04:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:04:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:04:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:04:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:04:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfbbdfe36872be683d507789f5d9f57b4472fe24b0ff3c3fcff320cbf2dab54`  
		Last Modified: Tue, 03 Feb 2026 05:04:30 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ac5c3b9c02c293325a36a6c76f0643c8ceb48134fbead6bc72a72712efa17e`  
		Last Modified: Tue, 03 Feb 2026 05:04:29 GMT  
		Size: 73.0 MB (72952925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9dfe488758086592fcd6462a057d4fc10ce551c1f73ca666ac1453c9db7b88`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ae76bb7ca089e43d100fa901b51f0f04fc967d3b219a5e9effe5a8d9c3b338`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02b9c0346418cd4f32cbdf2828a77ebdd4fa1173fe5b139eb6fdc1803639b985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2922934d66f72a814683e2305bcb95b2e9708cbad159fd2038e4fc1a4c01d7b2`

```dockerfile
```

-	Layers:
	-	`sha256:d65849885d8c575a421460525686d153bc7c30d5d1e00fe4c856c0091e302348`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 5.3 MB (5252223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922c849c6eed3bd20161705a99987f5c2addc19396b64bf109c70f4b1edf0fb8`  
		Last Modified: Tue, 03 Feb 2026 05:04:27 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
