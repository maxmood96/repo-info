## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:75141f5a92034403c766a8d2a02cf78cd571c84db51096e5edd7851ef42f56d0
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

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c272d0f5c8f4dc33d11595fe7fc4f7597f33d8b2bc825b35725d60deb092b89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227448468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a116cee012e1c04f4336ce3984055b8c4efec5769ef115d1a758d0d3b73687`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:53:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:41 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d7392da51aba5ffbce41ac0432d5c3551bd1265450b818597e3ee9a6b6c1c9`  
		Last Modified: Thu, 30 Apr 2026 23:54:21 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d2a385f0ff4a9f990bf7278f76b0b1f65d46aad0ba8e3681518d38ffa05289`  
		Last Modified: Thu, 30 Apr 2026 23:54:21 GMT  
		Size: 85.6 MB (85570727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2319afa28fe6ac0ca2bc0d32fee4e705bf561e7743cf811a6e5c0de75775c7ec`  
		Last Modified: Thu, 30 Apr 2026 23:54:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c88c53ff0155876d8fd1ee9eeedadafb890032999d6175347888c6c4516361`  
		Last Modified: Thu, 30 Apr 2026 23:54:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c17119be3e170db50e212fe3e7e11976923de4995398c8817950c2c365f8dfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730deff11b372e84fd75562b8b58ce7cf2b53ee432435adbee2607d6433bca26`

```dockerfile
```

-	Layers:
	-	`sha256:9bb9cd46815abd6699ea05a8a28c81d98265f27f7dbc1bc9ab17d927e7d98d87`  
		Last Modified: Thu, 30 Apr 2026 23:54:18 GMT  
		Size: 7.4 MB (7439410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6cc7b5ea3d0edf2e60823135c3733965c5d4128aa735f2f09376d22d212910f`  
		Last Modified: Thu, 30 Apr 2026 23:54:17 GMT  
		Size: 16.4 KB (16413 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:caf2bf1314e77f8d523661039ee5cdc0325eebbeb8b34952b5793fc145e0ac75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226596224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfda8b219c1674a4c2b3b5a366300811540b85305c343674ba1444059461a21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:53:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:22 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095815c5f94b82efe420057840d44ba0b7296e0a37626de3e5dfbdffe7cd7b7c`  
		Last Modified: Thu, 30 Apr 2026 23:54:02 GMT  
		Size: 91.5 MB (91542287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be31a2960640b62ea65e888ee0c2363f9b6a34ec7e0cb14c1dcc3f67a220f6`  
		Last Modified: Thu, 30 Apr 2026 23:54:04 GMT  
		Size: 85.4 MB (85383652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5774bfc6ed2555d4939b14de4681c2b92ed635057aa1bd4a6a505c3a29c4fdfa`  
		Last Modified: Thu, 30 Apr 2026 23:54:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9486d286588447efb56d7eec119f5e496c4c9976b2da95085b2eeabeb59d0e8b`  
		Last Modified: Thu, 30 Apr 2026 23:54:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:518265c3cbc81e2d0ac8b6f0186d9ce68b940b5ebf2dc33dedc1498993adeb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7463018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3642b348a6001d2dcc950bbdbba53ef0cf77b0edffc047e94c678c9aa4b08777`

```dockerfile
```

-	Layers:
	-	`sha256:4c131952cdc70533b1117c1f587df2cbcc8d9ff2545670886b2032edc055b586`  
		Last Modified: Thu, 30 Apr 2026 23:54:01 GMT  
		Size: 7.4 MB (7446461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc37320e153d311f5f2dc0480f456fb0112f15fd7a82ec73f6922058f9292ca3`  
		Last Modified: Thu, 30 Apr 2026 23:54:00 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1085606c43d6de3ff0bdca7aeac4b893934e30766c1af06389240f8f78f35ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236024507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4c947881eda5833f9efd655ac0c612203ec72360d7fc812d315a698c28e55b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 00:10:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:10:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:10:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:10:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 00:10:25 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:15:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 00:15:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 00:15:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:15:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:15:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d590980a89e49f373519dea262c7495fd62a199b44a41ded9f5575c826104460`  
		Last Modified: Fri, 01 May 2026 00:11:56 GMT  
		Size: 91.9 MB (91914031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad46ad8ef93162a4b532725d328c9789721e049382ad64d2ee1297780434152`  
		Last Modified: Fri, 01 May 2026 00:15:59 GMT  
		Size: 91.0 MB (90986452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef32b20917b4c8fc567227bfd6d76fa20a40125c53db8c667e7bcf90eb0054a`  
		Last Modified: Fri, 01 May 2026 00:15:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108038d04cdf50032a7951f45429a77bd83208c77f5bf563d8825d6b1459144`  
		Last Modified: Fri, 01 May 2026 00:15:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:04cda502ba387de4987b0e36375fc3f301370f072c1bf943d2252b89c4e7764e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490a4d197e05a2edc0f8155797a9fdef555741699914a25aa7ff62303b2d32da`

```dockerfile
```

-	Layers:
	-	`sha256:3c533f62a0abe2d8574f781cfe3dfaaa21d9c07b0a38f885f490a3e67c4f53dc`  
		Last Modified: Fri, 01 May 2026 00:15:57 GMT  
		Size: 7.4 MB (7427155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c7f5deeacab4862fb2091a188a21ea5125274a1a831f174eeb20c19eb9f945`  
		Last Modified: Fri, 01 May 2026 00:15:57 GMT  
		Size: 16.5 KB (16474 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9a0007e2a153006241a654c4b8ee0c8f88163625680fc7f26f1ef3d13e047ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223274071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934285164367c88eaeb9b8e69b6c785cd8cfe3f852f960064309a5f872e4146c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:11:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:11:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:11:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 01:11:16 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:32:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 01:32:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 01:32:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:32:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:32:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af697d12e7ce2f4ea84af1fb9a0a596fbf93eb7670e91abadfbefd74c762bc67`  
		Last Modified: Fri, 01 May 2026 01:16:52 GMT  
		Size: 91.0 MB (91014936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729740652b4cdbc2e6ee0c940fe6fe37b8ec7989bf2496b18e671869ad050db5`  
		Last Modified: Fri, 01 May 2026 01:36:54 GMT  
		Size: 84.5 MB (84459880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58db505e492a7bb0d48cca60146b61495e9ead3380a725f193a3a4d17d3f432`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e1f66b7ede5991fa02e70eae90c25e30431446b587ea7f4e3275b0607e8f64`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:504a26518932b2148c1bc15b84d3c62114c456887eb6644d891dd497910fee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddfd037d939382667b089d2ba0c82e0bf2e92fc617f4e59ed47dce6c6e1c863`

```dockerfile
```

-	Layers:
	-	`sha256:d8542829608a38f8b3b2340b5acafd7a072fba248a0fb37772a6874d018f47ea`  
		Last Modified: Fri, 01 May 2026 01:36:37 GMT  
		Size: 7.4 MB (7409348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d28545eb03c413f36a2e0b34d5ea5c6809bcd976e29717a20b1c33ad9a48e9`  
		Last Modified: Fri, 01 May 2026 01:36:35 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:9d41f1eeaa0b0b5147dfff3a6cae378d7f80071dc0efce55cc82db999c666cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224338809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38a3767196f9bb8f34e54f6c54efe93be93c9250baa8818e89139044b7af3ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:52:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:52:02 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a52fd9c513687d75c7681b6b507b51cbb775a31cb9520450f2655339d9667`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 88.4 MB (88420322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7fe5abdf2b316901c9363815e16a047c35304a2395c2051e905a8b39185899`  
		Last Modified: Thu, 30 Apr 2026 23:52:57 GMT  
		Size: 86.5 MB (86545343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d635664bf9270565247177e91cfd4adc5d53656740b579aa79012e55d6443a5`  
		Last Modified: Thu, 30 Apr 2026 23:52:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c6a6a0a950ad060be0a0e1bd25ebf6e3e37ba69f8336bbd4b3367106a4acac`  
		Last Modified: Thu, 30 Apr 2026 23:52:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ff7c6debdf8377e6a1d7d6634efd5c9d612cb24fa1ce29dedeb0448885291d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7436309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba5c5bff5a7e12e924ee401f2f764d5afc3d657b7f2091ba338a054c8ab45c8`

```dockerfile
```

-	Layers:
	-	`sha256:ea509f8070156c16aed92f47b2752e918f7c0cf609d05fd2b96c005009ba9c76`  
		Last Modified: Thu, 30 Apr 2026 23:52:55 GMT  
		Size: 7.4 MB (7419894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f595bb38554e5f7425cdf229d48c5e480e0c9057b9a764bdf9b523bc9ea049b4`  
		Last Modified: Thu, 30 Apr 2026 23:52:55 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
