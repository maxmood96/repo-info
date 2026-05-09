## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:e17d86a10d567c34b35c0a9e7f8af40686aa67cb53dd2717f37bb15d09761441
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fe77af9feea59887346fb313a7c188c7ecbd54ab2854631de992baf09dc32837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293040768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119a175797f440ba814bed81731af20fc1a57a2352fce6eb9ea17ee8620eb85b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:20 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:20 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:18:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:18:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8249cc346ae534d0699e064d3e8f3917f467c90bfc2ed0bdc18f63738a9196d2`  
		Last Modified: Fri, 08 May 2026 20:19:02 GMT  
		Size: 158.2 MB (158166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acca773762631c05cd73575bc5a7f9ad3b96c22dedd4732e4b72bada0b688927`  
		Last Modified: Fri, 08 May 2026 20:19:01 GMT  
		Size: 85.6 MB (85570468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42cbb5d719873cc8d1488cfdff2c37e5c62fe4fa7cac2d5f55696664b0ee454`  
		Last Modified: Fri, 08 May 2026 20:18:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15b7460167ad72b39a9080f4dc44eb7d7d9ee0ec9f7f1c8af56d578df357dea`  
		Last Modified: Fri, 08 May 2026 20:18:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cefa4a31811a0f8babf3640eee10d9e1456201352f841f6e678acec2e1c95950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a35c4c6a2e59adbfaf143b01cbdc6255c6cc19806fa2ef1344abd5ba0543ab`

```dockerfile
```

-	Layers:
	-	`sha256:ab372cf10ab242437a1c081b04b6065f089e1ff4f2a3db4ace55d751c22cb570`  
		Last Modified: Fri, 08 May 2026 20:18:58 GMT  
		Size: 7.5 MB (7473200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bf66542b427a8857c0a07276cdda207367b772f33295a557b26f13ec42097b`  
		Last Modified: Fri, 08 May 2026 20:18:57 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2126f971dfef28c9670d5f5099b7f5a3631c096ad9158488ccb8101c118a3cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291515116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c81c150128f0969e34576652ce0b5047f2688aac41d510c2ececb6cc8e08ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:22:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:22:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:23:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:23:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6ed0853bf0e4a5824a4a76bb44b9c61b4fc08fd465c1d00a3007c467c2e5d5`  
		Last Modified: Fri, 08 May 2026 20:23:34 GMT  
		Size: 156.5 MB (156461190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd8aeb281abef560f717723530db5dc4bd22405fc49ee12203b6ff20c15233c`  
		Last Modified: Fri, 08 May 2026 20:23:33 GMT  
		Size: 85.4 MB (85383439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99779a72e27db8a94eedf21a9db7fd150da0df553c15727cb28dd2d8dd67dc40`  
		Last Modified: Fri, 08 May 2026 20:23:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac720e652824413253da62160e37c9f8e6439ad440c8682e0a6f84b9d1612662`  
		Last Modified: Fri, 08 May 2026 20:23:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7ea481ac227e40fb57158fbd79e89787697e52406eb1f95627ce532c07208fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89ebcb6772ae012f64253996b022d550057102e14b6dbc9ea38bb1366e5cfe5`

```dockerfile
```

-	Layers:
	-	`sha256:804d46c7435399d5a09500ab498db4a00c7db0be47c7a9fcd6a1773cfe8ae5f1`  
		Last Modified: Fri, 08 May 2026 20:23:30 GMT  
		Size: 7.5 MB (7480230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96363c0bdf87c951ec1dc4229e6b3a4cb48bb7b0b9895d7fc21619732cea2d5e`  
		Last Modified: Fri, 08 May 2026 20:23:29 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:70c2630dbeb41741ce7984f340a44cacf79a6132a864e046a932ef29575b6aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302453615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3896e832e1b6bbba19218e0905a6d94f089d61701c8c9894ca2e94596b5d751`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:38:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:38:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:38:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:38:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:42:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:42:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:42:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:42:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:42:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef2aeb89dd432248a27be9658c9ad2fe8736e1bb0a40602c7b1b444a977ed1e`  
		Last Modified: Fri, 08 May 2026 01:39:21 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e4ef72133a6c9dd402973c479574b5d7cf184082f20abb89c47f9a3ec02ff`  
		Last Modified: Fri, 08 May 2026 01:43:17 GMT  
		Size: 91.0 MB (90986352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed836d8ee30823a14faf982ad9467edd66a04ed488d3121e9b24d73ea60d48e0`  
		Last Modified: Fri, 08 May 2026 01:43:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc1cb60dd07f4ea1625f8741262d4afc2ba4c39b0eecdda0d27788d1371d801`  
		Last Modified: Fri, 08 May 2026 01:43:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f8823656ea24b2ea26ce6a2a44a31cfe2ea33f5f117ebb705f860008d0df5c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dcd2d252a19ff68de95344d1b7135d367f2cc91163c3cf81379ebb06580ad9`

```dockerfile
```

-	Layers:
	-	`sha256:4a1a2c87f3a9dde89d13096b0b50d7e5155756dbfee0b0fec59221c15d70a013`  
		Last Modified: Fri, 08 May 2026 01:43:15 GMT  
		Size: 7.5 MB (7477621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca05686a224b995e61f30bf079969214b2cddda8b9769635a6441acf3b708c4`  
		Last Modified: Fri, 08 May 2026 01:43:14 GMT  
		Size: 16.0 KB (15955 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f00c43878ea30a2ef5ac0f5a9325c68bdf2a0705dfc1ee83bbd2c8435f614601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289476031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d1d7e7d50dd759bf6afa5677cd47dd8668dbbf479bfe8f3bff312daa7c902a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:09:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:09:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:09:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 18:09:44 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:26:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 18:26:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 18:26:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:26:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:26:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d4384d0aaf4c67d90bf2e07cb4852bca10fcf970d4b6c61ba3f1acafc7915a`  
		Last Modified: Fri, 24 Apr 2026 18:16:13 GMT  
		Size: 157.2 MB (157216912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0585ff758ed9b6f7c69ee80876dc8ccfa843986d0b4810fb359694b00051290e`  
		Last Modified: Fri, 24 Apr 2026 18:30:35 GMT  
		Size: 84.5 MB (84459862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aafee907925dbbe870efbd4c95cee231f6e6c351b8c93c053bda55a6578b402`  
		Last Modified: Fri, 24 Apr 2026 18:30:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd7bf6aeb2e5730a778806e4ef412b7438012d7d98b8edade956df1f21a2354`  
		Last Modified: Fri, 24 Apr 2026 18:30:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:79da2da682da246290a5d26abbbaa3cd34dea6e39ee17d77912655573f406ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f340a044f0cacc14425b1c5a610c0acf85d788ea8a0cff08cd112436ae7b1fb`

```dockerfile
```

-	Layers:
	-	`sha256:7c4014697035fbbd5ec26a2f1f701fd4bda684eb6607252f20ae3e30c63bbe3e`  
		Last Modified: Fri, 24 Apr 2026 18:30:24 GMT  
		Size: 7.5 MB (7460488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb95f6f40cf9fe59c017b42383d2cda3dcc179824bb14363db66e2451eedc6d6`  
		Last Modified: Fri, 24 Apr 2026 18:30:22 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c6bb61b133a138e8bbfc8f1f5a242d3104e7f145463bb833245470d491483b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283307104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b851970e95ce838e50b620a903547956431472a112d10bf5554f1a697fb7a6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:17:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:17:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:17:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:17:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:19:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:19:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:19:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:19:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:19:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322bcf3d705f2cea437ef1917f9da7ff28c4e9884b7d8a103b1f9bdb9098e5dd`  
		Last Modified: Fri, 08 May 2026 22:18:28 GMT  
		Size: 147.4 MB (147388345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db70941ddaea984b2b55f11964338e236b20d069519e79d03aae5fdaf76714e`  
		Last Modified: Fri, 08 May 2026 22:19:30 GMT  
		Size: 86.5 MB (86545412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee0adec9a014560e6a0e7d6eb2cd023de447fe1f284888b26709bed46b923e6`  
		Last Modified: Fri, 08 May 2026 22:19:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d2ce495e9bdf1de81c3dbfbbef0cf9c6d0027bcb4329685c9ce84882114acf`  
		Last Modified: Fri, 08 May 2026 22:19:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1cdb1251115490bebdb45d58a1e3a8630efaf89a935a30fece7a2d650bd1e06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2c158c5d226161ec8fe7bbab1b731e1eac9ff2e1d68ffc6cf0637d90b27e51`

```dockerfile
```

-	Layers:
	-	`sha256:be4c766c193a2c4192f76da7ac4cf8b7123f4ee94e783abf68343d59dcdcdddc`  
		Last Modified: Fri, 08 May 2026 22:19:29 GMT  
		Size: 7.5 MB (7469122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36da0480371bbd7ad756eebaefb161a424fb14d489e1ff5be167477acab65207`  
		Last Modified: Fri, 08 May 2026 22:19:28 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
