## `clojure:temurin-26-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:473fd03516276ec06a87cd157044cfa219d89be5e0cd6f634c0a9b538e35d5ed
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

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ac8915dbeef990f6c700220343d8779e2cb9cedc77b07569795cdcadc302e447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198461221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f62165de1d81491cda733a930adc25ad2116ca1bed711c54b6a0f3a4993102a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:30:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:30:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:30:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:30:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:30:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:38:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:38:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:38:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:38:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:38:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47667e33496618029b3928bbbeb951a3aac0dde70f2241e954b57318292c76ba`  
		Last Modified: Wed, 24 Jun 2026 08:34:15 GMT  
		Size: 93.9 MB (93902051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a811283b6cafb6268a86db0e68446d1319a07ec906a3f96ebfdec3df72caec6`  
		Last Modified: Wed, 24 Jun 2026 08:39:19 GMT  
		Size: 72.5 MB (72476151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a924959d08285e2acdea26f89a5b4a9c266a46ecb9df706b1dfcb9c054ce8041`  
		Last Modified: Wed, 24 Jun 2026 08:39:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e555d9cb74b291ffe446ca05a3f0e4e4a734e97fda2ae8dcca1b56f640e52e8`  
		Last Modified: Wed, 24 Jun 2026 08:39:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a21e9ee422abfcc2fe5591c6ddaa1aa5bad112ddfb8f6b913038e0399002604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44126aa42976c9ef9992504a4b546a11416634841eaa4e9baacd0cdfab2723b1`

```dockerfile
```

-	Layers:
	-	`sha256:ada8b9feef5ccf635aac9a6479a73b5ace8e540dfb8ebadd60284d5cd08f79c2`  
		Last Modified: Wed, 24 Jun 2026 08:39:17 GMT  
		Size: 5.1 MB (5067984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8980c91e73be017606e0c4f8a86d74e86095385daa47dbfb782d5232b5b79b9b`  
		Last Modified: Wed, 24 Jun 2026 08:39:16 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:aa44277e866f41d11b5470c31eff90827066666a7766cb7671612030a6604093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182883751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba612f87572bf8af1745f782ef9dc61d21a421f31978f3cf622d24807dc4724`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:19:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:19:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:19:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:19:36 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:21:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:21:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:21:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:21:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:21:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34db396c791848b69e7c26c38ce79f42e22c2f325a414bab3309ac2f2c84ba38`  
		Last Modified: Wed, 24 Jun 2026 04:21:13 GMT  
		Size: 90.5 MB (90536980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79634eaf7d6e008b5513a94d628f9c0d1dc787923dbdb82e20a3bad47ae115d3`  
		Last Modified: Wed, 24 Jun 2026 04:22:07 GMT  
		Size: 65.5 MB (65452147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33c8e107df4845f9bd7cefacbe388279729be92e2f9e5f7245393c7b0804ae6`  
		Last Modified: Wed, 24 Jun 2026 04:22:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8dee7441103f9f569704258fbc75920d9959cb502e45ef0f4aef4c3c02c3ce`  
		Last Modified: Wed, 24 Jun 2026 04:22:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32b38285eccfdf9b9f3e356dec96f2af9af6d74a0a2665df30a722a6205ab245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835449561285ec3db1657a98a0e2f4495d95a19d4b11db486251c3506920a441`

```dockerfile
```

-	Layers:
	-	`sha256:e59f7e197694c71b80b9d3f4f8c438246378b4a75495994585ce82b73646ba81`  
		Last Modified: Wed, 24 Jun 2026 04:22:06 GMT  
		Size: 5.1 MB (5055397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09d6b4be2efac987a19cd93876d58433778e1d9b96fac3df1c78ac792cac29d`  
		Last Modified: Wed, 24 Jun 2026 04:22:05 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json
