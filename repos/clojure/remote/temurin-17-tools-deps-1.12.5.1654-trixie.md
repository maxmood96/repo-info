## `clojure:temurin-17-tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:5bc6864438df2ed746f3fbb4a02a0539615503cc0bb798eedb43bb49f78a07a7
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

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a3b85b5193a63b46159b0f4e6c34d085bb72729ef39d2b95cbf0533632da7b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277742788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f366db4683f0e51ad844c7797098f4e27addd37f175f0a14193aaaa552c5052`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:18:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:18:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:18:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:18:34 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:18:34 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:18:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:18:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407dcaea88566292cf762e520483ec777f63f0e529273450f66725d96e4f080`  
		Last Modified: Wed, 24 Jun 2026 02:19:14 GMT  
		Size: 145.9 MB (145905407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3353b6c238105b437c31f814cb9e17fff5f647802cec8397d3e149431639caed`  
		Last Modified: Wed, 24 Jun 2026 02:19:13 GMT  
		Size: 82.5 MB (82519084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b04d7842d7ebbc09b3f32d99d973eb908c947aa35d1621bcd1c5b68a65ca140`  
		Last Modified: Wed, 24 Jun 2026 02:19:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a45b110e5f2924cb9955d91605b71e1fa8566ced02900b46a4570c72e8279b1`  
		Last Modified: Wed, 24 Jun 2026 02:19:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:22feb6f5ae7c150bfda9278dfe8dd656717d4bef2f13aa5d79c9a7116f88a777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28b477dfc5ed29a5f7158f865b81c60abc43ccdba0dbd12804ccc921d8be0cd`

```dockerfile
```

-	Layers:
	-	`sha256:fb3a714ceb98eb0d2e56710f80ed2cb98d8146ad28b0d8cb34dc73da2cb4c204`  
		Last Modified: Wed, 24 Jun 2026 02:19:10 GMT  
		Size: 7.5 MB (7468771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9444721323d03bbbeb560debf588953135fc185210bc9c4f4cf955e213cec503`  
		Last Modified: Wed, 24 Jun 2026 02:19:09 GMT  
		Size: 15.9 KB (15907 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb0bdaec95a602d9e59b7374defcc12a658d3f9b0fba532b1df6495eb8c96911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276742011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd125758d1d7ff3daf016de0c6d5e758a59342dcc60de7558bb88cc4f1de482`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:25:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:25:03 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:25:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:25:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:25:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187c8833ce05aa454f93fc0ace361d5fead4a6ac45fb2ab79bd63e5101b8427`  
		Last Modified: Wed, 24 Jun 2026 02:25:45 GMT  
		Size: 144.7 MB (144724351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715552457f4b143eee81c601f736d04e2f9a9db4cd4f4723791da8a32d6ca44d`  
		Last Modified: Wed, 24 Jun 2026 02:25:44 GMT  
		Size: 82.3 MB (82338221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e855cd2f744696718b252f61bc88dca25df5958853bcdaff71fd9c146bc52c`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43135fd5363e97a7f4a822edeeff7f8cb418ec41a946d51f8df3139f7b4efd40`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6e6df4238c6df780dfbcb611abe813dc1564b67b1ef9711cbe93877d398c8998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d9f62c17f0911d2511eae7d021482b43af75c92ca9aa11de01334e2599ad9`

```dockerfile
```

-	Layers:
	-	`sha256:91f6ca792cd8f93131a05e7b27f27c95d10481f945d721ba373889819557d4e3`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 7.5 MB (7475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faca259658f511abef8c70cdd9bd69d12f22362865c8b9390af282cb1d80aab8`  
		Last Modified: Wed, 24 Jun 2026 02:25:41 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:26baeeeb339bc69845650ba5d3610002dfde546903ada227514bed8a11b4a865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286843976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbf7413f55737cc77eddf9ef2a793e2a554566008ce4a769239eabb09257968`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:40:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:40:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:40:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:40:48 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:40:48 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:47:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4c522651359f2b9382194c5170132137b32f6d0214c41d2c39ba3ec770a8cb`  
		Last Modified: Fri, 19 Jun 2026 02:44:52 GMT  
		Size: 145.8 MB (145766191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551b2ca7bea8aa0d149a7d6228c220d1eb850ee641b23637f13e04830a40c77c`  
		Last Modified: Fri, 19 Jun 2026 02:48:40 GMT  
		Size: 87.9 MB (87938802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b3454e3eaff6273defe4e9a36538923faa7f811f684f93b558dc0889314606`  
		Last Modified: Fri, 19 Jun 2026 02:48:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6910d7560d0c4ae727068e2a104771515e2db7f19f7fc6cedea6c337ffb4d26a`  
		Last Modified: Fri, 19 Jun 2026 02:48:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6def1c7ea772ce8b8d9fea59c48307e95cc623a53a7a3fe00e6ffe8d5217f1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42e454e0b123f6e97584b1be586a62d62fe399332b43a1b7f702f58800750b2`

```dockerfile
```

-	Layers:
	-	`sha256:785f0214d5aa4f9d10b2d6ebfd93d47c33ec9af565bcf769f2d036d131af9d42`  
		Last Modified: Fri, 19 Jun 2026 02:48:38 GMT  
		Size: 7.5 MB (7473192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54ff817eecdcfcd4f7d518eb86a8e5fdc893266072bfad062a2dad6bd5372f08`  
		Last Modified: Fri, 19 Jun 2026 02:48:37 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:951b2f0d094ce462a3b714212a1c7eaae93fca152d3e89260b744f6a211307e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268799232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a780cefff3c6738a7f572ba1b854dec85c3ad026c3f034185dd0bbea9e80153`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:08 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:08 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918861cf680bf2b5b17504c84afdec10f9b09d3eb5a7a38387c5b5ff00597b16`  
		Last Modified: Fri, 19 Jun 2026 02:18:42 GMT  
		Size: 135.9 MB (135910421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05604fd093201395c35e0a394ebb9ffa94b07b9257b46627be968776477205b`  
		Last Modified: Fri, 19 Jun 2026 02:19:41 GMT  
		Size: 83.5 MB (83501876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249c0659418bbd4736ff737df8293b75fc22336f9507bb51e569117737922763`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a4181474c5ac99a9bd1948edfb4952a4f76073c22102f8cedd3d77cca6dad0`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e9d5e27d40d28f4ef56570ea433e392ffab25d919b6c3fa12b9d1d2d0182fb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e8d245d18e3cf3f0f1ca0f546053255784a12a2f6ce5d75cfa89d975a5d172`

```dockerfile
```

-	Layers:
	-	`sha256:562a8b19a3761ceaf411909f1c9224e7c382dda9ad7efb37807b75e5ede2cb8c`  
		Last Modified: Fri, 19 Jun 2026 02:19:40 GMT  
		Size: 7.5 MB (7464693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008fa772681810b0ff09b1b2dd4a5d6255eef2a8a173a110d04a93c21a1e3449`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
