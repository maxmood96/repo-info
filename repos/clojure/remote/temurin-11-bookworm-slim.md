## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:2ca63461621b0e4201531fe0714ce6bbc2438a28930837cebb8eeab64712e145
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:545bb79aa5b87611c7f705eeb0b2278f55e39230a034d29138ece719bad7a6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243469203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d55b9d18852bd07b0e72c00b4f65714deb72070d2e51749acf43d7e88e6d255`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe607e2a33ee3b8787e79339dbf75ae1703b50eba47a1aac3a78f9dd6538f51`  
		Last Modified: Tue, 19 Aug 2025 04:11:51 GMT  
		Size: 145.7 MB (145658140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faceac38e5f987d7ecca6f097bfe04a30c71eb22b000decabf7c1eb19a2c4514`  
		Last Modified: Tue, 19 Aug 2025 04:11:48 GMT  
		Size: 69.6 MB (69580162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f727ed18673261c9094ac84e10c5631232573003096aa251b98fdde02c69243e`  
		Last Modified: Tue, 19 Aug 2025 04:11:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35ec600cfef5457d6f19c3d5daa5adb52b80454edaeb03e283b1a8f1a8129abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4307f8f0ee7dab5891deb68d92d36d3b4ba438f6794d15976f9be139d6d62ef`

```dockerfile
```

-	Layers:
	-	`sha256:e35d7c143bc5fd94ba59b6aaeb3a243368e3e9ffb153c60c6fb34efe6e78a721`  
		Last Modified: Mon, 18 Aug 2025 18:35:07 GMT  
		Size: 5.1 MB (5131414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6c2e51aaa2339d2d48d29a5bf86c11a04aa321b9d5dbd38e7d1691efa85c86`  
		Last Modified: Mon, 18 Aug 2025 18:35:08 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4a38e432bf77bc20ad6962c94dcc5240240b0066c3c9a17861caeb146f804460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239995946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689fdf01923c631e04303ebeb01d40fa74cd3d1a93014aa56c5834b872012cb6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f170599e0d0d7ce8452567f601dd39705883bb1c67f4c2b875ddcbef1651e1c`  
		Last Modified: Tue, 19 Aug 2025 04:12:46 GMT  
		Size: 142.5 MB (142460571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d6cfbe36b70818b6a992e98aaa88fe5e232a2179b6805a4919ccd949c8c8c`  
		Last Modified: Mon, 18 Aug 2025 17:01:03 GMT  
		Size: 69.5 MB (69452726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2257ac01c078f0c5f176cbc6649a1fbb684b315467e5ea0d5755b2ce6bbfda0`  
		Last Modified: Mon, 18 Aug 2025 17:00:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6875a6fe491d9d27c261d15a9397bca9835efb6386014609286b0ab81ea98045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f607763bb4e24e74a6197f951a702083a65801641e251bd9c415745a3dba8e0`

```dockerfile
```

-	Layers:
	-	`sha256:acf42a9537aa0acf7da2615f91d06021e7cf4d1c7efb8b466cf02392a6109dc3`  
		Last Modified: Mon, 18 Aug 2025 18:35:13 GMT  
		Size: 5.1 MB (5137793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7988d7c878fb2667b9aa72593a8cc442248ced32b00de64d240348add9ceae7b`  
		Last Modified: Mon, 18 Aug 2025 18:35:14 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:32a5f45058141541e4b0438c714c58970ff66b814cf57ddc9ddda8b826e7bffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240333879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32f0c3b79a4e2d7ecc4899e039c21b555977c6372ed4c515b574c9809eb9fbf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46561d416a7c35ce0f5f369f09b10c84d52b854df0532c3ee5a10948491d390b`  
		Last Modified: Sun, 24 Aug 2025 07:12:04 GMT  
		Size: 132.9 MB (132853303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad4ae7896ee9aaae8e82aa000d9ad0729b0526d5f932a9f74766863e00730e3`  
		Last Modified: Mon, 18 Aug 2025 17:09:18 GMT  
		Size: 75.4 MB (75406509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd003cb73b330aad508025d29a248199c59ec78f47a4ab16c43547b19fbfa3af`  
		Last Modified: Mon, 18 Aug 2025 17:09:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f169aefdb930131a3cb24114d86a16b5bc6894b386b9e8d229d4c135542e6082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf77c837128cfcd466db8128393eb126bf357dd48a85e7621d7e073068bac1b`

```dockerfile
```

-	Layers:
	-	`sha256:52060e2a98c044fc6f95f4f096032c4e332bc6533d251448027e73f33f65d26b`  
		Last Modified: Mon, 18 Aug 2025 18:35:19 GMT  
		Size: 5.1 MB (5135957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2befe76be2b2b1cba35f836950f5e646ce3b2b842595558d1c894f078f4ee2e7`  
		Last Modified: Mon, 18 Aug 2025 18:35:20 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:47c17b39fa8a3b1a0efd3b04710e51e3c71d48755a7dca7995b7e6712b148b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220898714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d6b8faf108edf7cf55b313cff6d74ad58bf6b881e7e0610d20643b619e696`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae251331425e0189671e4f2efc07cc0c01261608ee3bdd189f86daaf400b4734`  
		Last Modified: Sun, 24 Aug 2025 07:12:26 GMT  
		Size: 125.6 MB (125622148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc1a3a0f36bc4c7fba8ade6beb800ad666c16846f56bfb5d80085830767d14e`  
		Last Modified: Sun, 24 Aug 2025 07:12:22 GMT  
		Size: 68.4 MB (68388082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b24ceb294c5e834e6e36e790dcfecb6a05c2b3a99aff8e227214905246c9ee`  
		Last Modified: Mon, 18 Aug 2025 17:22:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7509a83c3831e320b69b756f7126aa4f646d63ced68406b6f3c891112c5cb067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975addc699578174c31cdd36cc3ad0e04fb057d8ea3e6aecffa9c8f81790d703`

```dockerfile
```

-	Layers:
	-	`sha256:d908148c55037aa6c4fda8b250fc650b50eccae1ff8306107ed7274aef281f9d`  
		Last Modified: Mon, 18 Aug 2025 18:35:25 GMT  
		Size: 5.1 MB (5122739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0086848397d23ddbd2d85609b71e1bed02c79a606593787a704bf240e26e502`  
		Last Modified: Mon, 18 Aug 2025 18:35:26 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
