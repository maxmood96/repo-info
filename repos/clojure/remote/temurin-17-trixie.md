## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:0771945e84c4a9f708ffeba17921029330b726939ff021869e5c2904604b3901
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6cd712e0fb4d9c497a48af3b73ea0ae1a076af94ebeb491938b3edd7dc52d525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280502272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243a56a33f904584fe4706c5a07609afea81c74803a40011c69bcaca00e7fbf5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:18:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfb82a121e55ef27174faaa10661fa75f8472bacd345eff169ddcf69805a591`  
		Last Modified: Wed, 22 Apr 2026 02:19:37 GMT  
		Size: 145.6 MB (145628762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2446ada2bdbd53c642105f85968a45a481f5d636212bfa2cce284986d37502`  
		Last Modified: Wed, 22 Apr 2026 02:19:36 GMT  
		Size: 85.6 MB (85570374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be99b20d7e5e5b0defefc93446c3dce43abc34355aa961c68d10ec4e3b97bb6`  
		Last Modified: Wed, 22 Apr 2026 02:19:32 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df7ce54e923879ce9c70b25f9075a7ad8034b4e2a975995040f55754c825b4e`  
		Last Modified: Wed, 22 Apr 2026 02:19:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:06c78dacbcb15f831de1a5a028990a20af8f60bc121da6b221a2d5712a1273a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6872aec61bfa4520e36cf50634b350ddaa7e3315bb8292f6e42ea32d490e1dfe`

```dockerfile
```

-	Layers:
	-	`sha256:89d7ba3f4a44f10ea53eea291c29c50a271d6c0eee90137e6db9f94f3b0584b8`  
		Last Modified: Wed, 22 Apr 2026 02:19:33 GMT  
		Size: 7.5 MB (7470721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f2a3210000b0ddbc24ae15e0e72ad805b284e3ed0187b8414c56521151524a`  
		Last Modified: Wed, 22 Apr 2026 02:19:32 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:276d3e263d939f4f8e6c9f19033de6210e1d677e121eb2030c9567d8183cad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279489811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4152e87e3caa75cc308934b62cca9938fb92589ab4e3bf73eb9be0d2bee8cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:00 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa828840c6c86198601f5ded34fb7ed44a633615aaa9c1d5dfd5de8075fe9f6d`  
		Last Modified: Wed, 22 Apr 2026 02:22:41 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6f23164d45fab24de93c5afe14357a8310aa9933d604a5d315ebb413cee17`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 85.4 MB (85383340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5deb0cf6ad5b02557d68efa651dc78dc5558726f1d4ccb02cb5ca5e8f70beb`  
		Last Modified: Wed, 22 Apr 2026 02:22:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ee7626be781452d466f92fb742d01b413f46387bc88f5129c3bf2288ae50b1`  
		Last Modified: Wed, 22 Apr 2026 02:22:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7b9230dc88f324df1bc53aa6409333c500c175d0c107ae4e58f6cc14a9415a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc22c30a8d7f7fa6b13704580c815b878f46a64019a216c860df12d761eab3f5`

```dockerfile
```

-	Layers:
	-	`sha256:1680d38bf385a8e59ff84dcdee657d04e3af2fad816c964058d9babba8b8b8c4`  
		Last Modified: Wed, 22 Apr 2026 02:22:37 GMT  
		Size: 7.5 MB (7477751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297d2eb5ba2fc0782219ec3ca0eaa558e1584686af40dd9a31c32cba53e4d0d0`  
		Last Modified: Wed, 22 Apr 2026 02:22:36 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8600eb024a7fd18277dc6321d62ce70ffc5a49edec3a9b65c743aad2d16e97fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289548716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049a3d886d520acacae7221813c6415e478cca632092997a2064f4f129afa309`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:30:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:30:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:30:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:30:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:30:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:35:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:35:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:35:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:35:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:35:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8050bc2d6ceb1ba93f1bc7881f5152d6617c5ae147bbcf177968cb01c684519`  
		Last Modified: Wed, 22 Apr 2026 08:32:22 GMT  
		Size: 145.4 MB (145438281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6f70c61df3b80f0bcd01f6a8184e39b6e51adca3f36dec5f5d3471e813a527`  
		Last Modified: Wed, 22 Apr 2026 08:36:39 GMT  
		Size: 91.0 MB (90986410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04fde21b30df920f9014b6178f068823a87dd610915f1ea9a021a327eb7a17`  
		Last Modified: Wed, 22 Apr 2026 08:36:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66d0ce1a22c06a3fc9d4092fb1787b0c11cc8e816ca4d4e8021a0bbd01543cd`  
		Last Modified: Wed, 22 Apr 2026 08:36:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:86af698674f03f521dcb247cd1018406c1a66d1c6060857219b7c8eb1fabd0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f298fcd6f467961a50bf156d7f84a81461aaa99a71a3bed986ac2a4df1faf95`

```dockerfile
```

-	Layers:
	-	`sha256:58939ceefd75d554af35bfd70de9dd3c55929c4f741c9c27b49b8d04ce7d3285`  
		Last Modified: Wed, 22 Apr 2026 08:36:37 GMT  
		Size: 7.5 MB (7475142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8006820699e4809ade0fc00aeda77b4c5b5f608f1865a0cdb5889dca2d11befc`  
		Last Modified: Wed, 22 Apr 2026 08:36:37 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:ac6767af67ef37b8f7bb89f0225d02c7a9dcb25640fd49eca1f784d4edb7103c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278087570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8110c73b156cf9dd7f54b964c49b93fc556258d5f8660a843cbd5f57b12e89a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 18 Apr 2026 04:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 18 Apr 2026 04:06:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 18 Apr 2026 04:06:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 04:06:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 04:06:02 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 04:28:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 04:28:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 04:28:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 04:28:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 04:28:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffc354dbc62d2fe426028f99b2388496dd161130055d4d78bf40c555ad79b11`  
		Last Modified: Sat, 18 Apr 2026 04:12:12 GMT  
		Size: 142.7 MB (142662936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245f4fc9b6e354850f65d93b967bc13a5fb3e01551f10a1d4ad10677a7374c49`  
		Last Modified: Sat, 18 Apr 2026 04:32:48 GMT  
		Size: 87.6 MB (87630963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc028c56392389ca261838c1b5c74e9d288061b791e9f5ac1969756a7a49e57a`  
		Last Modified: Sat, 18 Apr 2026 04:32:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b0af7d50bc69eec10abc57cd63d2e98f89f5e57127753d268019abe23f3edd`  
		Last Modified: Sat, 18 Apr 2026 04:32:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:41c8fec980f2c402221f7d2c38d35a1246dcb5beb9360b977bf81ac41987239b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7472465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98f49e3eb0667e5d2f20937b2630c583476a52b9a7b225d76e6036cefd88498`

```dockerfile
```

-	Layers:
	-	`sha256:90f8e4cc4550fe4d99664f73bb6a875359b478a05f66fa7aa4d2893140a3baec`  
		Last Modified: Sat, 18 Apr 2026 04:32:35 GMT  
		Size: 7.5 MB (7456663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb435db38f6ec79940bd17ef8fe3c6e7addca503abf8b6feebed0ec5de599cd0`  
		Last Modified: Sat, 18 Apr 2026 04:32:32 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a2ce3ac3a773f5d1f56bf4becae6c7e594c16dbd355a093e2ad548493f901d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271545507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b0bb63bfbc746a4745ecef005b63c5c75658f902e5408a604ab74824aaf9bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:02:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:02:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:02:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:02:08 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:02:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:02:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:02:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:02:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:02:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bdf2a5fa643efe0a338a41632a93331b8ef5e9ff59f12ff100e1acc79a8c48`  
		Last Modified: Wed, 22 Apr 2026 04:02:58 GMT  
		Size: 135.6 MB (135627001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f0d160a298654cdb60a8dce3d117a776855c9233be01e89c4b5dc68eaeb317`  
		Last Modified: Wed, 22 Apr 2026 04:02:57 GMT  
		Size: 86.5 MB (86545358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac60a56f4dd90208d6c5ed19124485e5e5ed3bc4bc12ae77557e09175a27a7a`  
		Last Modified: Wed, 22 Apr 2026 04:02:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9764f978077b5eae2193478b3e02004c48f4fe581643b257398b92339ef534c5`  
		Last Modified: Wed, 22 Apr 2026 04:02:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9a5ce71978b41cbaf0ba309e2df4c5b4f11197b4bf96c48175c93b0d1a3dbee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d38c336906c63265228a65f7c0a51e789fcc21e53b7b04400fa71fd5a056d6`

```dockerfile
```

-	Layers:
	-	`sha256:d6645f2703e665e2aa269c282c4b961d4b1b109557af72b24c40fd71df13e45e`  
		Last Modified: Wed, 22 Apr 2026 04:02:55 GMT  
		Size: 7.5 MB (7466643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30728161dff114bec41e7a9011b0b9c4897dbb6a3c1a38e30b774de2aee3088`  
		Last Modified: Wed, 22 Apr 2026 04:02:55 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
