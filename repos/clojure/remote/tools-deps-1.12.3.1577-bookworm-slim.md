## `clojure:tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:eb5254eecb361c6148bdfd6acc052737b7cd2bf7a5367372696ad9d39ef84fb7
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

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:76528070a1b142dc76181256f31c5e680ab78b69addff755bf00f5b5aa30dbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189953968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31d75c98f0b411b6bd86d7b430b189d93a7ab139c39e6616576faeedaf9feb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:56:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:56:21 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:56:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:56:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:36 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dfbc97782bb4ef5510715f43433bb0a8145e3caa8d14c9d55f353cb09197b0`  
		Last Modified: Mon, 08 Dec 2025 23:57:12 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ff4035b2310fa75fb6e03bd68cc610612bf58dbd7602fcee240c843cbd2e3b`  
		Last Modified: Mon, 08 Dec 2025 23:57:07 GMT  
		Size: 69.7 MB (69679221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4630f70a79ee9547f4b0e8164221d09ff3ffca949b4239abf5eab768f9578f`  
		Last Modified: Mon, 08 Dec 2025 23:57:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d115b76beee215a42478f841efb1e902785c9b0aaa5d7cae609fbd2223a005ed`  
		Last Modified: Mon, 08 Dec 2025 23:57:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12d2b1246e08a57bc9dee11fd0c1388218e4ad4e581a29e367848b1f1cc8b7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9561d7e975f8c582bf54d2b6885e08d132627788f42b7e8ca7bc572e02e426`

```dockerfile
```

-	Layers:
	-	`sha256:21317c0ea17705aa27501b16bed9c0e7eef59d239fc3e33335e8a8eb6854600f`  
		Last Modified: Tue, 09 Dec 2025 04:45:41 GMT  
		Size: 5.1 MB (5064748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654aee3ba1cd7ac5e5638cf5c8244f6244712f8f844d7f8d921e9970b0ea69f2`  
		Last Modified: Tue, 09 Dec 2025 04:45:42 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a93ddc6fea8e5497abf14d0bf53f3fa39559c0ddc052bd5395188abb9adb3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188716261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fb2f10a19b802815707e3067efbfaab65851716267859adbe82ca8b2216d0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:03:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:42 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:03:42 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b78a4bf9c76a6a9314447be88b28314f5f3da6c99844402b32067a74715001`  
		Last Modified: Tue, 09 Dec 2025 00:04:41 GMT  
		Size: 91.1 MB (91052516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af82e7cad0b32178b97eb2b2d970ee11b81cb11de4e4eaa3b6d5c7c70a4854cd`  
		Last Modified: Tue, 09 Dec 2025 00:04:35 GMT  
		Size: 69.6 MB (69560478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a36895153194012fb29ad8343a6af9b9c84ff2e355bbd0e40356180d446768`  
		Last Modified: Tue, 09 Dec 2025 00:04:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6a8aace3a59628fe736a99832681abd7898789ef7380d922be0758b26f2e09`  
		Last Modified: Tue, 09 Dec 2025 00:04:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1211fd21b6e41d7d845c0f41c22a560e86d10600ef54ac151d7f593baefa9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e15e14a48bef92b3fe7e2b25908a6df1a0d6538e92ceea13e60e2d04700a178`

```dockerfile
```

-	Layers:
	-	`sha256:89371c524b6a2b7b35113829a7dd107c68bd5ea2fa7d434561507f712c2c3559`  
		Last Modified: Tue, 09 Dec 2025 04:45:47 GMT  
		Size: 5.1 MB (5070530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1f7fc17d254355cf7106da36c6194692069691413a568f9f62a3bfac40cfac`  
		Last Modified: Tue, 09 Dec 2025 04:45:47 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:19e8655b7527854f827e89bc5bc0063268fb41d5a0cbdc35a1256c72f7069795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199193815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d0434de11f18ffad0acf061cf2a7cca2349a5758c080caa966c3ea4651df5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:24:10 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 16:24:11 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 16:26:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 16:26:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 16:26:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 16:26:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 16:26:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34f3bc4e2e28ed95aba8ec4d91b1f2ea595dcea02126d32ce2f47b884268f0`  
		Last Modified: Tue, 09 Dec 2025 16:25:49 GMT  
		Size: 91.6 MB (91610770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758c758ef5922cbfe1a6121e160d9d3e703735c7af5deb17809cd6642312a45c`  
		Last Modified: Tue, 09 Dec 2025 16:27:55 GMT  
		Size: 75.5 MB (75513157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7afb6ee045afce2557dd9dc26019054191898e262138f9e317cc0be32dc720e`  
		Last Modified: Tue, 09 Dec 2025 16:27:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2328d72e76a9aea7f3f38961423a4fc374ab635bfbb5c6cb43951c69e8baa2b`  
		Last Modified: Tue, 09 Dec 2025 16:27:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c27415dc9721a14c34f93e1140d135e0412e5d2b1881a0bdbe7f7f3e11be7b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6afe6478dba8348bc1efa150aca8b5a8cab05c5efc8873b0ad63f8c9e86f088`

```dockerfile
```

-	Layers:
	-	`sha256:b6bc6b4cf658652748695f861d668b91364bdc5210f3a3f02a61df8fc0bee450`  
		Last Modified: Tue, 09 Dec 2025 19:37:20 GMT  
		Size: 5.1 MB (5071216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8e008d494ba7ee882eb3fa5fe3ce0ea21d61a75aef2471e0276216454157d3`  
		Last Modified: Tue, 09 Dec 2025 19:37:21 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c9bc5acd6caa66a1c19bcd36e6e72f440513c715b3e8dde5d3ca146cad0b0615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183587035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a104ef7292428d9dcfdc5cca26cdd0d782b2070a94c3372a7f5483aa475242`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:33:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:33:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:33:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:33:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:33:07 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:34:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:34:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:34:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:34:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:34:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709c0e13614b718d0c3c4ac64648d2daf3ff575c31cced0f8f9a4e0d7b37e36`  
		Last Modified: Tue, 09 Dec 2025 01:33:55 GMT  
		Size: 88.2 MB (88210730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c0e6f6ffe4bbcd7aadcaba1f2bc634c342e89f1feb71bc411c4065df03c85`  
		Last Modified: Tue, 09 Dec 2025 01:34:53 GMT  
		Size: 68.5 MB (68490840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eb3b560f252a440e33bdcdbad2290f51cc76a0505127def456748f78adb60b`  
		Last Modified: Tue, 09 Dec 2025 01:34:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c2f861230f6e1a80c377adcc681c1ac82af3209def1889165b876dff6d57c`  
		Last Modified: Tue, 09 Dec 2025 01:34:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3f538f16da123528d9b5f02264b7e1ae1cbdd605192ae6c15d00323de2d17bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5241c85cb6e6bb894d338e637a81d3cc564388e1baade1c6b77b4f1283310e2f`

```dockerfile
```

-	Layers:
	-	`sha256:1b4cf6763e1290f10072d0380ad3377b9ddd6ea4926b7a8cc9d11b7f9cc724d1`  
		Last Modified: Tue, 09 Dec 2025 04:45:56 GMT  
		Size: 5.1 MB (5058617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b186915e4b32de4c6ed076c0c4408868aa4b76dcbc26c4ce250a01dc110920b`  
		Last Modified: Tue, 09 Dec 2025 04:45:57 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
