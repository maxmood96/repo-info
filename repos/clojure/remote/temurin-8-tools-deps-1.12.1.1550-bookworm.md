## `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:a0ae948525c54596b058fa51a8591803a4a4b6e6b44d33ef43c9640d712e4659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c1897b02daee1ee8cfe5ed70c5307e8fa882cd19cb16d5d2dd9014520f6c1d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184220274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093560a717bc2a1fcb234ceb81a652a2bfeb0df90314c366da824044a1d7e1e8`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175de387389123125d6e72c759b57aa10799fe9f906eeea4bc850e6911af8bd9`  
		Last Modified: Tue, 12 Aug 2025 21:34:44 GMT  
		Size: 54.7 MB (54731347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0f19e7087d9556bc5c693a961d5ca1f8b1f046a2ab9f1b12494f123341ef55`  
		Last Modified: Tue, 12 Aug 2025 21:34:46 GMT  
		Size: 81.0 MB (80993772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df094ece11ae8564cc8174bfce25392aa77cfcb2e0a74feb07abb959cc5164`  
		Last Modified: Tue, 12 Aug 2025 21:34:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:14f7d5d4e9e8f20cf50d60fdba0ec34285bb387cc0255aff0d87c7eb7f88d7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f032fae2dc78e47b115efe503ad4da58b030472d60e212f36ecb0d8d5eefa58`

```dockerfile
```

-	Layers:
	-	`sha256:3bcf38fcb10fb440263bbb44cd549f1c298aa22d30c52f5541d9f4ed0c703a32`  
		Last Modified: Wed, 13 Aug 2025 00:41:33 GMT  
		Size: 7.5 MB (7489878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad515e5add7284d84c6c59197083e369309ec8f4d58f8475fdf391c6ecdbcc07`  
		Last Modified: Wed, 13 Aug 2025 00:41:33 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d6560b21c909934a0272e52997b6d3542661da802c218c993fd07487f8aedb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183047072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084ed413da36adce70592c220d7cb8cfe6329cfbf112a260d398ddb4d4284fd0`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d9af38b492ffb24e2d9a0e37d3ea9b006cb4dd1a87237a01481f2849be0b22`  
		Last Modified: Wed, 13 Aug 2025 14:01:04 GMT  
		Size: 53.8 MB (53835638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f447df2d5725ae65d2c0da52c1f67bd3cf9ec70aae7a22dab9557bd60bc7a1e4`  
		Last Modified: Wed, 13 Aug 2025 14:06:04 GMT  
		Size: 80.9 MB (80868340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900b98635aa719783279dd493fb68c6661719b8a1cdc448a06bfe2b0b4943fc7`  
		Last Modified: Wed, 13 Aug 2025 14:20:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d439403553cf4643acffcf156374dc8d28942671244982ef4dcddc78880ef9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a48875676f2e5c3c41da23a72450e4a989a5a33e9bd9f5b143668caa479d7d`

```dockerfile
```

-	Layers:
	-	`sha256:bca75236d74d612bbd76a615368c8bb8ea36a1ac329f26815c674a9a89276308`  
		Last Modified: Wed, 13 Aug 2025 15:42:07 GMT  
		Size: 7.5 MB (7496339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c67000d9a137a6668a9acb32830a7f86dd3df335fe44d19b594abffcc80565e`  
		Last Modified: Wed, 13 Aug 2025 15:42:08 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cd00e7bf6ad5b64b9dc85c73f850230112bdc50c9e2838dc280de1a64a7176ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191326462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6926812e969adb267b760a47b20c6def7efc2c68407697cf5c5e0e3b8331cefb`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc42a6d1e590d9eebbffb4c44e3f469a4ec105019325cbeba3b34793b02e58d`  
		Last Modified: Wed, 13 Aug 2025 19:17:00 GMT  
		Size: 52.2 MB (52165424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfa6e49202c5601d171e756a70cb434fd5a93fe400378b6d65888f526053a88`  
		Last Modified: Wed, 13 Aug 2025 19:24:33 GMT  
		Size: 86.8 MB (86822316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb946a1d0010eb51dabb4f67545bd1c5f5211b000d4552ead475db80b7ed4e8b`  
		Last Modified: Wed, 13 Aug 2025 19:24:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d9a0371681d22bc331ecbaa8b2c4ab9ee9d753b09851fdf7acdc4414a8c8d8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0607df3506756ae70db488a6c110214387951999dbd3c8cc9438c8174a819d7`

```dockerfile
```

-	Layers:
	-	`sha256:c2ea83d867cf844e64d7ca08428b1a28ada41ef7773c6a2900ea21fbf67833a4`  
		Last Modified: Wed, 13 Aug 2025 21:40:26 GMT  
		Size: 7.5 MB (7495675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6192ddca1a51e2647e07a0ca3481874e51fbc811366dd154e210522be66e1fb0`  
		Last Modified: Wed, 13 Aug 2025 21:40:27 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
