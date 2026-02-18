## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f5678b89557c65e4da9ac370a316b10d1f8a8d89ebdc53db4663eda651c6746a
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:344d4ef286233d816bddc36ea0a61e8aee9af8abdc72206b7d0adc73eef38056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243535943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78107ae2ead49958767021afba39d6c29f77e045be28b816d9360f1bee18b215`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:43:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:12 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60786c4bafcbee56275d983ed5109a507171352690cce450af5da945904d4e10`  
		Last Modified: Tue, 17 Feb 2026 21:43:48 GMT  
		Size: 145.6 MB (145628794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308523ea4ba886e002eea3d503dd52f90e6228acb9ff1850481ef41601c8577f`  
		Last Modified: Tue, 17 Feb 2026 21:43:46 GMT  
		Size: 69.7 MB (69677621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30eba6bbe0d32eff3c65a4484967934b31f0e375b291088cfd317b0123b07e3`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9485b182ae5ba4ead6f5fb585988a17d16a3eb27b49c4cc995c98533dbf7c`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:23acfa0f08006a5aceebe4e96eea6e326c643b13da926805a709b14a819cfc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7bfbf6f6673a0da9a6259bb9972fb0e6d6bfb84978e52cfbbebf9735bb78f8`

```dockerfile
```

-	Layers:
	-	`sha256:7483f5149dd5b27d42c2cc31af6b71b5fc962a590ac891f8cf9f95f5ea7c50f5`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 5.1 MB (5114654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98ec6cf641fd95ca64aed6ce0f8f40990f75d0d6603983ff2b6c98cac3efa22`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27ba2474f127cd0a0f5e999c3520a4e4573dc185b295524e078628b0e6a1d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242217662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a791ed4839186b4c7f8f7e3dcf92cfc4d5920301066fa0c101cc3604dcdc59e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:24 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f339462ebb73c47e790b7ae79d512da87bf812efd3933e67089d72b9a7c05288`  
		Last Modified: Tue, 17 Feb 2026 21:43:01 GMT  
		Size: 144.4 MB (144436250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482fab2c8fc6612c5c0af5a39ff06b007d0b7ba18dd8fd9fbd990afff89c5dbc`  
		Last Modified: Tue, 17 Feb 2026 21:43:40 GMT  
		Size: 69.7 MB (69672546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae531978889a8db3f416d0110a6b42db63d6cfeb7b29407d4ced652e84e09be`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d07701cbf82f05ad6c0001b1acec49133499e5cbf31bea98e6dd1f200cd39`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:00f458c72295a00da8f315e90a4bc3b9924a00de84b215587cc0dc0cf077cdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd50bda207d42db4c875afd689fe374a2037a4dceb1e74a3a3daeb328a4fda8e`

```dockerfile
```

-	Layers:
	-	`sha256:3b88366b394217790abd1279a71987816d2b4a869874cda732faf0e1d5666d05`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 5.1 MB (5120415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135f376c35b7856dc419018d780000e021fa6052b65c063817e7202f1899b3c7`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce0034fb812d2f625f263ecb25cf3f6d3177f9b160f8b8c6ac4278a988a4193d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253022086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43938c27bbe760d6238cec7d25860fc144adc98a5d9da616ef02c5fc32a886a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 23:45:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:45:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:45:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:45:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:45:08 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:51:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:51:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2bcebe1436b2e06a46e1026a9f267beb7b738921e7b714b94ecc1b9526b812`  
		Last Modified: Tue, 17 Feb 2026 23:46:43 GMT  
		Size: 145.4 MB (145438175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404b6ec3a53c3fcaf85af756b1d9f106beba11002b8052a39a920da47c732d41`  
		Last Modified: Tue, 17 Feb 2026 23:52:22 GMT  
		Size: 75.5 MB (75514154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0478af211283e6b920c2a7f5af0c12421eac9e3bf79010f2ba852f42d6763f2`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3834b12747b5a7a489b1ad0b133814c01f8e8381eea7d7c649ca417f85b35d8c`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70e81ab2611d9ae9911f1249b0427847541ad6e384512cdd4afd1857c226ff65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed3ae80eb520c3958847dfa469b62fd5579b18290cbe868dea24e4ada7b46d2`

```dockerfile
```

-	Layers:
	-	`sha256:7b22a5270bb8abab9b39259a237c307c3e6e594c9817b1c0f5044b27851115b4`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 5.1 MB (5119812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c493a2071a6b4add4db49f2fbe0012ed27794250da486ee3316b1692ea60472`  
		Last Modified: Tue, 17 Feb 2026 23:52:20 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8a12e361600ecfe6502ffe5c7f58ddc00609d0a6b5860f6d4e820522d4eff8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231002995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3576c054716134dc92404454591e05b1e589b9231d3b491d9dda447d7165c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:08:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:08:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:08:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:08:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:08:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:08:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:08:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e535dc0d305223a844c3403214deb9ebadafbe1230d72a59516621edab4af`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 135.6 MB (135627120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2703ecc0c2437d5eb8010fe147bd4bf5d372dded03e1d0b8db9f89c46ce65c1e`  
		Last Modified: Tue, 17 Feb 2026 22:09:21 GMT  
		Size: 68.5 MB (68490448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b3f1a76f0898489211d80bddbcaffeeb88c940603ea4f1f787b2833721702b`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb938f5390d545f64e20ba9316904463d1b9618926c67f5a3c72b50b6801251`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e85c0390be761e67343263bcffe058c11c81f5bee2acb7d82c9d150bba2d45f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05ea605e322c32a7d2eebd822dddbf1d3c1fd253799e7c1cf821db4b047bc5a`

```dockerfile
```

-	Layers:
	-	`sha256:a2f0c8b4ec3934730679b56e87ef2b74bdec8e35fddc544c34847c2b301ab4f5`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 5.1 MB (5105975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73052c71733f33c0db0bc101c62cc0f8188fd4ec124ca0679ad167bbdf87615a`  
		Last Modified: Tue, 17 Feb 2026 22:09:19 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
