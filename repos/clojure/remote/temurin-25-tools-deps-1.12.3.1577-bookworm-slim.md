## `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:8456b80f98ebb699168b96fcb2b57730efee4d27d3c2b8ae64f792fa3618b052
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3fb8101cb9ff2ee530ac77e7fcb28da7afeca92bd8cd9d6fae0f4fdb8144fb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199193869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7e568e4daa2a9d2c1e28c88b4f0703a318ba8860de50e24c50d00b9f48ed08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:40:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:40:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:40:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:40:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:40:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:43:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:43:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:43:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:43:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:43:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a439639461396cfe319eb84b16332b2671db8af4803837382350f840521b8ddd`  
		Last Modified: Tue, 18 Nov 2025 06:41:34 GMT  
		Size: 91.6 MB (91610763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443affb70f9ad5de78806a9bbd7d65fc5464c435aa60f4d78c669a8f99cd80c`  
		Last Modified: Tue, 18 Nov 2025 06:44:47 GMT  
		Size: 75.5 MB (75513240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccbe88b9f8129cbfdf4ef5c2871a4e795b9ccf04147f87e8ab936b9e7ba7860`  
		Last Modified: Tue, 18 Nov 2025 06:44:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b3657fb80852294249e4af0f42d25fa2929d0caf2a303b49b3f09ba84f3a9f`  
		Last Modified: Tue, 18 Nov 2025 06:44:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:934fb99fd9e155648ef379a8b462d4a5c6dfc68dc510da9cd1411ec286a33c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743a47cd1ebbdd8fe4ec0001dc8ddb42bfc6211eaae6e48e6f34bda687d8ef8b`

```dockerfile
```

-	Layers:
	-	`sha256:d15c8603f35321d8a3757ffb9676648bfff966ba9889c1f1d5b0d38b21852536`  
		Last Modified: Tue, 18 Nov 2025 07:47:25 GMT  
		Size: 5.1 MB (5071216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211a5896f075d9b41ee9be2e4a5f34b162103ca2f45db2f5789ad48715ffdf14`  
		Last Modified: Tue, 18 Nov 2025 07:47:26 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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
