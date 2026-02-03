## `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:49b1e97d4ce49612ece1cdeec0927c0e4af227cec06fab53f374fd32e21fa21e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f4ae50dbc9994f9715bc240aff3a41dbe2e027e53c826ff6f2fc41b3d2bd8ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156508451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1a364750b0dc4f8c371054b9e62667ce2e2ea8c408d35b2adc5fce6fdecb2b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:17:59 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:18:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:18:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5d23877b51c01d1e3dd5916935066d4accc854310db45c2a02af8943165e64`  
		Last Modified: Tue, 03 Feb 2026 03:18:32 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e24148846e3db49b7f099f2406326718007cdfde810b4adc9583818d94bef1b`  
		Last Modified: Tue, 03 Feb 2026 03:19:13 GMT  
		Size: 72.0 MB (71995838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25185a308338ebfb5a768f87740ac1230bc9e2d09b254947c0be23f61640c5e8`  
		Last Modified: Tue, 03 Feb 2026 03:19:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7065db29878a2a1161c28da21476f430c0aba7c991b458e5737756979e688dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c7da56abdf61f8a7e1f6496675d41f1354c328671331d3f7c850fd2ca415f9`

```dockerfile
```

-	Layers:
	-	`sha256:f896e669c0eb9ff70cf2570efd3c92f6bea71499225a6336eb69b1489ce2760f`  
		Last Modified: Tue, 03 Feb 2026 03:19:11 GMT  
		Size: 5.4 MB (5377907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdfc8487379f417dd1c68b840e044eab8a8b8a7785de367b688de1444e125a8`  
		Last Modified: Tue, 03 Feb 2026 03:19:11 GMT  
		Size: 13.4 KB (13428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b53c800d6dca67944632ba66d56c36573d9152d589fc650c541779339cf78a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155762304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6dbd08d1a0fe1e1acfd341b6c6b99932add24dbc52c859e4754abaad293bea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:36 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2047505dae0c83b30a65b712ee6c0a65147c64e896e0370d771362f22c96fb7`  
		Last Modified: Tue, 03 Feb 2026 03:21:08 GMT  
		Size: 53.8 MB (53814976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dac25450c753f915e11e654fc7928b19321b6da277fba928934ca8207123f5c`  
		Last Modified: Tue, 03 Feb 2026 03:21:49 GMT  
		Size: 71.8 MB (71806616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00001c6515ea0fa308423a553db9e70471c8094dbd5c3630a39bf51b98266846`  
		Last Modified: Tue, 03 Feb 2026 03:21:47 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d113a8d21b96429055a1883d8acddc52aa5f888bc59ef78fa3a4c7d79815b660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb241c03f1f7cf36f3ab01c7944464681c66eb01372be45622ebe23d80a092b`

```dockerfile
```

-	Layers:
	-	`sha256:739838a255bc6e802c47a4d73dcba720050557bc084fb6a36bb6c1dec7f5a6de`  
		Last Modified: Tue, 03 Feb 2026 03:21:48 GMT  
		Size: 5.4 MB (5384374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f3c15520ea0578c1b070c3297f07e3d41b515770cd1327979e35264b6e8b00`  
		Last Modified: Tue, 03 Feb 2026 03:21:47 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b6211e02fdaa84b368fc46f8cb5bc8995500dc6aa23a50b9d59ef9973905bc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163165032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b209fb5d1ae85306fe17e92f8c69f698041d8d66580ccda96f183a71dede94`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:30:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:30:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:30:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:30:19 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:33:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:33:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:33:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c819a89e06acae8f0e6e8b0e7165e0365d89135dc37230b2f706d88a3eb226b`  
		Last Modified: Tue, 03 Feb 2026 09:31:29 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ce2a7990ba9e73b3be97fae7ac08d52a7c87e9cc1769e4a658c3abc6f8acfb`  
		Last Modified: Tue, 03 Feb 2026 09:34:35 GMT  
		Size: 77.4 MB (77389058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f8fa08d479e243641861c25932eae86921052591534262c09611c62441ce4b`  
		Last Modified: Tue, 03 Feb 2026 09:34:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:591f33dee26f2dec094cd4064197514b8aaf6e18812e2452598d8f19c0bc944f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2cace2f7a6c5f7be3a73b9f90b0c66d067eb7ede3f0c6ded7b11720bf2ab84`

```dockerfile
```

-	Layers:
	-	`sha256:16116c4eaa7a09ec680e94fbc4725d5c9c389bdda5a3251c2b3600c5b3a34968`  
		Last Modified: Tue, 03 Feb 2026 09:34:33 GMT  
		Size: 5.4 MB (5382871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57dd869176b7fda41e516c3666fa675457e291ac5f747bbd65fcb1c6592fa322`  
		Last Modified: Tue, 03 Feb 2026 09:34:33 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
