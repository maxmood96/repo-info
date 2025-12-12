## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2c9e1a4a8527df6c362b4af91336597fe460bda64f9bbbf1ca650d0f55b32d69
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:68d640c6f136a6880ad6765577ac324fbf790b47ad7ad83aefe6d0bff37340ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242755082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd35a76b8469de60acf47b175f187bec6d40e623b190c16157abeffc69e5c01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:39:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:21 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:21 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a6a2684a188223a01ceded9f89dbb1697cac4cfe3b79df5d3e7fe090967c6e`  
		Last Modified: Thu, 11 Dec 2025 22:40:00 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c606464495c0c8875202bdc3f47dae78d0ea0a4601ceaeb7edf45b7897539b`  
		Last Modified: Thu, 11 Dec 2025 22:40:10 GMT  
		Size: 69.7 MB (69677703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753a1bc60b9644d1947d748ffc52461aa26438cfde4938560d70b510394c7b0d`  
		Last Modified: Thu, 11 Dec 2025 22:40:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce0efca9cd07939e867be5af54a33d4e4f669a259cdd8ce1b116b12f570cadf`  
		Last Modified: Thu, 11 Dec 2025 22:40:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d470102dc2b4f2152a1e57ec2997f466ecfe3fd68975c536d9c2688a89081a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2fa7c56ea31395544f4e7dce21050b04ba04f1537a0776b3be685316961b2f8`

```dockerfile
```

-	Layers:
	-	`sha256:c05bb0e3582840c68fd1bb053c760648c9f7dd9b5acf850cd1b38a91fdb4b710`  
		Last Modified: Fri, 12 Dec 2025 01:37:56 GMT  
		Size: 5.1 MB (5113390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c3645a7d464fc6ac9f9385ce724b9faa90f197d484d890859b88704846f1012`  
		Last Modified: Fri, 12 Dec 2025 01:37:57 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e686e42adcfc5e813be6c825647b774673cf4ed5228bae0f57b43fa2ab801eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241341614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13902a79ee8a5a58a4f447d8ffa940599bc978ae6a50dfc32784c278cba9daf1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:39:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:13 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136b0ca6be80c6ee28769db2ee15dd28adab23e15693101158aeb8db3bc07d18`  
		Last Modified: Thu, 11 Dec 2025 22:39:50 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549da42bd6392132aa32717b2b677737091d6b603bf26ecf3f65d94f48cf8185`  
		Last Modified: Thu, 11 Dec 2025 22:40:00 GMT  
		Size: 69.6 MB (69558429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30712c0c9e57510fccebdd310ca19de498330c994afab7eba5b3ff0fb6afd627`  
		Last Modified: Thu, 11 Dec 2025 22:39:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a407922dcdfcc4145fe926f67fa7a6d24a025296da3d74429aab0ed19ebd3ccc`  
		Last Modified: Thu, 11 Dec 2025 22:39:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fe17c724b2d7c46048440569042fe9d7d4a858a680bdcf2f3f4a63f276798229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769bbea3028e5eaebcd2e28e050765bf88a07f6d7c4386ac77cf9202376ddc40`

```dockerfile
```

-	Layers:
	-	`sha256:dbe135e8c44cee254d110e361f179ff47ba4af539dce2f9bfb1f237c0fdb00e9`  
		Last Modified: Fri, 12 Dec 2025 01:38:03 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548433a28b8c97b53f8bb694ab81a90df359bd0f9311de6e5977afb74a13fbdd`  
		Last Modified: Fri, 12 Dec 2025 01:38:03 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:95038829958f224358e0ebf434afd509a96f747af0124e6fa633f84b36edd532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252104992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0428a813f0f2854c2950b45c83feab5202c9158059eb0e8b277e3c744b33143`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:19:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:19:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:19:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:19:41 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:19:42 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:55:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:55:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:55:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:55:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:55:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca5d6201ce1f6df8beca96bd758c86429f17de7a899d824f11ee65b7c98225a`  
		Last Modified: Tue, 09 Dec 2025 16:23:43 GMT  
		Size: 144.5 MB (144525256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a30c26a4da49534ed38acfda95596594ff19691b8c9c0ea7137ac85befb7612`  
		Last Modified: Thu, 11 Dec 2025 22:56:15 GMT  
		Size: 75.5 MB (75509849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8bce2491ed28bfd0f97151c129d1859e1dc219cea2c12b01b7ae36246570b5`  
		Last Modified: Thu, 11 Dec 2025 22:56:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6f88f24b16e85ef0285d40cb1850f0c1cca2fc31478589f40ce1a68b2de3b`  
		Last Modified: Thu, 11 Dec 2025 22:56:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99c8218e678e7d9a5cf2b02e42cfdebf603443b27efd92674633b821c6b8b3b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f5a22a058d79e7dc1ff51dcb450ce99f864fdc9d2f2222c173c5a0b1e54db4`

```dockerfile
```

-	Layers:
	-	`sha256:0b4ea8fcc457073a47ad5d4d50d0b841dc8215177a24e2b586d2516a41c19d45`  
		Last Modified: Fri, 12 Dec 2025 01:38:09 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3d09c7aedb5ce6091a1baa3dc994740d71b8639c771cacc09d9397d562241f`  
		Last Modified: Fri, 12 Dec 2025 01:38:09 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4e90fcf739fa41451d914bb5a1eee1fed43308e04c8fcd6ceef8771ca4b17eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230232217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add2f1d3c2dd3dab07ffb4b5eecc6a80f4e3655a0dc6cfc38f57bc433d74a52c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:34:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:34:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:34:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:34:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:34:15 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:34:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:34:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:34:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:34:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:34:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd96691148dd6012cccd8bf9acc816d822e7526c38a602302f11cbc55573cb1`  
		Last Modified: Thu, 11 Dec 2025 22:35:12 GMT  
		Size: 134.9 MB (134859068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b511a1336d7cdf977834aecf8010528ec617bc4e68cd29a6e76a60179bfc4cb`  
		Last Modified: Thu, 11 Dec 2025 22:35:07 GMT  
		Size: 68.5 MB (68487679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6747de6a162a6243a73da4358bf3c0dca03926591f331bb9640baf0e855b5`  
		Last Modified: Thu, 11 Dec 2025 22:35:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79872b4ab55b6457d0c69f16b431f2bf04711906d27f66d190fc6686e91f5f2`  
		Last Modified: Thu, 11 Dec 2025 22:35:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82f84abc3917f70883401db88cd75f306dfff3e74f2413762ccf9fc9bd1c9772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22ae511cbfc5d558a32ed1cf3a9879edc43a8245e60197d3467b9b6431dcf3a`

```dockerfile
```

-	Layers:
	-	`sha256:6fd938e902b74ba3c382a24be203cdf0502efa7437b314e7019b63dfdd393860`  
		Last Modified: Fri, 12 Dec 2025 01:38:14 GMT  
		Size: 5.1 MB (5104711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8418a895a6138dd3812624ce4eccb324915206e1ab43f3dcb056d5a5a02f881d`  
		Last Modified: Fri, 12 Dec 2025 01:38:15 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json
