## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:6e0783023d3d77432ca31cb3a886a6f21021b776c282ceaadfcfe57262df22d3
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fc8e9d2c6d657c8a4746dbf3a0937afdeaec2814606859318627672ccd78ad98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255732373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8326c13663c22d5d0f2a96ba6d97379eb5be26cff067e686707a30de61607768`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:35:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:35:45 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:35:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:35:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923ceb83ced0d49735199f4791598aa5191f4ecfce292203c014a0857d9b8`  
		Last Modified: Tue, 13 Jan 2026 08:16:10 GMT  
		Size: 157.8 MB (157825957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b3e37ae79066e36ceeed2bec7c5d835b12ae7b6fe32fbc703456015d04038`  
		Last Modified: Tue, 13 Jan 2026 03:36:32 GMT  
		Size: 69.7 MB (69676801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b99411d727a1bed083309f39d6046178c000a8df41ae7275328b90ac0e8d645`  
		Last Modified: Tue, 13 Jan 2026 03:36:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4a4ec40a4719687f1cf48a15718f9217aeef80164379497f0347c26137f3e6`  
		Last Modified: Tue, 13 Jan 2026 03:36:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3bf3e0c417f547d15ce84bb47e39254e1678ad2d3cef7bfa84dc21ed3e829bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1531484f667c5dcc8d271c48a41d4123ff1d9ef1caf0e60de03acbf672dd4536`

```dockerfile
```

-	Layers:
	-	`sha256:a2b5913ca8c339bf9d92c5385e0ac3d7e743534131aae116ae11148c11a1a103`  
		Last Modified: Tue, 13 Jan 2026 07:42:23 GMT  
		Size: 5.1 MB (5116502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dd3cf548002e1dd41a035522d86e6d5d78d2fcc42236e0c0a038cfd7ce8102`  
		Last Modified: Tue, 13 Jan 2026 07:42:24 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3492fc6a1f761df694a2a6f27991bb620b34d8488885a29ca2468be2f881b6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253889201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc17e4c062fd6a5b1dabc3e705491d6cd41336e793d84a054326e72e2ea2a03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:39:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:05 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:39:05 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:39:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:39:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389f14ef53abc291e26db566dc411b559aecded673e9c299675a360fdc6e2f1`  
		Last Modified: Tue, 13 Jan 2026 03:40:09 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1446fde5a888baf83ff692cb9eadd04849e6623e72fae2d5ee8160772eed4512`  
		Last Modified: Tue, 13 Jan 2026 03:39:58 GMT  
		Size: 69.7 MB (69672697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcbb0b707dc695796681a70dd07e2252feb5a4efc548e95f5fbb76f023eb013`  
		Last Modified: Tue, 13 Jan 2026 03:39:50 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da985f17ac43ad82f119dce1c5dfe5b04fcfc68b415220388217a9f5d8b30db`  
		Last Modified: Tue, 13 Jan 2026 03:39:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b1d59551dae5184be88baa945a9f44d4290c6918d6b77908812b26b38efb2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1679b41e0d849cfd8d5a25235ec171c019dadf073e05b46139f9eafc2c89b753`

```dockerfile
```

-	Layers:
	-	`sha256:1cc288f70415fcbc206dd9677f7927fef06017e611c3b20b0a41a2c01ce9bc89`  
		Last Modified: Tue, 13 Jan 2026 07:44:25 GMT  
		Size: 5.1 MB (5122263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc5b438102f2967502495fa1c9cbbf350c423f5e778c903c0606ffef43afe1a`  
		Last Modified: Tue, 13 Jan 2026 07:44:26 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:904dbbe666cb556e1d167c8b88ac2b093346345dcb3204e14236d757d43685c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265525266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07d258283f84fb1481a9ef6f5aedc9806779b4d9c4e5842197af1d356d1d64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 03:02:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 03:02:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 03:02:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 03:02:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Wed, 14 Jan 2026 03:02:23 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 03:05:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 14 Jan 2026 03:05:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 14 Jan 2026 03:05:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 14 Jan 2026 03:05:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 14 Jan 2026 03:05:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988a99efa32b6764c786b7a182133c65d55660c4cf1e6f5287fce43c2a14051`  
		Last Modified: Wed, 14 Jan 2026 03:04:43 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56514fd5984181545ec4884700324f9515e0a37229028f48b96188e222a4e0f7`  
		Last Modified: Wed, 14 Jan 2026 03:06:08 GMT  
		Size: 75.5 MB (75512566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60119b32f4638e862105021f202275aa3b29562fd290342803a7d6b5d3c61d39`  
		Last Modified: Wed, 14 Jan 2026 03:06:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b345e44db2b9c674c5762d69e118515be5b6280de00c61e7f4f8179aff65c86`  
		Last Modified: Wed, 14 Jan 2026 03:06:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43f609b7d3303db2354500502ae9bda9a20a5511e1c0cb27e803356805abee72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9e6af264eb6bc4f9b3d8309df365a52169abbc875fe5d2a7cb6873916c487e`

```dockerfile
```

-	Layers:
	-	`sha256:5c3f3725e31de736bd93fa1e2077e875deed83866efca5043e92c91e40416e13`  
		Last Modified: Wed, 14 Jan 2026 04:36:33 GMT  
		Size: 5.1 MB (5121660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475105e23607ee56e9eff32fbd96d810d33299d669055d2de903d2d7824c6df6`  
		Last Modified: Wed, 14 Jan 2026 04:36:33 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:562f1a9cd980336d87da553512759fb315071ffff09730a1994c2b2c370f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242443852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52794dc06de5ce427192c236d1b9f67543d6087935bd89822a5f20a8a192f16f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:20:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:20:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:20:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:20:00 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:20:00 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:20:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:20:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:20:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:20:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:20:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cbe2e3b111a17feebbf9e28d72c13e483bd7bdf86d08ab8e10c7c3d5063be4`  
		Last Modified: Thu, 15 Jan 2026 23:21:15 GMT  
		Size: 147.1 MB (147069874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f57447f55b2dc37cce1b87328c91e5e2d618b33d469e2a8ce49600cbba0ccd`  
		Last Modified: Thu, 15 Jan 2026 23:20:58 GMT  
		Size: 68.5 MB (68488524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcedf78be2a47e215e89e70ffae848de1a82b987120af5f4de086b6a0d6ef3b1`  
		Last Modified: Thu, 15 Jan 2026 23:20:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16531d62ea508068b0b79bfd6db827028446497bcd9b176258350804cda378a0`  
		Last Modified: Thu, 15 Jan 2026 23:20:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba9f61d73dc851c26752aa957a69b97e374b4eee6abdffbb9dcd71de1f6498f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d098ccb9004cc5341f074f1568fb35c6cc2dafa645d2e04826c10ac210ac55aa`

```dockerfile
```

-	Layers:
	-	`sha256:70f207512ab48c8c2d39fddec262b7da4948636517d8ac17a87d21becbf0a7a5`  
		Last Modified: Fri, 16 Jan 2026 01:41:24 GMT  
		Size: 5.1 MB (5107823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05837d61269d5076b02d9b4cd1a33c51009afd117c6d18ae87a7fa4a794fc1bf`  
		Last Modified: Fri, 16 Jan 2026 01:41:24 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
