## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:01ed233f590c7e300baa6d8bd68a40753e2a7e84cc5892f4f0c45ddcdc5c5b48
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4661885a57f95d4fd85236e2ad8ae245c563312bc5973783d508fc23f2fbb35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259652093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15e3de804ac473c45e5d82da7335a0a2ffd85597a580e4c0070cc13bcb07cd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:02 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:20 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5fbd7bd90132e24b774d4928199b50fb3e4b5d205651bc0aa12cd2d9f1f2b1`  
		Last Modified: Mon, 09 Mar 2026 20:36:44 GMT  
		Size: 157.9 MB (157857123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e195e8383d5c1f3e1763a49de30010b3a0ce88a051add0e6fbbdf734294ec2c`  
		Last Modified: Mon, 09 Mar 2026 20:36:42 GMT  
		Size: 72.0 MB (72015294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e5cfd81031db4876892628e99b116d7ff5677e0d36d7fae596e879fe64fafc`  
		Last Modified: Mon, 09 Mar 2026 20:36:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d92648c3f01682cd31d9f6db0907398d777ecbd6169a82186a6c1df9bbeec9`  
		Last Modified: Mon, 09 Mar 2026 20:36:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d2e8aff2b7398f119aaf015b98c981039e00b3b11104340f518ba923a1b3bebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9bbe58b5d9db8556c14071e5f3b5e9065ca66c58fcf9e3386cd32291312fd6`

```dockerfile
```

-	Layers:
	-	`sha256:a336607bda54cf1d023831d42d61cc34726ee12c7281472ece6e6738528eaa96`  
		Last Modified: Mon, 09 Mar 2026 20:36:39 GMT  
		Size: 5.3 MB (5260916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7a310cef63c8f94ba99940f669311ca8f0200da8170c6681eb143bdcc7a8fe`  
		Last Modified: Mon, 09 Mar 2026 20:36:38 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:062a3a5cc295808e2690aac46a0692083e73985aacc34c9cd62a7801b8d1d042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258106051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869849e147a256a62c115600f91914e0dd4fcb701fb69fe818f0f3386dc01211`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:35:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:56 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:15 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8334a5d5cfda220ab018796f5026779259df72b7b4244dd7a4e3d923c477f2a4`  
		Last Modified: Mon, 09 Mar 2026 20:36:39 GMT  
		Size: 156.1 MB (156133016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde58a3977c74d7f4a3482d3f6e9bf01edd7b6ef0c87815d5fdddeb62922e6c4`  
		Last Modified: Mon, 09 Mar 2026 20:36:37 GMT  
		Size: 71.8 MB (71831893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07636f3193474e4516859eaf1b50f7323248a562db3eb6fe0ff62857e905f0e`  
		Last Modified: Mon, 09 Mar 2026 20:36:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1639e61f7aadbbbb7e0abd89986285fd4ce6ea9e8259e57bb032f6a66659839`  
		Last Modified: Mon, 09 Mar 2026 20:36:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e54bfea7cb9b5f7db1b31de92658090e98a246215c34f37c5c14b5adedd60387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2886e68ba975eae91b6a32b9bb0419bdf91588695b016889259f21153199a78`

```dockerfile
```

-	Layers:
	-	`sha256:bfbc4c2c43d9c2641d84c1c55869559bbdbc66d1f3f6732fd6e7c2342ae0f6ac`  
		Last Modified: Mon, 09 Mar 2026 20:36:35 GMT  
		Size: 5.3 MB (5266685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b90c2a35f481226e98c8cead9322c2ecd2bffeb1e77b21bab2ccc26a4a305`  
		Last Modified: Mon, 09 Mar 2026 20:36:34 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:51e98b00536a0e578cafdca75e5a611aad49aac7311e88008495def9265e713b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269007041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196689b3daae3e383dd083f00839301d47b3c4c74de1866abcf9f8016181b0a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 21:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 21:03:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 21:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 21:03:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 21:03:49 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:04:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:04:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7028262671fb5dadcebcc8bf5d066709ff6037f20f3a6dacd4f71d5d28a35f6`  
		Last Modified: Mon, 09 Mar 2026 21:05:55 GMT  
		Size: 158.0 MB (157977490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f2869619fc921515d3fdded2b0fdef33f2b9ba6e15ef780fa4055d41e1b4da`  
		Last Modified: Mon, 09 Mar 2026 21:05:53 GMT  
		Size: 77.4 MB (77428288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f14f74ecff4abbd8712386c02b2696ddaf3a8426ae33dfa1d8cdefeb414840`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f44972a83cef7a1cdbbb34dfbb324fd4b1de5da68e40af7c82bb690f7be19`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f7001a3b75e77c360a7451f28d1554bfbd043b3de9a35525c3052064929dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3086f5da652f33a05ff0b32aae72f6587f8462787f83a2104fb8c5da050ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ff39406a782378ddba1eacca741e01553fb9d97813106e76ad0fc8320d7cb778`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 5.3 MB (5265287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42daa6b54a256337818e1c54c7d7fa9f42d5e4d666cc8904de441d6f54f1417e`  
		Last Modified: Mon, 09 Mar 2026 21:05:50 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:7868966579d592cbec34f180a5eaf076fcf906b55fd0fcc8d174c9bf52611b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256393722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f5b09b81f1851d3ecef57a2a968cdff1e226ceb3d06edea57b3d6c3085d9fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:23:46 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 11:23:47 GMT
WORKDIR /tmp
# Thu, 05 Mar 2026 06:45:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Mar 2026 06:45:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Mar 2026 06:45:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Mar 2026 06:45:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Mar 2026 06:45:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6f2d4c20cb87ce38553ebd9ee153c1d2ba4124eefd89d1277f7fcbaccfbfa3`  
		Last Modified: Wed, 04 Mar 2026 11:31:31 GMT  
		Size: 157.2 MB (157216904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39a9910e65691f48125ccc354aee0a2ae5231eb0751141a2d5e6d4229a50c8f`  
		Last Modified: Thu, 05 Mar 2026 06:48:54 GMT  
		Size: 70.9 MB (70899356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb72f8ef552f54020ae854a8405f8256fb0e4f4afa3549e31b1daa92a3f7f8c`  
		Last Modified: Thu, 05 Mar 2026 06:48:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5f23e7e4465bbdd3f25b13f66f8f0b9548d4b12781e4ba684fd938aede4f5`  
		Last Modified: Thu, 05 Mar 2026 06:48:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82fbca0d980e280295002874bd0cfa8d378f3928d02827bfc8887f8284de4ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a11dcf30d6a927db4074e52cf4f78f48cba224a729a01fd70e836eaac32a634`

```dockerfile
```

-	Layers:
	-	`sha256:2f595b1e56b76d10c3e94cfe8b241580f5d827bb4dadf3851596289bbd186023`  
		Last Modified: Thu, 05 Mar 2026 06:48:44 GMT  
		Size: 5.3 MB (5250380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f329442fe6229c0e14e767720eba599471856c132d3099d98894bbf1bd602bea`  
		Last Modified: Thu, 05 Mar 2026 06:48:42 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a214e162d422c98f86ac65ae5579c3b705e08af21729949a76e8ec5a14b3a17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249928231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4ec2f1a7661f4d0ee9591011abc068a82c31f4adad98cd2e60f4cafa8f5c12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:43 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1739455c8adaa1831c28f6e8345aa92a5327b6efcacea5168e2647078f0e63`  
		Last Modified: Mon, 09 Mar 2026 20:37:32 GMT  
		Size: 147.1 MB (147105306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b0847a2070dd3a416be85d53c4de86228b82a1cdd7c43642a3daf5e9e2c0dd`  
		Last Modified: Mon, 09 Mar 2026 20:37:30 GMT  
		Size: 73.0 MB (72983703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2476888f386cb12ad521ba25efd3bcef44a9a2ae826e12082715d64b3da4be`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868dbbc915c30e4b0e0e9469d545270c3f61ecad90436101cc4507dae8cbd135`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d14bb29593b312550beab0af9d4fa696ce907223c5b6db3589649c05122d6b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5b1303955a5d8848c395637bd24fb55c67e9e933bf5cdf798805e9085869b5`

```dockerfile
```

-	Layers:
	-	`sha256:1c287f4a98407ae083ed6cee2d7ebc2317fd4d2c2b977ce65bd81cd335b69495`  
		Last Modified: Mon, 09 Mar 2026 20:37:27 GMT  
		Size: 5.3 MB (5256840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c90d86da52254d720abb921a661f635bc0e381a5f9d27cd62d09ebdedbee54c`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
