## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:a7fcd3cb399c40a2ca58091a37e79bf42e79a3887c74651dea4dbd71117a3e94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bd29953172f66cedaf9752749f5af2976c99558134ebd3c8cf71fdc4d3e2f957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152638587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3996846881522e62a232cd0ad35ba8b067d8ca72c9b315fe98d4f80b49e234`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0484c5763245840f0fa70de5138ce64370da24f33f06343a0929c200a51bb122`  
		Last Modified: Tue, 02 Sep 2025 00:17:18 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c14d7f3e21e4dd79611f8de374ce4a77b5ad9a6db6733268845d09d4ee749c`  
		Last Modified: Tue, 02 Sep 2025 00:17:19 GMT  
		Size: 69.7 MB (69676379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4d470a0c7346f0ec4f4726d56a49723285e6cbaa2253af4863d4fc55e2401b`  
		Last Modified: Tue, 02 Sep 2025 00:17:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1330dda5f3d5907473036667db176c2b68d0e498be02e5f0af14516f80a42f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f27be4ddef7669b8e20ec5acd7c5435cc0659192cb31f22927da476021ae8e9`

```dockerfile
```

-	Layers:
	-	`sha256:7ebdf1a59e4611f68257d9e10c4ef377c8908c3031d4d337b3cca8ddce52bb7a`  
		Last Modified: Tue, 02 Sep 2025 03:45:19 GMT  
		Size: 5.2 MB (5232883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf80911d4e43ebdeaa091233a54db56b93797ba91eae3044b829e57a4e8606e8`  
		Last Modified: Tue, 02 Sep 2025 03:45:20 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:29d37189e6480b422fe9b7d5552aea656a8bd2dd4736f0d95ab62f4936de6ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151468022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c89532af3f4d4d9b5869c7da283892640adaa0f5c7a18a475a8fdf634a0d13`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a3a86c825e220a176990d2df8f382acba2166acb0758d72c614d0a2721cab8`  
		Last Modified: Tue, 02 Sep 2025 07:34:10 GMT  
		Size: 53.8 MB (53835638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbba7612e484d9d8a0d2498020b5145ae62ec59c641710391c898f4bc365df99`  
		Last Modified: Tue, 02 Sep 2025 07:40:07 GMT  
		Size: 69.5 MB (69549736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04568c6abb526a4cefb922d115c3516e5762d24a477e2dc5adf6f61ef2fa552`  
		Last Modified: Tue, 02 Sep 2025 07:40:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fb7c05cb6a1a223800c5384191342f93c87696a986758f5e3197493df18220e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546d724758659360ce380965112b349d935975f49c2410f84d1dc0946fa4b3c`

```dockerfile
```

-	Layers:
	-	`sha256:845e4de56878c9c9bf2ebc64499d58fb180a4ffaac553f442ad15fffe162d9a0`  
		Last Modified: Tue, 02 Sep 2025 09:44:23 GMT  
		Size: 5.2 MB (5239342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330a1f03be9c41c5e7125a80ec44acbe5610d216ad27753612ac3735197c7ab7`  
		Last Modified: Tue, 02 Sep 2025 09:44:24 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d138bfc5b2a74eaf56f9181ab841713b07b20577efe4d3d9a288b97fbae0947d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159743420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bee5c8ddb352bf49598aceac2d3d09c398761ef755963da19863c9d9fdc03c0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970d5ed7e7cca3514b30899e1c6f9a7db1fea89aa6aaacfd6066cb2d0b3fa613`  
		Last Modified: Tue, 02 Sep 2025 07:52:08 GMT  
		Size: 52.2 MB (52165399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632796a6ee3a0bf26faaa49916e010f9979543cc4af1e8db59c098acbac6c228`  
		Last Modified: Tue, 02 Sep 2025 08:02:10 GMT  
		Size: 75.5 MB (75503957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41e77d968c04a18609cd2be4308a2f9e36faeda6caec494da945ea3d8bcf3a1`  
		Last Modified: Tue, 02 Sep 2025 08:01:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94cf53785b6c683cf8f9c5bafd796d2526973e72cfa58c7f5672bbf12583fca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9efd48e06efcc3cecc0d0ba90d3c71723d3be64a36ec9e0e0cfa849c7c5af`

```dockerfile
```

-	Layers:
	-	`sha256:b07292343f6ffe4d7a0c7d0dca47e0f3f5d89ac3d8379f7475b4d5f863457219`  
		Last Modified: Tue, 02 Sep 2025 09:44:28 GMT  
		Size: 5.2 MB (5238634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ebc2936db5dcd63dcf91c86c62c953a94adf9d25bd403d209a75e2a97f373f1`  
		Last Modified: Tue, 02 Sep 2025 09:44:29 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
