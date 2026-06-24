## `clojure:temurin-17-tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:e8dd3e71542b198ddd26383c8d42527a602ddc7b7f6e71c3e32608538fca1562
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
$ docker pull clojure@sha256:718d3c152b2f31692a4af4f85a592d00f77de71ddc1733cbf070dfa189f3b469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286843288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c5181e9c98fc8a00debaf099f95f6e1185a10d0cc81bd7e65496ac460d3bb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:04:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:04:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:04:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:04:56 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:10:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:10:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:10:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:10:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:10:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a53855c06118fa5b5b33f6c132118109dfa1caf9e1afd948759aa32dd0c2b`  
		Last Modified: Wed, 24 Jun 2026 08:08:20 GMT  
		Size: 145.8 MB (145766157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb98c866146722cf46c926ddfc3dac4f3963fc03406505094f75035af9bb01f0`  
		Last Modified: Wed, 24 Jun 2026 08:11:28 GMT  
		Size: 87.9 MB (87938021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700561016e6474393d512c1527619ad76e346765bc1424357d1a0097e53ca6af`  
		Last Modified: Wed, 24 Jun 2026 08:11:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09551f12b53de28aaa308f55a367388c05b37f669043b9ff6d9a79f2d04862f6`  
		Last Modified: Wed, 24 Jun 2026 08:11:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f4972bca689e5abb8ed4d9c2a6050bc158543d80670a2d84f48508aa8b53f952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4cc09cd94df1ab4fb6d018c988f7e80b8546c297e46a901075a0f568bb1cb7`

```dockerfile
```

-	Layers:
	-	`sha256:7b309501d9d763cda0e12d95105744a58fbccc6922a2252d54c1eb38e4188247`  
		Last Modified: Wed, 24 Jun 2026 08:11:26 GMT  
		Size: 7.5 MB (7473192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddaf0defb977bf32938e43f46b13b869ae8848a561e632a572957bbb1a38014c`  
		Last Modified: Wed, 24 Jun 2026 08:11:25 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8ab373572f63194ea1d505c83e6dac697853242d08845e83b7e248ab1b45a96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268799256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3676e81c4f1d2da189b5b361c4ec39a4dded472184c2ae527428f2451312ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:11:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:11:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:11:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:11:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:11:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:14:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:14:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:14:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:14:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:14:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f578fd1d3edc228a6dfcbdc9d47149a7226cc5f1ca354d1a0d7b0fcbb5c79263`  
		Last Modified: Wed, 24 Jun 2026 04:13:26 GMT  
		Size: 135.9 MB (135910382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dca9b84d51d0f279963f23b9aca3e78a36bc337c4057e3d7c47d92deb24430`  
		Last Modified: Wed, 24 Jun 2026 04:14:27 GMT  
		Size: 83.5 MB (83501777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ee59a36c76c305f157927987b5dbf0d86fb81777abb17d1fb4dac6288f5f28`  
		Last Modified: Wed, 24 Jun 2026 04:14:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2071cb47f0270f962660d43f93ce3d63b02b28e7e6e5ae59e29b03e0bf1fd82c`  
		Last Modified: Wed, 24 Jun 2026 04:14:26 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4807df20d2bd1b6c3984102c86e5abfb7869207e6cb928f77a16aecec24d9b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07951410041f3d03e60a80118654122c113bc364f68024ef11961bc2afb67a6`

```dockerfile
```

-	Layers:
	-	`sha256:47c4ba563b88d0462c59fccb23c6fc1fd355b9dcc68d3976374a836ebbadb6f2`  
		Last Modified: Wed, 24 Jun 2026 04:14:26 GMT  
		Size: 7.5 MB (7464693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0668628dd26f22e17edbe59408b52191ddae4eaa9a3f5c8f02983857b8c7e3e3`  
		Last Modified: Wed, 24 Jun 2026 04:14:26 GMT  
		Size: 15.0 KB (14953 bytes)  
		MIME: application/vnd.in-toto+json
