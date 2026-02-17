## `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:904788341de33c6e70fabb28563ed3ca2e8de55a77712f1d2d265394f5518345
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
$ docker pull clojure@sha256:32b10db04ee51b86bb595f4737cd2635c9ddf7b389e2bfc1bbe1ba5901e0a539
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
$ docker pull clojure@sha256:7c5a1273be3ad2db6ce68f99aeeed9c6fa55fc981c2e2eecffea7065b659963e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f6fdf15af8f7d1c96dea0edd31fc8e8663ec3a45bc950fc65b731e53cdd314`

```dockerfile
```

-	Layers:
	-	`sha256:b2bc6f8e55ee1cb6513cd8fdc905f573215483f40106eef0acf448c84abbd017`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 5.1 MB (5121664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed9b82b833a6e16035e83dbc6f17aef322a511e7ea371eaf5207ab6ae71bbcdf`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ce9a8e2436fae3da9e9af9d2ed99e1938a34079a9bc10253b1fe16294710ee02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3725f6733a71c614246b62c09a3e0beb5f47cf5dbcd6e9ceeb41758fa97265d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:06:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:44 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773403c4ac668294912a2f4bf051fccdb773b7f95b012f2359c393546e2ddef9`  
		Last Modified: Thu, 05 Feb 2026 23:07:29 GMT  
		Size: 147.1 MB (147105284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c378967ab4ba8289ea3b6f0834f056aa2928ffba607825b8e155f7a897ad2b5c`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 68.5 MB (68489976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690e0a039ed09ba1f7719fe86faba2b1576fbdf42003609d9307311e5a5284d4`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fef3b70f0946f8f228064f0b8526f80a5a4bde0150a76e5747952fe1f80d30`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f024b7e0b5bdc79e6dc269d2735deb44e6069a621913bb7b53dfdab9992c1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1240576bc2eff6bd181ae867aef772fbc018ad60022dd38ea1bf16c89fc38f45`

```dockerfile
```

-	Layers:
	-	`sha256:bf49f8402469653d9e12a8fe13d495bba6c6602f2cf499c8c87493904a9c62c5`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 5.1 MB (5107827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65ce1ee2c3921150b49acb3cada5ed41ba0df08b611f6503c854c97f292c36d`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
