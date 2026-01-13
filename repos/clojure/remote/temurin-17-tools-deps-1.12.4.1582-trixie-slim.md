## `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim`

```console
$ docker pull clojure@sha256:85b7dfd8a46682ff642c3b8ba49fb2deec4631f17ca6dc4faacbb2b5940832bf
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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e1255d026f5e2b2963a03b24b2cd6906a3c4dcb1e010db9d81de5a2f8055362c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246615842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d44529ac9791ebf18f23b2e558dc1d4c5fc2f26240cb13702d3dc803b664f7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:33:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:33:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:33:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:33:12 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:33:12 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:33:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:33:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:33:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:33:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:33:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe92b2e66ff44b083f3403af78ac02cffbc71d2168404b31aeeb92c3fdff0fc9`  
		Last Modified: Tue, 13 Jan 2026 10:40:26 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c05d3c9a0de7a419adf3e7dce064d5e9eda8487871e8b805cdcaf3b8b539fe1`  
		Last Modified: Tue, 13 Jan 2026 03:34:01 GMT  
		Size: 72.0 MB (71993165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d4fbf05ff50bb0b0dd515bae0edba66866e6cf8522746f8efa87b0efc96d1b`  
		Last Modified: Tue, 13 Jan 2026 03:33:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676941e5b80dd3bdf103e65319e5c3afa518c9ebb5489134b24dc1e4a3a989d1`  
		Last Modified: Tue, 13 Jan 2026 03:33:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6ec892c3ae2defaa19ab816fb5d0b9a8f46302909f52dc15ef3374cef9c0c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939a3aeef7f7116d8f1a016682c0c883b09480b7051553963b6f29f92ac870e1`

```dockerfile
```

-	Layers:
	-	`sha256:127ee93c06d953281b91ba2bea59912f860178d8cf381d94dc6179f1af35b5b4`  
		Last Modified: Tue, 13 Jan 2026 07:41:41 GMT  
		Size: 5.3 MB (5256297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fcc9f3fdf2f93784df70a2fe1cfd5e4571f847988344f1575880171709b15b`  
		Last Modified: Tue, 13 Jan 2026 07:41:42 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a5a8e1ad4d78cb7244c794f988cc40809410d141420427ea4ca6c5d51d6c72f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245621189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf894605d78b12e1257ea4aba27cdb36acac779d1d60b89a357d2d76b28451f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:36:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:36:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:36:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:36:37 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:36:37 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:36:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:36:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:36:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:36:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:36:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93c84859b464083927e8af266a5137f87c28ebdc2a55f49ca422ab31f9a227a`  
		Last Modified: Tue, 13 Jan 2026 21:13:46 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624246f60bdcb33044ff55e11980cdb2dcfd1383adbdddd7656bc8788eab3b3f`  
		Last Modified: Tue, 13 Jan 2026 03:37:29 GMT  
		Size: 71.8 MB (71806188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6111fc63e5f220ca7a7e826059a456eebc486d415ea539af9a7f430884af55c`  
		Last Modified: Tue, 13 Jan 2026 03:37:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db115b692ecfc772c35b615a8363bf1bbffd6316ce51beecb6367cf6e4abdd70`  
		Last Modified: Tue, 13 Jan 2026 03:37:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8412f62171bf3e9d183b8e8d40dd47366c193e36aa09714a7a2818af87591fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce37dbd44f627820dba6ad4546c8eb61bb187c194cc0cc2a27d1d4ab3b3f403`

```dockerfile
```

-	Layers:
	-	`sha256:20384b236c72a8d561bfd353764e3d9ef2fb50c84f2fe502f1928050189fd4f6`  
		Last Modified: Tue, 13 Jan 2026 07:41:47 GMT  
		Size: 5.3 MB (5262066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57194ddaaedd8e131959909d182df434b6883b4f6d30ac730eff79303af45afe`  
		Last Modified: Tue, 13 Jan 2026 07:41:48 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fae7b9816e6679e89e035a88a4ec454cfebd57eaaa7ba07288f196e006c771c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255511284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d7b316951b21b72cda2e0c230028b63a19ad0eb93fd752491db1ef87444419`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:42:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:42:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:42:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:42:48 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:42:49 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:46:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:46:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:46:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:46:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:46:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27844d738e02788c6b697812732ba5feb3fc1d5093e037428695dcbe90d378f0`  
		Last Modified: Tue, 13 Jan 2026 05:50:04 GMT  
		Size: 144.5 MB (144525242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f6a5a9ac1a1f9491dc3acd0ca27ca500253777664aac801f08c0cbec111fe7`  
		Last Modified: Tue, 13 Jan 2026 05:47:11 GMT  
		Size: 77.4 MB (77389399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b343fe0486072037c94a888d57407399dd26756b50410308062f0d532b21bd0`  
		Last Modified: Tue, 13 Jan 2026 05:47:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ed003a7987c66f5c071220c4f93da087434483ffac1721fbae29c5a60dee3`  
		Last Modified: Tue, 13 Jan 2026 05:47:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88c3c61c52524ee4f6b08f78bf5847f2632ac850526455cb799dbf28bfcc357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d7a631f5386e537f19080af52a693201dd493e0881a3215dc1aa54b6206a32`

```dockerfile
```

-	Layers:
	-	`sha256:1b13c73da6178a44d5e320daa52d617e4ac1a1937540fd74fbff98ac621ffd41`  
		Last Modified: Tue, 13 Jan 2026 07:41:53 GMT  
		Size: 5.3 MB (5260668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12287d0209b8d8f025c2e9d30d25cc12f52cc62586d716158a998de491491d9`  
		Last Modified: Tue, 13 Jan 2026 07:41:54 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e6bad6d9852e3d6f80f8fffc573c53280c53705184f50c921d552a9927ea615c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241041662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399ed849df7879a3e7eb4bbaf5c152df3283cffd3f7f2c2e3d38ae87fc296a68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:35:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:35:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:35:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:35:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 06:35:03 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:51:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 06:51:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 06:51:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:51:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:51:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c47e4b223479384cb91259f631c9c203246ef873e850a7fe5e6ff70d31329ee`  
		Last Modified: Thu, 01 Jan 2026 06:41:38 GMT  
		Size: 141.9 MB (141889571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cc585b93e3e20213957c5dd5b3c125d9945ffc7e093bb3d9c1d7310d9f83ea`  
		Last Modified: Thu, 01 Jan 2026 06:55:28 GMT  
		Size: 70.9 MB (70877919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0318aab2d926170901cae285fb051c89b7e991b70613cd4d507d97ab1e6988f`  
		Last Modified: Thu, 01 Jan 2026 06:55:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc085b40e88e8dea55a124943f2d673a3dd08531d24d2acca86b2c4f8e8ff4f7`  
		Last Modified: Thu, 01 Jan 2026 06:55:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d3dea53c41a2b97ea1523520a593c030046b6afdf7c6539e1fa5dc290c0c96a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102b8347d7500724ff5d38fa530575b12081d3e4e194c77c8216ec85e83d6954`

```dockerfile
```

-	Layers:
	-	`sha256:be273a0a4b1417e10c88eb9076044a523213af56f46dee41ccf576f30260b74b`  
		Last Modified: Thu, 01 Jan 2026 07:36:00 GMT  
		Size: 5.2 MB (5243744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa697c888d64aa30032972e268c86352ca7806002c6ffb539f54d29d0641a35`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:24d7a698e43add73aa35f195c4011a6beb2eaf0209cb657b4dc50f88ce7ebe3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237645799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabd2ff97370f0be73eaa3862c1f3e816d692ca3af0e4863bd19764c883bf0fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:37:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 15:37:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 15:37:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 15:37:40 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 15:37:40 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 15:37:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 15:37:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 15:37:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 15:37:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 15:37:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77d760f143dc76fbfa81eb118de9aeafd738da1a2bab7e0b4cb478c63e75113`  
		Last Modified: Tue, 13 Jan 2026 15:38:24 GMT  
		Size: 134.9 MB (134859044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbba572007e41012e36f75211e152ff1523985befa29c79d6ff0c0fdea4a9e8`  
		Last Modified: Tue, 13 Jan 2026 15:38:43 GMT  
		Size: 73.0 MB (72952301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ae599ee72470bbeb3714866ad296247836a08c75109013118b109d1259cc3a`  
		Last Modified: Tue, 13 Jan 2026 15:38:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d17ace574c90b83d19f89ba4b5aa05c116e1ceb46ed380373754f840ed865a9`  
		Last Modified: Tue, 13 Jan 2026 15:38:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b229ae6c73f75570552bf9762c037978eb1c43d5be02c676ca361b7429bdf3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be187ad6555e8d3565969ea831317680799a519948bf429bca43d38eb48dce0`

```dockerfile
```

-	Layers:
	-	`sha256:3a9cbe1a232d3ef037026ba1ff909be05d71842636e2b13304ff26c1b602cdd5`  
		Last Modified: Tue, 13 Jan 2026 16:36:29 GMT  
		Size: 5.3 MB (5252221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af86309a08b203adf606197fb61385a1595e747234bceba5cca0eaf8ee5c267b`  
		Last Modified: Tue, 13 Jan 2026 16:36:30 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
