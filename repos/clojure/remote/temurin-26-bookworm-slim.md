## `clojure:temurin-26-bookworm-slim`

```console
$ docker pull clojure@sha256:b4fb035a722a12b374a9cf78f72f0c4a993f10f2cf053ff34953fea17a4ad9f5
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

### `clojure:temurin-26-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ab0f88c8f5f80e3fb3a802c553f89ddf24125a6e1adb5cfdf7d97573cd40b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189405610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5c999ad1d6f8b19a332254602b70332b51696531675f5267afce0f0c81d01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:22:59 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249017cab6d102120d4d5164f20f817b1b6e2059c2499ed61dce0a7efb4e4570`  
		Last Modified: Wed, 24 Jun 2026 02:23:38 GMT  
		Size: 94.5 MB (94524361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f7f79511f7943b41761f32fba502111ebb48ef38ef344a964e6792ef7e90d5`  
		Last Modified: Wed, 24 Jun 2026 02:23:38 GMT  
		Size: 66.6 MB (66642566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16124959d385863449af4e385e3d1062739899afc9fcfef28849cec1fd6e72a5`  
		Last Modified: Wed, 24 Jun 2026 02:23:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497e97b7ba48d25783d005453a6041b9a7c9eea9b0f75719b04f55aabe6e7eb2`  
		Last Modified: Wed, 24 Jun 2026 02:23:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd29d931fd66c66878afb3b724300478607691f19de47517b54dc277a65959ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f551d4cda47ff6a965c974e7ed5d70e44522a9bbbd1891e840640a9b6d3acc4`

```dockerfile
```

-	Layers:
	-	`sha256:8b8d50141d5e1e065d4259f9eb8445f044e991546c1ce1aad3351301a3055361`  
		Last Modified: Wed, 24 Jun 2026 02:23:35 GMT  
		Size: 5.1 MB (5078890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ffad86afa32215b665c3e4326ce76b613a433b3742cc819e61b9b9e6eab0ae`  
		Last Modified: Wed, 24 Jun 2026 02:23:34 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a1dba50a583b62e01489ac8c9bb708a9ad4af594ba5a4a74535ef1483c70a5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188271024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a20ab1b09eb7657d8895ceb34fe6d2abbacc34e820b189314d6c5dc82b3bff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:29:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:29:39 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:29:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:29:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:29:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:29:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:29:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3305929a5aa38554afe5dbed785af2936cbd19e2130391eb80909bf6f85a965`  
		Last Modified: Wed, 24 Jun 2026 02:30:16 GMT  
		Size: 93.5 MB (93504335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a07293f44d595d86a2f742a6e96b3f485342e198e0dcbe12d242531d7cb6ec`  
		Last Modified: Wed, 24 Jun 2026 02:30:16 GMT  
		Size: 66.6 MB (66643230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62ee1ae2967afb68ec50643dfc759269832584221d85fc4c01fb850c39cd4a`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2091bffd0c310c07b61cf4f3f6c98d7d264f05f1c5edb7dabd401401557c464a`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:020b407a335f3883a917c1c96022fd860746ff207da6dc90535be9b5e05b772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4fb705ef509dca246dcfcbd31c943e3a1aab595e0e6813d0a1ab3f52153a85`

```dockerfile
```

-	Layers:
	-	`sha256:7ac8568e6127704e16f89b5f74f690f69936df42c988c2e224f489945e989b25`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 5.1 MB (5084648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e84bbef77f0cfd902da42d15802742f65224d2ca30bc65c5deb48c51e41edfee`  
		Last Modified: Wed, 24 Jun 2026 02:30:13 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:eb78d16b427fd0451b7fbd9c56af90f74a46d658057268d7e727ea6d497bf54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198461296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5ecd9cbac51729f5f7f85e01c0f1cf06f74f35df6713a24803449ae524f09b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:10:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:10:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:10:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:10:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:10:18 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 03:00:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 03:00:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f29b00e9bc0b9af92e1b64e13edf9ecde1571af48c5d8d0fce068fb62ea3514`  
		Last Modified: Wed, 17 Jun 2026 00:13:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08e2bae7d64244f7ca140327e02f1900cbf17e7ae9cfe6f3a602b4dba3c77d`  
		Last Modified: Fri, 19 Jun 2026 03:00:58 GMT  
		Size: 72.5 MB (72476233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3853afc64ac098a49454f9bfa5cbafbfc6152cdfbdea9912c1233ec1aba3b9d5`  
		Last Modified: Fri, 19 Jun 2026 03:00:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b810f7f241f7891842f13067f6a91e0eb15c5e00c219dd5f5c713dbefa18b91`  
		Last Modified: Fri, 19 Jun 2026 03:00:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b41e8402ac754efb90d2305cd74455e0f250d683a4fa13c475c7f694495f2aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a06e67759dab66f884756c9ab72f60c7489aa3b4f617a9a5322ee49d18bd6b3`

```dockerfile
```

-	Layers:
	-	`sha256:1dd32dcf94a3ed28da62c5460e64fce3e9a41edddfce650ba5fe6d5bf71f0f26`  
		Last Modified: Fri, 19 Jun 2026 03:00:56 GMT  
		Size: 5.1 MB (5067984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb8964dc5b3490056c358769448650eee63574f4359879624bea7c476b44cc0`  
		Last Modified: Fri, 19 Jun 2026 03:00:56 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:561e84368748078612ebde78836c0e3f499c5369a06fea8a0cbed63f377e4a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182883593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd230768a748bf861dededa89a79d988a233487163999f284f7d5c8a2b056c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:41:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:41:38 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:24:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:24:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:24:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:24:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:24:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf175e00b02ff27e4e23a84cea45ce5d6e96921b94bae771e56baf106f5ca05d`  
		Last Modified: Tue, 16 Jun 2026 23:43:12 GMT  
		Size: 90.5 MB (90536986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a02278344e3ae963ee27ae0fa98d25c697da9b7a5c3d68ef0e55a8b60001621`  
		Last Modified: Fri, 19 Jun 2026 02:24:46 GMT  
		Size: 65.5 MB (65452059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8983bf23a270885ecbfe5052e5a93bfcfe134f1c86589ac89640dbdfddf636`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67fa011f886fe2fcec3d7871f3c0592613e1dfd8d7a357bfbee4b2dd2da97f`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d8f45163ad8299a3ed0ea46870471108f0982c661d5f6c7ff25fe27f05fb6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dac28fd8d248b4928c34cd81b4e424c911edff5e3dff603a70cb24fc6383fb`

```dockerfile
```

-	Layers:
	-	`sha256:75fac332319857cb9cb7dac338f8b41bf2e8d72344ebe4a9e03f309d9194e395`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 5.1 MB (5055397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2132e1b5e39b63e74de1a77bfdfeb01093bf8191fad5899f11ec666d69e669fc`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json
