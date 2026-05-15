## `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim`

```console
$ docker pull clojure@sha256:39ddb4e2280f833b29788519cb59179aaeb12de3081274003cfe4bfafd56404e
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

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a780df06132df1b9f327b5547c6f1d2d2918dcf106ee367ded08a4614f19d6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196283582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d504c3336862b5829c98d2dbea0d69b0def2530690ad51cd2cad6802bb648c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:13 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:13 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa1e8705e550ced63c58419f12aa40a00ef6fe82bd3d3150232c2187b3a75`  
		Last Modified: Thu, 14 May 2026 23:37:50 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0305a2ee7876db75e365fc9b72d42bed17a5c5c9bd475fffa7cf22eb3f8914f2`  
		Last Modified: Thu, 14 May 2026 23:37:49 GMT  
		Size: 72.0 MB (72046617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5584555155577bdc7532d0f1c15b07049d85ea102e621ad10adafe001dcb86d`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192ed0cbade24a554c1b557a3a0f13f6c7543f24a54f931f45f80f4e67e667c0`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec4b6680cacd477033c088f8a652dde2a2a2ef7badf6d4c4ae978a4a438a20c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5b4995a3ebf089151fddb344828822a57b9aa900ec174d502a74a62a2733ee`

```dockerfile
```

-	Layers:
	-	`sha256:b9a80d835791c5e44798855aa4d76121f435f10a1e622a34867a7ebaab2337b1`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 5.2 MB (5224730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e4de003e7c7d0001373488cbfb67a92fb24e56afc902605e0d7d7404704ab1`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26a85f436b445852a9b907064d8f5651f5efde186af7913e4a069b05369960fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195394461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac450e70745d17779921a8b42a9e4b043b51ac5a39620947352ce7871ea7316b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:37:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:24 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:24 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3f6098d2ca3d565f743bd3f00173b2b594ed38bc0b459c4ae5f8df8cf0f62d`  
		Last Modified: Thu, 14 May 2026 23:38:03 GMT  
		Size: 93.4 MB (93395165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6891c2f4049fc336ca2afa54f01bd050784a036da24d2691441476e90517dfc`  
		Last Modified: Thu, 14 May 2026 23:38:03 GMT  
		Size: 71.9 MB (71854607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943c1ffb98cbd8e741bb984bb2c62c871f3a22ce75e2dd142058a89be3758e3`  
		Last Modified: Thu, 14 May 2026 23:38:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318a9690fb4ac1bf4a7363335806d8de314d130d373ac866c1c426ed90412e7f`  
		Last Modified: Thu, 14 May 2026 23:38:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f32e76a2cb00d19e9d7f28b593f0e3a0aca0f48b72176a3426f42783ec09e4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c0fda4ba1e4a6c93b5314d34d02cc5e75226cd93a723ff2dc8d6a1e7d6ee75`

```dockerfile
```

-	Layers:
	-	`sha256:5e86eb380330331d198f8c716d9fcd7736a90e12480dad69d70db3d9b0fc596e`  
		Last Modified: Thu, 14 May 2026 23:38:00 GMT  
		Size: 5.2 MB (5230496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:030dcc61e51e5b9aa6a75c1e9425c8e43e478c9365115a4a8f9dd7cd510adb22`  
		Last Modified: Thu, 14 May 2026 23:38:00 GMT  
		Size: 15.9 KB (15923 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fcbad04b28864f43d6dc09dc44d99d7c4763eb98f33a677843c1f831a85cf49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.8 MB (204838226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b907f8d4185dcd6b4a27ee977294736d2b1b4001c73a83b47c4b74356f70600`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:48:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:48:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:48:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:48:40 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:48:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 00:00:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 00:00:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 00:00:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 00:00:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 00:00:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c851b38219aaa7b8bb1dc9df4fae07f486ef426ba65b2ac9fddc58f5530e930e`  
		Last Modified: Sat, 09 May 2026 02:49:48 GMT  
		Size: 93.8 MB (93781452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f69d429cd41158d29895cc91a6f94b7c5651c4a26f785502c7249bf44db8ca2`  
		Last Modified: Fri, 15 May 2026 00:01:32 GMT  
		Size: 77.5 MB (77457641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b2fd41cbe7ac388aa3e5aabc533e9331bb40dc332564463ed07b656483e76`  
		Last Modified: Fri, 15 May 2026 00:01:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade9cb095ea5e5c681ce99e7c6f9d736a35772b0ac3d2fa63834dcc3bf5967a`  
		Last Modified: Fri, 15 May 2026 00:01:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0b993db1095a4f9ac19e33e2460b43b6863a47dfb4be61771421f879bc96f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b1aa298c7e306aa299e471a9e17ddbfa968be518da6c755f241549f69bbb0b`

```dockerfile
```

-	Layers:
	-	`sha256:f984cdb334565aee02b84a9912290aaaa33bcf0eb89e7f6c4d698d99a4911cff`  
		Last Modified: Fri, 15 May 2026 00:01:28 GMT  
		Size: 5.2 MB (5213037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444bf6798efd4c7a30a43873480ec297a5ad910ce0bb83e586564f1b7501d3f3`  
		Last Modified: Fri, 15 May 2026 00:01:28 GMT  
		Size: 15.9 KB (15852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e9f66e45ff5ea0d3a0716a505c0d5bc623fc6267ece772cffeb9ad6888bbead4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193404078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f28d2fabd56e38bef8516a5ceb6559c0b9c7085241126ab5b9a953f8cb5c177`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:39:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:39:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:39:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:39:49 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:39:49 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:40:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:40:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:40:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:40:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:40:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73d5241852e0afbdcd0935ab5ba1fa781242a71af94e93428d0cbb97483c9e`  
		Last Modified: Thu, 14 May 2026 23:40:30 GMT  
		Size: 90.5 MB (90547745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec6ca4310a77c08bade679790b9b586a8dd1b096b107ce46243b9e330ade5a8`  
		Last Modified: Thu, 14 May 2026 23:40:30 GMT  
		Size: 73.0 MB (73014944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b63b85fc2e9db80ed91eac79e2c57d3150c9f462ed08ba8cc8866d97b6f3c3`  
		Last Modified: Thu, 14 May 2026 23:40:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c77762304eb8d599d13222c42d1678efef0ed18b914bc8865e51d9352f02be`  
		Last Modified: Thu, 14 May 2026 23:40:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f39aca65333699530c9ef390b07119f368808fd63cb13698bc0ebb38d3beeb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d27ef1ec070d0eabf3215ea0c23de092ede829dab1da320ab5596a59192009`

```dockerfile
```

-	Layers:
	-	`sha256:f1ad45235bb0717fb529babfead94ad4474ebac51a903e157c841be6fd7b1f3a`  
		Last Modified: Thu, 14 May 2026 23:40:28 GMT  
		Size: 5.2 MB (5205840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b95e21e4f4beddb60f33d860c1cb813d17f6b6a7bad78bc19a97246e91de5c2`  
		Last Modified: Thu, 14 May 2026 23:40:28 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json
