## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:ec09c123c58093b05ea1dad423302d73c78483922a4a149422e982e9470e7c7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0d5a2c6493a6e24294f1df5f7b8e7109878228ad64d8cf4e1d3b86e00626971f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178047907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c85557f5df8869631c8ff256f564f2fff16af2ac64193025ccb354da44856d2`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a702fde8e19e23f52aae83b0c182ee09d2efb516c2f2a202f67b5b98d3315a`  
		Last Modified: Tue, 30 Sep 2025 00:51:29 GMT  
		Size: 54.7 MB (54731283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3756c7c8aac4652545f0c81047ecdd29697fd42f1d13cd941ac76e168aa97b7`  
		Last Modified: Tue, 30 Sep 2025 00:51:27 GMT  
		Size: 69.6 MB (69559915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b62634d92b74d3f1e1b8b0c9416165e51bf093d7c45c1f16db18cdc4aebc5d8`  
		Last Modified: Tue, 30 Sep 2025 00:51:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:44a0d3da8102635890fd44bc14722bdb1b9cf1bb5037cd6710cbf20dcb521c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5b2c2bf0be30bd724bdc79e45a52564777af37e51c3269be54356c4fbba84c`

```dockerfile
```

-	Layers:
	-	`sha256:32b417232e83ec926eb1529670e190df9cb003348d5511b6ec5357a4d0d990f9`  
		Last Modified: Wed, 01 Oct 2025 15:43:23 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09576f4c1e90ffc5523471e5a720caa1b38bf0d32990a515e790818bd51f6654`  
		Last Modified: Wed, 01 Oct 2025 15:43:24 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc1298b1a419f214cb4d41f10dcfa31cc12fb310482881af072450402245a7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175773142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ea03fea2df8ae89a73ddd7dc609fcbcd0bc63ea4c35d33d1d750e33200cb8b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f5f145040cac7c8485f2c163ee82a27ad04b0a99bd8d1fce3bd488cd859422`  
		Last Modified: Fri, 26 Sep 2025 20:03:38 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea14f6d927c9a78178c166f1025b8bdfbcdc37eaa81ab2fd62143a3959b6a8d`  
		Last Modified: Fri, 26 Sep 2025 20:03:59 GMT  
		Size: 69.7 MB (69688518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966cf21bbba0dd67223c1164c7a37d75fa9a882eb0fa40d70cfca7b999179b17`  
		Last Modified: Fri, 26 Sep 2025 20:04:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0fedc30e0457cd3d42b933f78024eea245315a4e219448376f913466dda7af7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4c4617c4e352fb523d405af812decc5d3378828cc4cfef8da9c970ff27d337`

```dockerfile
```

-	Layers:
	-	`sha256:98d687c68618b0b3e69e5917ac44f0cd44b6eb2d5868bf115286c64e038a7309`  
		Last Modified: Fri, 26 Sep 2025 18:46:50 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642e21777e4e5eccc329d939798c7f1de172e958dd568296c9231da5e5e01cf1`  
		Last Modified: Fri, 26 Sep 2025 18:46:51 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json
