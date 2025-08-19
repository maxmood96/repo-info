## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:dbfb19bd7b17714d5c505f45a8c8c3d82f2b15849e763470bcfc5c01d755a95c
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3cc120570aca7eda0bc8ee766823d58386842dac0f08e696c0610403e45dbcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890ea4b49d609514ca76e91c2319eaa7299e90cbcd7fe690ec9a11ae443e7cea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef853900c39f7a385dfc4798c87e050626403392984d06d6dafd8565ed8cebc1`  
		Last Modified: Tue, 19 Aug 2025 04:01:28 GMT  
		Size: 145.7 MB (145658140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd8782e93694717d457718154beabb7ed77a377f6902be59b0a81806dd6c651`  
		Last Modified: Tue, 19 Aug 2025 04:01:27 GMT  
		Size: 85.4 MB (85435995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14b5c375818b0941b87d847b42d58f33f317a5cbcd87b7e001145902ebc6d91`  
		Last Modified: Tue, 19 Aug 2025 04:01:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:328dbc8be3cc9e1f41229b2bfafbb6529b42dee99cedc3b39586cf160640aafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979c02ebc625a7c1dddbd2821880900fe9b2b49447520b981640ce6c69356998`

```dockerfile
```

-	Layers:
	-	`sha256:8e4d201f249c51c23297d2aca1e2b5fd6a06de16b35220382ab2a066537471fd`  
		Last Modified: Mon, 18 Aug 2025 18:36:30 GMT  
		Size: 7.5 MB (7482362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:087612113e6424457b5df389c996ca3816ba70a01f7da42b20661ce05eb22399`  
		Last Modified: Mon, 18 Aug 2025 18:36:31 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22abed3d05dbdff06abafb65832bdb11c6ed3908509009f4f437fccddf2b5b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277359260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20117ab22ad3c3f78c301f9620fbe7aed8c7ebe221a8a1344df354ef23336695`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1cc20894541cbd711745752d2223fc23d38752d9fb22d82b12f78632b069aa`  
		Last Modified: Tue, 19 Aug 2025 04:02:21 GMT  
		Size: 142.5 MB (142460532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed794ca98e567aa1aaec8612b934aa0c4ba7e95441967b3d3ba4c1496cbcd1d`  
		Last Modified: Tue, 19 Aug 2025 04:02:17 GMT  
		Size: 85.3 MB (85256480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44330ce39f76d2e1d06262f53299bb7695b89a8691bc17d27a95c168c6162518`  
		Last Modified: Mon, 18 Aug 2025 17:09:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:66044a05ea4e75ca06a6efdd6bfe1c69f338cd0d6bcaa7dfd6e07b6f1b657316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28059abc736d98ef45b8a783c2e1c9b808da25364bfe586056e10422d5cb42b0`

```dockerfile
```

-	Layers:
	-	`sha256:3e818e9764adf950aa1c3628435668f44f5373803145355638fd786807fbccc0`  
		Last Modified: Mon, 18 Aug 2025 18:36:37 GMT  
		Size: 7.5 MB (7490010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da62b7da5b6831cb04147531fd34a9c36053d84961c0637e1605f8e059a3d520`  
		Last Modified: Mon, 18 Aug 2025 18:36:38 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7bf9794af7dc962539ffe495702c91436ff9c27edd55de5faf050cb6e99937fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276797983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c373fb4ad83587e3c3d0219c1d31ee46b36ea0afdb68d00b7f95963220d227`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967a97862e5fba4f3e376cb8ef40e6f26a430a3f4696b51f2bc128f1d58140fd`  
		Last Modified: Mon, 18 Aug 2025 17:13:09 GMT  
		Size: 132.9 MB (132853303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c73bfd56a6508458012f31413f456e55d54558c0320af8d821b3a6ec0ebe5ec`  
		Last Modified: Mon, 18 Aug 2025 17:13:46 GMT  
		Size: 90.8 MB (90840649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7ca3eb6c09707726e76567433bfeb13d237e07eef7d6342a58e2bf4f6311d4`  
		Last Modified: Mon, 18 Aug 2025 17:13:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ea5ece0c0841941b8032764939fa89b73718d3f27bfc0914977ad069d49c427c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b0fd3f15e7023eb9a4a51d9889fa82b40897b6c8defdd973a3dc88af882053`

```dockerfile
```

-	Layers:
	-	`sha256:300756926f7610e3488ffbfa980040ede17da42fb0925139f370ed8f91642e80`  
		Last Modified: Mon, 18 Aug 2025 18:36:44 GMT  
		Size: 7.5 MB (7486166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab6ac5b974e2afb6d61e0e76c13d1dc418250106c85d5278190a4bd133b39db`  
		Last Modified: Mon, 18 Aug 2025 18:36:45 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:cb3079fde101d72e014b850002568fd129bcb68d1e0cacb193864aca6a344cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261371274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ab80702dfd0d52422f5cee2d2582dd1052b02425c39e72ea5a54086ce24931`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6ab5525c66f1bbcad56e2757390ec72fcf1952e5dc1a6fb67ffb9b8e6bbbd8`  
		Last Modified: Mon, 18 Aug 2025 17:31:25 GMT  
		Size: 125.6 MB (125622148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975e2d300d03c70105a2937577cb8d70ab4e09d26d9c9920af73a732de08db0f`  
		Last Modified: Mon, 18 Aug 2025 17:31:21 GMT  
		Size: 86.4 MB (86403319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105c4dca00112afa5e0e9177e46463056e67190c873f523bcf3ecc3aaa9876de`  
		Last Modified: Mon, 18 Aug 2025 17:30:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:73e9aa13ed66bc871acfa1aec8f76f9e908c201aee5c780077fcf2917a1db9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711b58cfb51f4587d5f18d78678731a9875cd43be05c3352ed75926a778a6d69`

```dockerfile
```

-	Layers:
	-	`sha256:cdcc6877cfbfa0475539eacf405d77ed248fcea81829ddeee33f4e577ea3c4b8`  
		Last Modified: Mon, 18 Aug 2025 18:36:51 GMT  
		Size: 7.5 MB (7478288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a10f3f8f58507c8e82385855bb3b0659acf7d1ed1bac4d40c33a60421c9c6a`  
		Last Modified: Mon, 18 Aug 2025 18:36:52 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
