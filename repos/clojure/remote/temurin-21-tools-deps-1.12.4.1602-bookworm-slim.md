## `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:953a5570410deb9a69517581e62419e70e2f2ed15a7c40f61e9f989f05f00f49
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

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cf4aa6e06b1d1ceda45cc7aa02fd68dd01c4cc03e308d9f403255739327363a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255764038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d497428ae2f0976421eb96bd63d66e38d625f5d539fdb90e56b3ecab0933fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:37 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfc159b05be645f97217437c0c30aa6361e27967895692739799784e6c83f4d`  
		Last Modified: Tue, 17 Feb 2026 21:45:15 GMT  
		Size: 157.9 MB (157857046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d0717579482f2175223461356b5ff112f6d4f4f2533a14f2b0d2d49f1a6526`  
		Last Modified: Tue, 17 Feb 2026 21:45:13 GMT  
		Size: 69.7 MB (69677460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa68114f72f08d3f1ac0f7c6520f69841dfc8df7c385bed69d29b80ab180c77`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6af814606e5bce6059b4905ec5c47c2ead6922f2c3d8956c2397df179c4f24`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4754f97801ef3afd6217f432d8f8eee50f32d7b0b6e15e630c493c7abbf2f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7644fe283d42da09142ba377fe81364c23b4c13493590a0744f7f6e454769791`

```dockerfile
```

-	Layers:
	-	`sha256:451ab6718312043e5e2b3db6e2fe1094c5852a8e1698f70dff12b413c245112e`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 5.1 MB (5116506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820c3c691c8f5d87c129de5c46dc42d9e43759b6b65c428da85db9a4c3452ba7`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45f365ed8e785de447db6ec028442a55f967d66c82108f12f3d0f8ba574f4b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253914598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7576fa041d564039ffff48ffdda9a06245fb1326d9fc2fe651bd43bf85c5e44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:44:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:36 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f9f6d86ff3bea27763b6b0dcd9792dc323972e93d655e01beadbc165ae5d12`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 156.1 MB (156133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867e102e05594cd9767417bb7fdb09d3d62847ca31ca6612783d2754ab39256c`  
		Last Modified: Tue, 17 Feb 2026 21:45:13 GMT  
		Size: 69.7 MB (69672661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00ff6610ce865a19b87a70d2a3917f96fdc7b743ac7e63aade55fd9cccfdbce`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b454718383646527aab35f64c9e99a980c3e10a52d06d2cb80c3aec622b9d5b9`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1757869720a98d32ce058b7eb7c450d2f2cc9fe6816eba286e6fb03129f09115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0417191e7287754e5f3f71e3b74fb50e4e158100b6628d792e0f4c18e50d4`

```dockerfile
```

-	Layers:
	-	`sha256:0309f60f7435ba8c7971ad084e0ee6c7ad4c5c47570fa774e2a71dd72a42aa11`  
		Last Modified: Tue, 17 Feb 2026 21:45:10 GMT  
		Size: 5.1 MB (5122267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8147a2c663dd876799c5b4eccccab5dcd65c24330345aff61145aafa5f9a6b1e`  
		Last Modified: Tue, 17 Feb 2026 21:45:09 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ff8bf69316c5a61e28a084a859b62c60c8d3b4445bc9e43ab3970af3c68849d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265561408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e45247d9ae011d5bac4478a8006dc3020e2032a2c132a93257d8216e35b01ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:34:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:34:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:34:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:34:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:34:00 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:41:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:41:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:41:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:41:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:41:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04686be48d2a894920edac0c0c6434c05a7128013df9522a975b048c103c93d`  
		Last Modified: Fri, 06 Feb 2026 00:36:06 GMT  
		Size: 158.0 MB (157977491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ff8ed03f353a0ece5f58bd3ce03806e34111b0130fe1fac2ba69c56d0e8e2f`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 75.5 MB (75514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7265c5180d70ca2c83535214d9fd18f098c2a50781f5aad0b7f5df89b09cee`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81e3bbf033fe93b7b083fd05fd6c7bf3ad2317b1c830b56e7b82f3b001ac9ff`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a8ce8c3ecdd6d2f1ce2b344f4d4c8973307b9f992fd6bce75031b915497cd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dcd4ab30efe6e3a5aaa2ecc8ebaaf33c7771419200ed04f6fe7d48f4802cbc`

```dockerfile
```

-	Layers:
	-	`sha256:9b8aedfaf5c7109d228a7108634c9401ca0fb7628a1779d5b2f8f7b724fdec3d`  
		Last Modified: Tue, 17 Feb 2026 23:59:43 GMT  
		Size: 5.1 MB (5121664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f5dfeee110634173b5eea3adf60bbf9b91d861b606700c6c2dab519f5700b9`  
		Last Modified: Tue, 17 Feb 2026 23:59:42 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a27cecb9f5fa8ce5d8b2dc85657d0d4ef01f47e2de72c8ebfe95c47639656834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242481210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2732460ae39174a8c83e14cfe992ef71c168f5d5f610e41c06b48d20ec605ea4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:13:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:13:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:13:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:13:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:13:12 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:13:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:13:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b838670a4f355a1ac037114110d70a67c8c7c1288cea2a0bcf49e74a0f97637`  
		Last Modified: Tue, 17 Feb 2026 22:14:43 GMT  
		Size: 147.1 MB (147105302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d46a41181b95fce21464a8c6075dcb829a6a59ce7605b7ba5be0648c5ca091`  
		Last Modified: Tue, 17 Feb 2026 22:14:42 GMT  
		Size: 68.5 MB (68490479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af4ca1e6d77b67989dcdaa7ff5c8725e45dd4cc2abd1787e50296da24970f3a`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618432aefeca4f6d066d9cfd5d19d37e2afdbb4e7195b433fd669dc6a7897c63`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89dccc571eca74bd9ecfd2bab8ad667516aa8e93331ec70419179d75e1298be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8ea6727b283bdd6b1c87e54c6c05cbb9be7572cac74fa6fc7cf7d186be74e3`

```dockerfile
```

-	Layers:
	-	`sha256:78093cb699d13b05b1ba68e67ede3ff5c40c6cd950011efc1d2ea97a09e347c4`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 5.1 MB (5107827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014901a333973ac8938e57130a350376dcd1032d803b976256539e5909356635`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
