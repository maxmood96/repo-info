## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:295be6f262a870e944d5ae935ec10e89850edb8976278131b3203b79aa230333
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b504082f25c0be5e333849dd6be997c7a8dd1b8028d53d70755c21ca5bfe706e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280144617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01040371170918b816683c4c6e2b8c1ca68fec1065531172b48ee001c42f224`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e42ae5d0b772429d9b20f12b10d97686887f40b669834dde620a0c787fcb679`  
		Last Modified: Sat, 17 May 2025 13:48:02 GMT  
		Size: 145.6 MB (145635719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe681a48ae73831ce31f7f6b58663e67936e887c7d930b7df5adee940006384`  
		Last Modified: Sat, 17 May 2025 13:47:56 GMT  
		Size: 85.3 MB (85260015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1bfd0432aabcfa39f37ed8dee417ac85ec1d293d9f1f0fc5e051a9dad70a0`  
		Last Modified: Sat, 17 May 2025 13:47:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9ae81abb9b2060a5a43270f7512e15e7ea25d0c1daccdbb5697e674db3d772f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7303538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0117e38a7ee97e3d0060ec50df776d22d4a0d6e58d3028884cbed8131fdc787e`

```dockerfile
```

-	Layers:
	-	`sha256:7706cc6aab25ef0a3611a985d040719d0c142974bfae07cbe42ce02e27b7dce0`  
		Last Modified: Tue, 13 May 2025 17:53:40 GMT  
		Size: 7.3 MB (7289310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:510e37dc49e5c309ec90800cbb0d5e1c6fa495289f59695bfac46b9577877a53`  
		Last Modified: Tue, 13 May 2025 17:53:40 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f79b10da486e0f6023c36b13980e3c0a8b07d942ad2f65aa3728b182dfa37f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277217967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d030b6766f5e84a76945bd34b8adbf05e3e15c8fc7e148a4f13223580255eef1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Thu, 08 May 2025 17:11:50 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa81e2617996b590287af40ced269fbafb204b4143062c93006401b1b1e34c4`  
		Last Modified: Tue, 13 May 2025 17:57:09 GMT  
		Size: 142.4 MB (142420736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08511797091f7ba70cfb208e018a489f10117a9ef8051981eea2b266767efd6c`  
		Last Modified: Tue, 13 May 2025 17:58:54 GMT  
		Size: 85.2 MB (85172467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7da2e7e4560ddbb8c7609967b343dca38ab2d802e3d90fac4adbecc862108b`  
		Last Modified: Tue, 13 May 2025 17:58:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e190377e6423f13fa633dc338fbedd0e62596bfc421b894f297e3c69ad4d3697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7311304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6aef37d4add0be451ef250a189e0e5bf0c9194e978d348981272b90b9b83d1`

```dockerfile
```

-	Layers:
	-	`sha256:4995aff9aa4c523e8fc5e10960c67bc7963c4684df4269efd51ce08db67624a4`  
		Last Modified: Tue, 13 May 2025 17:58:52 GMT  
		Size: 7.3 MB (7296958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65a7039624ac03b851bf876c0a0d72c0439d0405ef1f69fe932132d7e842dc6`  
		Last Modified: Tue, 13 May 2025 17:58:51 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d9c795b6ddf59e3f14ab303a01085b2064c4c2d0439bf9b91004e87e24afc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276625493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05e66f4bbeb22cd90af6b0e7c392876347a8a12b77b2d121540fc6c16096281`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Fri, 09 May 2025 00:28:48 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cae647bc37778358b907d22b7bf35eb9da015bfb7b8a8800a879a20173b410d`  
		Last Modified: Tue, 13 May 2025 18:34:18 GMT  
		Size: 132.8 MB (132809833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b624595fee2e9c5cc6b200917de575903a351bb8e157dcadbe4de1187bbdff09`  
		Last Modified: Tue, 13 May 2025 18:44:17 GMT  
		Size: 90.7 MB (90742462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925061405230820572745f5e9add62419103ce912ea4d03f2429ab40f50fd1dd`  
		Last Modified: Tue, 13 May 2025 18:44:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2e25556fa9b99226ae87a3699376870f257f994dcb44815e60a7a916cd15d787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7307222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdf1c46dacc1f7419752ae8dc0d0a0ac0a4b0d058f9232c1991bf9e2f07253d`

```dockerfile
```

-	Layers:
	-	`sha256:89bf8735cbb7ec79f59d5c2784b047b0e0b6143b0b9834e39b233158644a617a`  
		Last Modified: Tue, 13 May 2025 18:44:15 GMT  
		Size: 7.3 MB (7292948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe57ed7bac4d6542d792b35caebf8e6e858666d1f9617b237bc739c6be84fb0a`  
		Last Modified: Tue, 13 May 2025 18:44:14 GMT  
		Size: 14.3 KB (14274 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a4eef1560913a8fd3baed3a13d3adb16e2262982a4e0f324450a176f5d12f855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261242523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18918960c58b4540f051406643a7b4a1cb9490ead14739df1d508541ca055f6c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Tue, 20 May 2025 02:46:00 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30965b6dc7dc6f235e602cd0f410e0e3efa7a40e49d969d8b610ce2a574addf`  
		Last Modified: Tue, 13 May 2025 17:59:51 GMT  
		Size: 125.6 MB (125585838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6e542e85b6caef9f0277018847abd311645077f4f8abeba1da9fadfc6de0fc`  
		Last Modified: Tue, 13 May 2025 18:06:14 GMT  
		Size: 86.3 MB (86339395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e213a3b64f85198203d612b46d95c370b4f2255adebb05f7fc2d4921f0dac3a`  
		Last Modified: Tue, 13 May 2025 18:06:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a1aba50eda37531a3bbdeb6995ed8efa5474948b0e4f1b3b7f9d5438feba34bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d152afb5805686fd95463034d1c8a42b43d49a2f0b3aabf34cb42061b9b30df`

```dockerfile
```

-	Layers:
	-	`sha256:4fb11e0a2eb15106cd51c9b5458e69a71da4c19493122489fb64a2995c4932b1`  
		Last Modified: Tue, 13 May 2025 18:06:12 GMT  
		Size: 7.3 MB (7285236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff14829fb2a9ffbb069b0f392f5a2f13dd91e859d7314e174ddf766e7c7d0f2`  
		Last Modified: Tue, 13 May 2025 18:06:12 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json
