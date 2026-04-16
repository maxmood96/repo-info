## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:e6fe05b1484cd7e94cd5b75ec375249ad8dd59962f20353a6e52c01f0920bf9c
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2b7b811e1a7d801a8ea6a27a2b9e9a96d9a1322ca4a360bf3ee788c6af339f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.2 MB (284186831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa049fdc936853d8719ba8074eb9f331705fd486f43245d0fcc311fa44840297`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:03:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:03:06 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:03:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:03:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9034f4cf268e09db509ca456f99f930bf40a5d28f93d7a2ddb21d5c8507e6b`  
		Last Modified: Wed, 15 Apr 2026 22:03:48 GMT  
		Size: 145.8 MB (145806808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b32978c55bbed493b79980c7150ce0038a8cd9b1b4b659d353be68c625ba3c`  
		Last Modified: Wed, 15 Apr 2026 22:03:47 GMT  
		Size: 89.1 MB (89081544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ea5bad7144ff252157dfe560a7bc59b5c3bfe62285341c67a8271abf04d777`  
		Last Modified: Wed, 15 Apr 2026 22:03:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fd470c4d502307b9fd1b8298c40d73250c931379db6f92c81a668b55cbae8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd358db8efc9aa18b087a90f6d3652ed14aeb4346b19cdec6e651ff3d26a10d`

```dockerfile
```

-	Layers:
	-	`sha256:0b0d535c7e9572fb9533744a250bc05e437941b107220ebcb0f82d8583a4ab5e`  
		Last Modified: Wed, 15 Apr 2026 22:03:44 GMT  
		Size: 7.5 MB (7490808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1fc11862ea97e35f706c67dd072171ffcef6b9db0a0de12592b23047ead9c9`  
		Last Modified: Wed, 15 Apr 2026 22:03:43 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4c743dada66d89bedc3f0120bd6b29fbd29c622db116bfb2b634b0dc1578716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281420636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369b7b756118a865ac0d6d34fa130e1315db583f3f5b79950d1b411b188f0ee2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:14:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:14:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:14:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:14:22 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:14:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:14:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:14:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9556ac11abe14a7c8b10290415a8eb7c0237588034d542ad5c4f17fdf027e0`  
		Last Modified: Wed, 15 Apr 2026 22:15:08 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af618f9566eeb9427d93733e64f858542edf050c408e4282fe658ac748a59299`  
		Last Modified: Wed, 15 Apr 2026 22:15:07 GMT  
		Size: 89.3 MB (89253932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885b49cfc3ccf9530c394a275b0d43625e082686d8dc7772a61384e1da5b2af4`  
		Last Modified: Wed, 15 Apr 2026 22:15:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:137e7fdcddd10b69c74fbe057fa0be55a56a88cdb318aa20ac7f87d11509f68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e602c6767a2a1d22a6f8783840727e504e16c65b6f52fc5da2874b3824e8d52a`

```dockerfile
```

-	Layers:
	-	`sha256:24bdbeb12449e694d1dd18fc96c844b62428872e9db63c4641dc5bdd4a786b99`  
		Last Modified: Wed, 15 Apr 2026 22:15:03 GMT  
		Size: 7.5 MB (7498456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca79a1fdab9892625f7e40aee50a105a257fd83e917a256bfcb20cf5cf5d845`  
		Last Modified: Wed, 15 Apr 2026 22:15:01 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d4e16876aadc4f8bb5052202fdba1cb1db75cac676dddf89739c1cedf0459cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277104404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2e6930216f78e58311dda19c156223be99f787b74f4babd29c21c928a14576`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:31:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:31:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:31:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:31:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:31:25 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:36:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:36:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:36:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e47589c6fe4c4dc982ab170f9b8ead6b8f83c6423e7987728feb0248d380cd`  
		Last Modified: Tue, 07 Apr 2026 14:32:43 GMT  
		Size: 133.0 MB (132997689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d51cebcef6b6da44f8914ca5673eb49b9a1d7012fbb5eb3c224ad4bd870048`  
		Last Modified: Tue, 07 Apr 2026 14:36:43 GMT  
		Size: 91.0 MB (90987402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c869f16ed8445795212f733205542910412c457c17f72976f443e3d6891e689e`  
		Last Modified: Tue, 07 Apr 2026 14:36:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:64b14ba28a620eafeb96b5f8901ab135acc706480f40bda75e760e9195410e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf32d635f75abbe72eb0c19d985e32d3a948192b1b1b27e81971547015ee728d`

```dockerfile
```

-	Layers:
	-	`sha256:52464ff882a25e0a2338a3e1391e95d8716978f2205d0ba51c979a646616ef05`  
		Last Modified: Tue, 07 Apr 2026 14:36:41 GMT  
		Size: 7.5 MB (7494614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc1da2ad510b4445334087f19bc4a4c7129239edcb9d34d6e0c969b9e4c2f100`  
		Last Modified: Tue, 07 Apr 2026 14:36:40 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ddae7d176f592b08eaeb9ad835a6c16f85ac23a1988d5fbb0e2fc597bc594e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265638466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc7550057e198209847b2fdcfdcad239b97117a2cfaa3fff32640f8b0e59f2a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:37:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:37:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:37:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:37:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:37:08 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:37:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:37:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:37:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d204c9facd3f98b011522f39934cee41b1cb7f52f0aff655a7defce535ed5e4`  
		Last Modified: Thu, 16 Apr 2026 00:38:01 GMT  
		Size: 126.6 MB (126562151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5956a7419505fba569222dbf09bd58e57648ef94c7fb90471ebb473d2d32b946`  
		Last Modified: Thu, 16 Apr 2026 00:38:00 GMT  
		Size: 89.7 MB (89710565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091f6455c5d9bb154ca8c85ca4cbedacf2c889b9f4b519f44ba07c1476d3f57d`  
		Last Modified: Thu, 16 Apr 2026 00:37:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d5f3d0475c60b08afe86d82428632c458c416296b9aa4d4a931510c27b43a7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01945d2639b60e4f8f7b3c9bf8301f7c9791cc9635a928633d537a8a763ffcc`

```dockerfile
```

-	Layers:
	-	`sha256:ade9cc6096fdbc226e0bc0c6eb648d7293d120b8f21abfcd40a8f3b586bfbd6a`  
		Last Modified: Thu, 16 Apr 2026 00:37:58 GMT  
		Size: 7.5 MB (7486734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c810ca02e209fc630260135018480cdb2eb37fc35f6791dbb06f42c3f15e3b2`  
		Last Modified: Thu, 16 Apr 2026 00:37:58 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
