## `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:31cdf41490208d41a84bdb41f83f941df512e5727d494d96bdfa29e575c65025
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

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:74d25ac2c9fcb4dacd816aa36ece0aa199d69e4d44f9b2fa54191d72bb66c3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247581772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6790e975cced8c7c80097e9cd65e87b762bd0e9f2813cce7dcd5d1616bd6051`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:10 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3281c884f84e8b5431f30d6be1f1f7b39136f089e6a73482ccca86598ac7aa9d`  
		Last Modified: Tue, 17 Feb 2026 21:42:48 GMT  
		Size: 145.8 MB (145806745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19071baebadcf5175cd0d4a5fd64978db88ba057a968a52d7e48d742785cd1c1`  
		Last Modified: Tue, 17 Feb 2026 21:42:46 GMT  
		Size: 72.0 MB (71995786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493bc6ab807f8b90e87ea8579af25a3ed5c1b50312bb86b579dc3340d04bc959`  
		Last Modified: Tue, 17 Feb 2026 21:42:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5d41d96f76b67c29b5faf68caadd7812ca350e324968960a3917231c373104c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b48eac7807c031f40654bdd813b632ec68b922b714ea3da11f35f381630374`

```dockerfile
```

-	Layers:
	-	`sha256:620fddafa9eea06a95c0a3df8da6d2017d5cb95a75d9de1d17ed6c36cd7acf70`  
		Last Modified: Tue, 17 Feb 2026 21:42:43 GMT  
		Size: 5.3 MB (5277692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ffe1e7eddb71c9e68d1f2b8ee3a69b0b65a1541608bcc8d47118d223dabb3f9`  
		Last Modified: Tue, 17 Feb 2026 21:42:43 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8cf8738f034e625c288d79da26bc30a88b21853b243e6b933ebfbce8e614c379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244448784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb6fd6bfa63bfbf1572cd0722408ac290dd0e7b20d6381f90aee77dfadcc351`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:42:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:05 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5794674822b528b71ad7dd02bc57800afc1bfed9d8754d05010a0cc44a362426`  
		Last Modified: Tue, 17 Feb 2026 21:42:46 GMT  
		Size: 142.5 MB (142501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1793a49994d78dc1e937506520bee9baedf21b80474085422a5aff15ac7f1bf`  
		Last Modified: Tue, 17 Feb 2026 21:42:45 GMT  
		Size: 71.8 MB (71806650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7557975aa46262d8aeacb03ba59c68374316904e97ac7baf7f874278e7c0a6dd`  
		Last Modified: Tue, 17 Feb 2026 21:42:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6339730e2c0879dc72ca1209eb217fd59e19d6fad4c405d487144257dd78ddbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f9f2a6a280589fccd19ff4e17c0035b5c651c5a6a28144663389d1f7b9e722`

```dockerfile
```

-	Layers:
	-	`sha256:0d778308cd9cb88fad1a4f9857fc5dab1a093a865991f393886ab7e07c495cbc`  
		Last Modified: Tue, 17 Feb 2026 21:42:42 GMT  
		Size: 5.3 MB (5284079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7203102e0df3d0b67217c64fb3ea0aac7b6a396787cad3807c3f7b4398f51ed7`  
		Last Modified: Tue, 17 Feb 2026 21:42:42 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1e2e36b78f7341bcb2f025d9071d8eba5d4432f65898f8d9fb863e458fbe103a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243988985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f1a7aa8b5cefb38424f2d09bcd2145bba3336f5dab7e47a6885f743637ab99`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 23:36:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:36:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:36:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:36:32 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:36:33 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:44:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:44:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:44:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ea58df9d5eb840d3ee88162e3f67c2743c098ce80de629ce328e4ca1f7bf22`  
		Last Modified: Tue, 17 Feb 2026 23:38:15 GMT  
		Size: 133.0 MB (132997814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ee119024f45087d6133f4c886e3daae9ead6420ebf737dec88495bfd32945a`  
		Last Modified: Tue, 17 Feb 2026 23:44:47 GMT  
		Size: 77.4 MB (77390339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a240f46d2574a8d16c923b44d1e590e8fa1519a6c4f4e1793d67a79db255e496`  
		Last Modified: Tue, 17 Feb 2026 23:44:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70dd82eadb11b503eb48df516d5049d6982d727e8b9b11e263879a0602b4b4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5295739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bddd069198efa497b2015be7310d83d7f592dc9c9634455b8b4d242360376d`

```dockerfile
```

-	Layers:
	-	`sha256:52359d3ba01f35ba0b5bccd652267ec20ad3ceeef24b00eaa451ce868311426d`  
		Last Modified: Tue, 17 Feb 2026 23:44:45 GMT  
		Size: 5.3 MB (5281448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab524fc544a470e326721a4d89f3abac1c8673d50d6f1c33c0a5b80616e723e0`  
		Last Modified: Tue, 17 Feb 2026 23:44:45 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c06cb07fc57b28fc8d729537c655466bb21fc3584e1bce203252f34df97eaaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229354013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811e952de955a981d46e9085d4cd31b1e994fd4c5eb2057db9e8d02d99a9e316`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:04:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:04:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:05:00 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:05:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:05:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:05:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4228042fd7c68977db9732b8db040ab2bd28f30bc9d5526751b817a4d24e5ef`  
		Last Modified: Tue, 17 Feb 2026 22:06:38 GMT  
		Size: 126.6 MB (126562060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518d12f377ce94aee4e3dbbd4baff57f061dd069f2b1d59aee359b3cdc471c1`  
		Last Modified: Tue, 17 Feb 2026 22:06:37 GMT  
		Size: 73.0 MB (72953155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32c14f4be0ad73764e4d7b1977fdcd4f5b1f608237796c964fa61529724bdd0`  
		Last Modified: Tue, 17 Feb 2026 22:06:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f73b0a9cd895325892cdcb7755a6ba6c265611c72f0bb238ebf48d95bceadd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5e80867fc07801857708a7e04ae27752718bfe2b2efe64ded8b8a23cebf795`

```dockerfile
```

-	Layers:
	-	`sha256:ec795bfd3799056da0adb2e4fe8d2a1931a31fc4de0e20943fdd216d48a59778`  
		Last Modified: Tue, 17 Feb 2026 22:06:35 GMT  
		Size: 5.3 MB (5273620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1ae02c02c0f2622eb0c34f39c760cb818947159b85be8fd391ee46e45420fd`  
		Last Modified: Tue, 17 Feb 2026 22:06:34 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
