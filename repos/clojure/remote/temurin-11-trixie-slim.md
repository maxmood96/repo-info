## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:c924c71a5d4fe36eab17bb53d2cea4a0cfe85a7119db7abd401073367e93ba80
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:17d67b9c4dd46a12a789d1a7030cf220d52a5667d92689a1a18074af9521a2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247714259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeb9321e4d0cb69192af19df11e904bd6af9d12ace962056313d9a67eb81dee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:57:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:57:58 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:58:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:58:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b833aacdd2d434f2182e4a118b77f818d247af59acdc41d54936130f1f1727a`  
		Last Modified: Tue, 19 May 2026 23:58:33 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3789f1fd383229b81d3f57c9393af8a58f8a681f7207913d147d0b4c48648aff`  
		Last Modified: Tue, 19 May 2026 23:58:32 GMT  
		Size: 72.0 MB (72047426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce3bb56bd20b9036b787f7436811ed1efae32a8334f5a89affe730a05124611`  
		Last Modified: Tue, 19 May 2026 23:58:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97cf04a0d5d820c6511325dcefd2c3a2370e0fc7b30eaac85ca88efdf567158f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb0a09bb0321f76f46b530a13600b197f7c9af0943ae7038344222f1fa5c5af`

```dockerfile
```

-	Layers:
	-	`sha256:ed78dc1168dba00179709766e5b726add4a6d4e2dcd587667316110b13f0d740`  
		Last Modified: Tue, 19 May 2026 23:58:29 GMT  
		Size: 5.3 MB (5279483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14bb28e883148257a3bbb2b9823bc617300eae2c0bc5ef98005e95428c709a41`  
		Last Modified: Tue, 19 May 2026 23:58:29 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4609bf29eff1e81380f6c9405d961bb1f29893359a56bd2fb7a0bf88bb9a4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244596039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7f8a2cd95371edd98b82547e97d93e707e4eb88c8938437e6e2d44727e90b6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:05:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:30 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:05:30 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:05:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:05:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeeea6720a2b32a9dff6ab569738bf7d6f0966d49e556d5690388a60e38bbb9`  
		Last Modified: Wed, 20 May 2026 00:06:10 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd07eb24c6af518094294fa6cdc54e5d3d9eadf0f705605e779d8b972f1bb3e`  
		Last Modified: Wed, 20 May 2026 00:06:09 GMT  
		Size: 71.9 MB (71871245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe0eb8f4af74c0ded1b7f1b1bcf0b3760990a3fe3d406ece315b7b2a829e15`  
		Last Modified: Wed, 20 May 2026 00:06:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c87e39150db21e33b615c8d2b6be7342e86d2b42ffe47514bf79f0772ace5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d32a81676a0704f23369db8e0574f7e645080ec9d4d2288418376298f323f1f`

```dockerfile
```

-	Layers:
	-	`sha256:c095dcbb221936ed4d53238cb5ac883f05fa65c188cf92f83a3726242409f4a4`  
		Last Modified: Wed, 20 May 2026 00:06:06 GMT  
		Size: 5.3 MB (5285862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a63ffd5dd61dd189ea2cf78a4d87605962c7b15bf66a07311f2531799c4c4e`  
		Last Modified: Wed, 20 May 2026 00:06:06 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a06112d7a790986852fab7534339c7842a2bd7b5b9ad70c14b5ef8c67ac77803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244164515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757c845ff7eb38f0080fbcc135029bb65c8620fd0322ae74b05679dfb7158678`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:45 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:26:45 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:22:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:22:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:22:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96ee5b4d347c9b3ee6f86dcde18c044f7ee128c0ca544845fafbcc3bad0c1c3`  
		Last Modified: Sat, 09 May 2026 02:27:49 GMT  
		Size: 133.1 MB (133110179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6481e726fcbce8985d9ef871fa019cec438ce11ba352b263db3829d5f3de8261`  
		Last Modified: Fri, 15 May 2026 20:22:47 GMT  
		Size: 77.5 MB (77455602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012a4cc5edf76685fdc04bb99ec4ce8701d14f4cb3d53ae9f6b2936ced69257f`  
		Last Modified: Fri, 15 May 2026 20:22:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65a6544a976c7397ba78c8b9d82c674c0696a9f6e0f440648112b219251d17ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d4418f70ea001a995469459574e7c1bbe4f3c1fceabc3dd19e73de15159329`

```dockerfile
```

-	Layers:
	-	`sha256:77422c8861229e713a1be1b1f4233399e97af309e5d91fc21cecc4ae0476f29f`  
		Last Modified: Fri, 15 May 2026 20:22:45 GMT  
		Size: 5.3 MB (5283125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699a79bb8faac7f4ebfd8bd589ce41734a8bd1c386b57f317f56b5619428c237`  
		Last Modified: Fri, 15 May 2026 20:22:44 GMT  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1a626f44467825c61025401d161f08da865295ceddfd7a8e40287f7cf7e5e599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229507690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48909835d53beb1d45be96d390cc84055d230367455e58201ac35a5ab59c2f59`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:47 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:47 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301d03359195b2db4e16ef3d853eef1d64ffe78f0949990c433cade4fd354430`  
		Last Modified: Fri, 15 May 2026 20:18:36 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbd4bf7e1200a07e20bb9e7daeb32b5aca93c4012904c44850a3ec1c51c5dd4`  
		Last Modified: Fri, 15 May 2026 20:18:34 GMT  
		Size: 73.0 MB (73014962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efb4a8ebcfc0e455fb88dc2743b8842b269050c2aee3468a4d22d2ebdb9383`  
		Last Modified: Fri, 15 May 2026 20:18:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0cf9e3ee0d17e2172febe5d69867cbfc2a404167cd1d01a403622e8f1bad4874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689d53c210853473ca46fee538b93365d2c925db011566cc5359f73eceb89fff`

```dockerfile
```

-	Layers:
	-	`sha256:92864466c07ffac746f99d647062b7fd53be0bbfeea89780f050238ac96e784a`  
		Last Modified: Fri, 15 May 2026 20:18:30 GMT  
		Size: 5.3 MB (5275297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f741d9ac94049679565bb556c84c7ede90f8624f030658ea9aed19196e1883e`  
		Last Modified: Fri, 15 May 2026 20:18:28 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json
