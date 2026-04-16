## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:cb0fb826cd06c5eda8cf1ad63bdad531dd5bbc7b587fd3730a7955aed74067ff
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

### `clojure:temurin-11-trixie` - unknown; unknown

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

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7fadf012360a262c9ccd80729a1ace5aba00bcaa6f276e796e9f1ee854c888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277548908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a0914a4f54bbbb21e6c20183030f5fb5156c393259e3707187ee8af5560019`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:25:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb89399051b92d45beb86afca05500e7b3427471d1e6499c23f8bf1d0042b3ac`  
		Last Modified: Tue, 07 Apr 2026 03:25:40 GMT  
		Size: 142.5 MB (142500029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16bc5fa3e7deb66b54217f931f4ce11e0b8f0b306b7456a14ca1139d619d79`  
		Last Modified: Tue, 07 Apr 2026 03:25:39 GMT  
		Size: 85.4 MB (85382977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73af49cf236e722ad5053c31406ae443a5492bbe2379ffadfc553f29ec1c5006`  
		Last Modified: Tue, 07 Apr 2026 03:25:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a0c44b727c6bc5aac5c7325851ec8690745a65de47f0e5c763fc4e6172eb2f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c21306397c1f4c4e18bb09d8d80dc7abc3200e555aa65b8950661209a993bd7`

```dockerfile
```

-	Layers:
	-	`sha256:f74560a3c61c1d9f74a36da449738598f14cc0d579defc9b43f722bebc36d0e6`  
		Last Modified: Tue, 07 Apr 2026 03:25:36 GMT  
		Size: 7.5 MB (7498456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:864c39ff7a6be04a6601b3f9565c260d6c87288e17b59fcf2efeff91a961b36f`  
		Last Modified: Tue, 07 Apr 2026 03:25:36 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

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

### `clojure:temurin-11-trixie` - unknown; unknown

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

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b90c4dfb5bd6f2860b1e255058cfff8ed38395a9ab4fae21b398f68debdd0f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262471881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8e0c5c44f389ccccd27dfd768e71e8ce19e1debece5d0b2e915c949e5d2b78`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:39:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:39:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:39:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:39:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:39:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:41:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:41:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:41:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0f6af54b41978b4b00c1cf75bd9972713058d469f37803b6fe31ba2949998`  
		Last Modified: Tue, 07 Apr 2026 05:40:42 GMT  
		Size: 126.6 MB (126562219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db28f8d40c7226ca446d17147551bf99e50f6e9b4241c3998ea991229c9abe`  
		Last Modified: Tue, 07 Apr 2026 05:41:46 GMT  
		Size: 86.5 MB (86543912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff24c24f3fa61f7817f087583f6d8d42dbfa29a10a443a3b504505efcd9f36c`  
		Last Modified: Tue, 07 Apr 2026 05:41:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9d253ff11cee3ada43deb75293bc1df6cdbfa1c017c67103ed1bacd503b90012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a29fcb64d82a8f35872937ec8c5b1ea15335aeb9fa96d6a7b27d3d763664ae`

```dockerfile
```

-	Layers:
	-	`sha256:50982e8c3e6a06e588c9db4d40e5c2c6db856f566907c3c8398c61a3020f0e7d`  
		Last Modified: Tue, 07 Apr 2026 05:41:44 GMT  
		Size: 7.5 MB (7486734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac5c63678365d86f8027b4e1ce3356a1182d8a6ffc2c442f94a07dbebfc2833c`  
		Last Modified: Tue, 07 Apr 2026 05:41:44 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
