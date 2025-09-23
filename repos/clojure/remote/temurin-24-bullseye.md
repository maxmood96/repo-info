## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:e7be9df5119c73e5a85312aef54c47cac0047b4953a3a5b57282b80b417f4306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:62e7930b2d1ebbe2368f3147cd05c07669e26731b3fee0e8601f48b71e908de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213292079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881af4c170f9b5c5955beb6ae9e430998a25240615943d35f944f3554aabe6d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb95f7236c5dfa01adeb05c3702c668f896c5eb07b800aba5be8abd446da64f`  
		Last Modified: Mon, 22 Sep 2025 23:47:18 GMT  
		Size: 90.0 MB (89975193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65bf245b3ec474cfc8ecaf5f9e223be1ea483c89f3f70be4eb115db3d76e604`  
		Last Modified: Mon, 22 Sep 2025 23:47:16 GMT  
		Size: 69.6 MB (69560445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c499a379e4fdb6d601086f2b7a94ab3ce9dd57d3978df18d44833a2f82131636`  
		Last Modified: Mon, 22 Sep 2025 23:47:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934565df5ab98858020e4b42a05155753bdec5e443403f4e54c1b9e67d00c7a4`  
		Last Modified: Mon, 22 Sep 2025 23:47:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e91a2b22baa7d2a285a9ff28ebae4f70dd953163bbdd2d146f9b31e64de9147d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93c3e7590eda8b2124daf17e6c4eba3813b7cb0126bf40c54003db41f808e12`

```dockerfile
```

-	Layers:
	-	`sha256:d978ecdde7c5b25a81b5f2a101b836cf36bad377c05f4a389232854d397cc97d`  
		Last Modified: Tue, 23 Sep 2025 00:44:17 GMT  
		Size: 7.3 MB (7346315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3f7363c07e8b3ad5b33f998ea9891b40881ebe7cbfe2a0673ecc38dcaea54c`  
		Last Modified: Tue, 23 Sep 2025 00:44:18 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a4f1b9740a2ae899aab7ec5ccf261ebe2f0aac629921c94943a1911c54d4d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211029827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd27781f0d21ff9377bb20d6d41f6d6c8ee3c0c4d76b0a6a6f422cb51665db0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9eda5f230686f34b4c05b07994f004033a1b1263a60f548f5d0f5a1319ccc1`  
		Last Modified: Mon, 22 Sep 2025 22:21:08 GMT  
		Size: 89.1 MB (89092539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fb052ffb328e2b78d23122d67d1079de9db52848ffdc85f592feb3256f8d83`  
		Last Modified: Mon, 22 Sep 2025 22:20:44 GMT  
		Size: 69.7 MB (69687876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f301e08be383c1b446785ef87158cc989c897050a93a4131ec1f97ff1cb09d5a`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1338f2374c8141744342612e1ae63558d134a985228acee84eae36268556413a`  
		Last Modified: Mon, 22 Sep 2025 22:20:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fff812daa669e44d1c53afa154e96c77ba3c5922871edb84acfb0cb0b170b8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cec3fd82767a385ed47939bd5896f94c874837ad3822bff6d533704837d5ad6`

```dockerfile
```

-	Layers:
	-	`sha256:980e8e9ec8c4022e178158b46292221cdbbfb28244d40ed6691c7162edc7eed8`  
		Last Modified: Tue, 23 Sep 2025 00:44:25 GMT  
		Size: 7.4 MB (7351411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7196616b07774b260a39d8809da1d48d47b2f5de90ef7c3f5c5dd07fb62471`  
		Last Modified: Tue, 23 Sep 2025 00:44:26 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
