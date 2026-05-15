## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:798677cc0681ca09f910ff002770acff0a62bace50456970791a0ec4875a6c75
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f415d2aec1457e8b2fa12e69484cc2f1bc625861e39cad9bcadb9a8c68244a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275589319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea218a7a13c2a17fbb17c260d3968399178bf24ca93a4eda3470d75b120c2f6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:13:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:48 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:48 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3661f1d84aaa134a6c05a2f76a44bae8b31d75de246183b995ff4a0b38d2abfc`  
		Last Modified: Fri, 15 May 2026 20:14:26 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893bbbce66060472105cb402db3e24cdd21ec53eb831642930b00c6fa25dfc8b`  
		Last Modified: Fri, 15 May 2026 20:14:25 GMT  
		Size: 81.2 MB (81213733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccef674b979eece589eea51d98d1fec3dfc7720c5ee8892a5eb36cecb055cf6`  
		Last Modified: Fri, 15 May 2026 20:14:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c0c7e501733cf778cbb970525e30e7eb6a5159fb020286932d5f5f8fcf92270c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43605715dd984a4031ef8ed7b5f5322442f34c2e84be0495400fd68091612561`

```dockerfile
```

-	Layers:
	-	`sha256:f9c72d069d956d09811d3a53bb9f89500effbc114e64c8074b891936c2fadf04`  
		Last Modified: Fri, 15 May 2026 20:14:21 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e81acf5a6af2bb9f1e5d50aac52c63894a72a79e7091b654be53dd0deaad779`  
		Last Modified: Fri, 15 May 2026 20:14:21 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bea865b20d48af71dc7dcd02499c9057e9c238370d2485c24b31ca8c452e76d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272150473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c240e9ae5daa976a0b109837b6115ecc5aaf0b667279811d4aa0288a4139f7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:13:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:40 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:40 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b4ffa9ce449308c8ed7b3c3f9bc80c4bf64524c9a1d2245475a0d218afa9b0`  
		Last Modified: Fri, 15 May 2026 20:14:19 GMT  
		Size: 142.6 MB (142582199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776e701192a8b73531ba262ae5080f769d6cfc60d3dd770c2a1bb17b40b0c24`  
		Last Modified: Fri, 15 May 2026 20:14:18 GMT  
		Size: 81.2 MB (81194477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad43b6cc4e22510853e6db12f61ea6a0d64f9ea6b8e9e3b0081d321251e4e52`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d600d20daed3a00fc1ffccc6fe837c942293d3b724f1bb9591a4aa70fa7c5f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfebc65c2b3d70ccb2db09454386e29fd56062cdd9eae1a3f1686a9411e538ac`

```dockerfile
```

-	Layers:
	-	`sha256:0e2975ec510197ac6fc5e95607ffe9beafb760e186a6f50ffd4dbf69772f330e`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d6666e2865f7a586f0ddff477b9480d4f91ab801d91eda1521137476d4f96e`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 14.5 KB (14480 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ad71579b0a39252fa9d465664cfebd33b256ca1947be05aca60dc1bc5fa32a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272480967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb616e69751cf88e8ca13e4f6def5a8db909dcad24cb776ace4b4543f0b94cf`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:25:03 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cbaabc187f4e33faa4937073e6b8d37c4b4ee8836b24edba986c27660880f2`  
		Last Modified: Sat, 09 May 2026 02:26:07 GMT  
		Size: 133.1 MB (133110168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2b6d4d875c4b9e472651f2ac7937e0f343a7c36537581ea54dcbf08d0638e`  
		Last Modified: Fri, 15 May 2026 20:18:29 GMT  
		Size: 87.0 MB (87033365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243527edf726bd337d3bbf0233e9ee9b4c1220f99f67d2358812d118d471d896`  
		Last Modified: Fri, 15 May 2026 20:18:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c9c3a5e6a90174ee7b17434b3b1cc430ab72f45ae881419420b302f319da73a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e012574e247da8b3c66fe94c0deba7c9e993338c012a7e88a2bac03d2d9266f8`

```dockerfile
```

-	Layers:
	-	`sha256:5c80bfc9b27ba86312fe2be2838b7cc83f5035bdf233043490ad5ea2cf6fb19d`  
		Last Modified: Fri, 15 May 2026 20:18:27 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48ec215bd4a75123942f9ee58130a6a8e840ca18d4ddc4d70bdaf7bbe7690d9`  
		Last Modified: Fri, 15 May 2026 20:18:26 GMT  
		Size: 13.5 KB (13456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fe4d8373ad1b5a128fd7da96954db805d6807832fcb192561821dec84b74894c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253825767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284c1087f036282200555891a05963f386f8b7e363f1d2264b7bdee1f28cd811`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:32:15 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52372d5fb2e4448599149f5fdd18e1d6933ee7757f50701f6b69d3caa03696a`  
		Last Modified: Thu, 14 May 2026 23:33:05 GMT  
		Size: 126.7 MB (126651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321ceea7ad7f84a7e5a6ae84c96b339fc1997ccca2d9b23774cdf1dce56bcb7`  
		Last Modified: Fri, 15 May 2026 20:14:17 GMT  
		Size: 80.0 MB (80025378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7264922cb08a03539a1a09b3ce8dcb79e62402cfa2033a0a48b49efc5ef33cc9`  
		Last Modified: Fri, 15 May 2026 20:14:09 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:df9b4811c519a6aa91882687af8f43c141b62393abc1c3b4331291982c656ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b28584aad5800a1c1c71adced07e47b44a6bfeda7d8047eacb9d63cd4b28f`

```dockerfile
```

-	Layers:
	-	`sha256:8e994ce011c7348eae3685edb66cbd83e92bca2afcc2e771a80063b7c75589ca`  
		Last Modified: Fri, 15 May 2026 20:14:14 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:299cc4c22b150a6dab2a076d8ace9c3bd480dded54e97e2c8e8940a43043269d`  
		Last Modified: Fri, 15 May 2026 20:14:13 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
