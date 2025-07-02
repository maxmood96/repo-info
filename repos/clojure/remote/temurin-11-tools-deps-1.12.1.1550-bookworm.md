## `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:ce3115a0be771d0b0b66cb0762dab0cd6033180db4066584913e1ae753af103d
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9464616cd5e09a229688b47f06a849d556de59ae9ee3de6d23933d017cc94430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275123479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a8ee217c1ab2369648eb4f680d404b590a81e8127b57ff7f7ac1329d09d60b`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c75ba428ad6db3248a0423d8d1cde7b29b14fb5ae82fc6db855d0144700c8e5`  
		Last Modified: Wed, 02 Jul 2025 14:49:42 GMT  
		Size: 145.6 MB (145635731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c040b3f3ed8dffd7363c537632a792f24ceb361b329b520d2dbc1aaae83f1557`  
		Last Modified: Wed, 02 Jul 2025 17:14:59 GMT  
		Size: 81.0 MB (80992821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ac3e83e2d28bbcdd833eb36b2f50c880a30bc514de6108bb732669eef9b65`  
		Last Modified: Wed, 02 Jul 2025 17:14:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9d7d6998863b2ecb464f39fe09f8bdc576e9fe6f9369294f76b17d6e216bfe91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a978c614391228add7565bcec5345e61d3b5c3db02aaf065393392bdee66ab5c`

```dockerfile
```

-	Layers:
	-	`sha256:5363f2a6c3a1ba686e618dcade4dc9314b76cd56352234299076d3a41eda3d2e`  
		Last Modified: Wed, 02 Jul 2025 06:35:05 GMT  
		Size: 7.4 MB (7388409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce60d57af170087ef9e7ba5dc025667d56b6f20194c969dcc34eb2b81b9c3b76`  
		Last Modified: Wed, 02 Jul 2025 06:35:06 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c46097a0feffb9799548c114e8ad5dd86e097e798737db5c33c090994645f040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271611644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e665aff01d9e803ecf5194a8689798391b59d5e737d8f75152203d9c25520817`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d77c5ea592f7d6257eba2d5f820d6ff682dec53d5a33f15d78253e59edd12d`  
		Last Modified: Wed, 02 Jul 2025 17:15:51 GMT  
		Size: 142.4 MB (142420716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9749e9c2718950ce5bc647d94e24d9de761985ecb193956526aed47c952661a`  
		Last Modified: Wed, 02 Jul 2025 12:24:08 GMT  
		Size: 80.9 MB (80851500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dcffd54546d9d62928f2e40e49082c544d27ed11ebc6687cde80c230fabd64`  
		Last Modified: Wed, 02 Jul 2025 12:24:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:40cc34c1eba379a0b1c15eb13803d00646c5492a58068205d0e4940ad7cd9123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9967e7efda084227eb9a62df609266d27093e089a106a64cb0ac977c791ead2`

```dockerfile
```

-	Layers:
	-	`sha256:2a00d8e98822a212d877ed3fe91aa7bac006fdee8892cbbe42e7d3455e1302d1`  
		Last Modified: Wed, 02 Jul 2025 15:35:07 GMT  
		Size: 7.4 MB (7394790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182e93ab2e88c1e201310dce2f927daa8b558e6211d4700d656738bd86cfba9f`  
		Last Modified: Wed, 02 Jul 2025 15:35:08 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:21b8a165f678da4c6f84ed2e33aa86ad384171c019e68fc2eaf9db2e7b3fa191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271967639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb781327396c3f3610b784a0775ed1dff59918ccf00e8e684eabba2f856d067`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb88e0eb604515442a1d3c4c17a1fcf57f0a95fb0a8a641f329ce7e3c4fd95a`  
		Last Modified: Wed, 02 Jul 2025 10:09:23 GMT  
		Size: 132.8 MB (132810433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1e537901fdc8fae5bf89429d3106eb9f5fd1dd9f0df1fcf30589616f2132eb`  
		Last Modified: Wed, 02 Jul 2025 10:18:25 GMT  
		Size: 86.8 MB (86819318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f879e08db1f8b16e14901fa3e8266f91ce128e6b23c00c1f73606724a116847`  
		Last Modified: Wed, 02 Jul 2025 10:18:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:104ae9d4370b0f32699c32ca3a43f204d8e754fd65de472183edcf4a0bbb2b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a380cc4b896a790b036b30115fc0d00032fb52aba3117f07ea3d16d193cf22`

```dockerfile
```

-	Layers:
	-	`sha256:b6617df7e9458067c0e322fea755dbb2bfa8b7f16c169c64acf5deb971826122`  
		Last Modified: Wed, 02 Jul 2025 12:35:09 GMT  
		Size: 7.4 MB (7392998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5b66de124168bad8d8e4a078fe9b2d86787adda553254a8f4db108d6fe579b`  
		Last Modified: Wed, 02 Jul 2025 12:35:10 GMT  
		Size: 14.3 KB (14298 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:66e83cf9af73d22c239d19e4c61f0015913d8a90b5e0f0af52b958df1aa256f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252535434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767a8c2b40bf09f408685dfbe2fa428e9456fd6f006ac4a03e238ba8b12ad98`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c6eddb7fd2cb0b6c9d23b14702da84a9d8be39cef62acea8cdb15f9969b1cc`  
		Last Modified: Wed, 02 Jul 2025 06:24:15 GMT  
		Size: 125.6 MB (125586082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3731e88423559d7880c2e88610e0940c0c0a0277d8adcea1262319fb403a27e`  
		Last Modified: Wed, 02 Jul 2025 06:29:44 GMT  
		Size: 79.8 MB (79799422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af071341e5d89a9b1a753f0228ce4cd0bcbe21d8d23c2d2bd25cbe741929bb25`  
		Last Modified: Wed, 02 Jul 2025 06:29:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e1bf2b74991cf40a5925f42f6222511341f5c77107c1a818e362b6a60b02c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df52086e7a76155e50c43eaa79b6ef1ffb86379609150c8e1a0fe096e2ffa22e`

```dockerfile
```

-	Layers:
	-	`sha256:db31ad3bd9f1ea083625a59b1411060927552b12c58cec0ba687a2740dde1e0b`  
		Last Modified: Wed, 02 Jul 2025 09:35:11 GMT  
		Size: 7.4 MB (7379732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691924963896b019b53e0c225f09d598ae95eed86f22989e0dd674eee1cde5e2`  
		Last Modified: Wed, 02 Jul 2025 09:35:11 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
