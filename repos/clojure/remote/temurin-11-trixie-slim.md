## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:eba28a3e3852f7642b7467ff43be7a3241097166ecfa2aa2c3ff321b4b57c620
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
$ docker pull clojure@sha256:2db1cdea6a9f03be6ba1323415df5b77c874390b8013ee7d8938a356dc84907f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244177754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c274a6d0df13b14cf1aaf0522fb9bee712075a721f36b6756f791ae26364`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:50:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:50:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:50:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:50:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:50:04 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:53:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:53:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:53:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af1c2a52fcf12729088136b65ef4038671f55a12f26a215e7c24989df640e8d`  
		Last Modified: Wed, 20 May 2026 05:51:10 GMT  
		Size: 133.1 MB (133110217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960a5c36c79a8ce8c15dfd53a1fa42fb3b3273cff9550776c72dea0b13205c15`  
		Last Modified: Wed, 20 May 2026 05:54:09 GMT  
		Size: 77.5 MB (77466438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dafe2ef38cadf6c2e08a92fa0fbbaf31c458b5a23bddb56733394fd07380ed0`  
		Last Modified: Wed, 20 May 2026 05:54:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:adb1b18efc66e52a0da8cd22eddd185c8e8c5fb0ed71315991f9c5a1320c558c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b52d1eef289f0b6b83bbed8e338c76f9c4d02800998d2d4d152e9c5ff7e8f`

```dockerfile
```

-	Layers:
	-	`sha256:16adf78f681254e577f4085b16fed4e9451df6a2b28873ee50b2c25599f6d604`  
		Last Modified: Wed, 20 May 2026 05:54:07 GMT  
		Size: 5.3 MB (5283239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb734a298672958561a99ae06bd3b4879c468e8f10595f57391b03197688e7b0`  
		Last Modified: Wed, 20 May 2026 05:54:06 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:bde7530c96c140dabf53fb0c471f386f24dfce8a45d7b72ee0c16c0d32514f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229526967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabf91e421693e107bb514840dcd139cd085f8bf7250169ccbb0034529185b72`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:42:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:42:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:42:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:42:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:42:01 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:43:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:43:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:43:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389166517857b01275246c592e1b1023d8f38bd4a17cfadfd10346a353b496e`  
		Last Modified: Wed, 20 May 2026 01:42:44 GMT  
		Size: 126.7 MB (126651734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af450966ead5e91387abedd85a2315d3e310e76eba317fd6f9f5504562c68120`  
		Last Modified: Wed, 20 May 2026 01:43:45 GMT  
		Size: 73.0 MB (73028665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1988cdfb20ed833b30aaf7f324ca3b6053ab30236cdc71c91544303690a2030d`  
		Last Modified: Wed, 20 May 2026 01:43:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34bd894c011ad0cbeb721dbb279ae1dfcdc7dfaf3408f6a6539137a743ac9cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5288852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80335135447d153806c7f949761087790578cdae942058fdf464e93dc1f1dad7`

```dockerfile
```

-	Layers:
	-	`sha256:6646f1bcc097baf3cb182d0c6d04c8b91638000ddbd2fa1722f63b7c9cccadee`  
		Last Modified: Wed, 20 May 2026 01:43:44 GMT  
		Size: 5.3 MB (5275411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d93f6e8d7709ceac19063992f8f679df35909365d662738d811aa5cf301375f`  
		Last Modified: Wed, 20 May 2026 01:43:44 GMT  
		Size: 13.4 KB (13441 bytes)  
		MIME: application/vnd.in-toto+json
