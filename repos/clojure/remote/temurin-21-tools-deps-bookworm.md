## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:48e7ec68ad3428a58d81d09d2a3fb317add2751585026899857b75defad6a5d2
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bb1332b148570acd8e026a181708bc65f1311e6c8161ec19466d7560ba6f7dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287513352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114934c787e3f3dee8cf32a2d0fa18f79eb3319b25043f1122a4c810f9000e55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:16 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc807d263e14d09a0c0c239598fdf5fdb38c7beb75974194be9dacaa976b09`  
		Last Modified: Wed, 15 Apr 2026 22:05:56 GMT  
		Size: 157.9 MB (157857054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e8c816ad3da8590935f328e0a4c8055e14283e20957b65a3c52dcc42bacff1`  
		Last Modified: Wed, 15 Apr 2026 22:05:54 GMT  
		Size: 81.2 MB (81166433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1894a37a64257ff9adb53753d7db4b706565d3c88d4849008952f0d14ecf6`  
		Last Modified: Wed, 15 Apr 2026 22:05:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f476cb4c51c91acbf6a464fc4c5e4de62978c4fb83c60bf6580f32155da8a11`  
		Last Modified: Wed, 15 Apr 2026 22:05:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:84357aeed88f65f52e23397ca2d42eecbbdd451b8fd2367a800ea734be745b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48786e0b28c055c51222cacb7016dcbac6d5c72e1991f80d57b3b8990656c853`

```dockerfile
```

-	Layers:
	-	`sha256:31c4b49a0941f4aa78d62e8dba0a4c49ca90ba162a18c5d483fafa10102d2e45`  
		Last Modified: Wed, 15 Apr 2026 22:05:51 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362e0268296369cd4dd2e21a05613cd8920e946301e3e2df29ac6518d8724c13`  
		Last Modified: Wed, 15 Apr 2026 22:05:50 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f64f358ccbfb3f197597fed0896f78c8691cbb068bf26f20a7284a404f13c051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285679035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c6c8cf3404ab34925b4d0729716d4b989a2355fec387e37b5b99283fa52a91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:16:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:16:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:16:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:16:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:16:44 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:16:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:16:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf52751f9d74629b64586e16eb7e6a2dd7c853659c90ebfbd03004c1debbca6`  
		Last Modified: Wed, 15 Apr 2026 22:17:26 GMT  
		Size: 156.1 MB (156133027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627d12def70263ef91ae110beb5495274bbf3e79fc51d7999e4cd2769bfac373`  
		Last Modified: Wed, 15 Apr 2026 22:17:24 GMT  
		Size: 81.2 MB (81171707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4442ac741716b57cd5e288c40e93b50ad7392506565b213f36ade1d6a6e793`  
		Last Modified: Wed, 15 Apr 2026 22:17:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c9139cb4b476a2bee1d9ba998e7fdca3ad5010127e921a235a2dc80caf3a2c`  
		Last Modified: Wed, 15 Apr 2026 22:17:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8ddcc3369f75004c36362563f622950318b0b5a29df46d6491219a4ccd6be7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fef156a966e0348fdc7b54f56f9583442a164cb54c3757e44cfe1a35ed0d3de`

```dockerfile
```

-	Layers:
	-	`sha256:7227c223b82f194089d13865303e9224aa43c42b73621663542d1301df08b17d`  
		Last Modified: Wed, 15 Apr 2026 22:17:21 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4773ac2d623bd76b69d82726fca963dfd27e60c64f6074ce3a2fdecc766db81e`  
		Last Modified: Wed, 15 Apr 2026 22:17:20 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cd471b2de0150752153ae3fb47beafc32527619e0ed7f33997f1276fd48497f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297319703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8dfebd0009f7744c8e16f9da6b7a06cb020f233a502167a7b203b960e9c5ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:58:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:58:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:58:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:58:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:58:27 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:04:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:04:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:04:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1250e3e4882e6e928fe5b248de7b760cd787cd434e4a4d31f63aa8ed6c00e040`  
		Last Modified: Thu, 16 Apr 2026 02:59:56 GMT  
		Size: 158.0 MB (157977483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e1679c7fc0758ed24a902d450880b010120f98cb0320d8ef6250007b191c4b`  
		Last Modified: Thu, 16 Apr 2026 03:05:09 GMT  
		Size: 87.0 MB (87004239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b81ad85740b10f8ab8bd819a208d7d2e499abf0803ce9313c0654afcd08ece`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c4482b634ceb998e5383955076f3d7481eb902d240dcb2d39a7eff50b3c2ad`  
		Last Modified: Thu, 16 Apr 2026 03:05:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:00c8644f7b8aca84bc06eec1cd587b11d35f11b4ede01c8d61e089fac602911a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427e567b54b1f802d0da3d3644ad66301ec195bb9d361110f664d278b205e0b3`

```dockerfile
```

-	Layers:
	-	`sha256:4954f32d5e27968b16695d9e486e8fcd26e92d44f55434a708334bb66de6e695`  
		Last Modified: Thu, 16 Apr 2026 03:05:07 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa52ffa0dc24ea2edf0e612eb3d21fd0e0b0737e9361545f7678f0a72a018fb`  
		Last Modified: Thu, 16 Apr 2026 03:05:07 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d57238164b118830eec43717672e2f25f3b4d8a1acf69d97f7267be455810283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274234504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4054230065faedb4e2f3741ab2a85ba8f44f5a011ad802a7c63522a2ac0d6f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:41:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:41:54 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:42:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:42:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:42:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:42:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:42:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b0fbc569e5eb992d36e1e7d0f1837586a776e70d2a1fa511f4869bda5edae3`  
		Last Modified: Thu, 16 Apr 2026 00:42:44 GMT  
		Size: 147.1 MB (147105233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7a4dac0830daacf75270a8ec9c3846d7f11951ff93b3af515bb6b20509d6ff`  
		Last Modified: Thu, 16 Apr 2026 00:42:43 GMT  
		Size: 80.0 MB (79980147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0421ce775d268ad38bc27cf51e70a900ef9d33c2f2e7019017d5b25605e50ff1`  
		Last Modified: Thu, 16 Apr 2026 00:42:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fd8cf4b1410da52a6c7f493bc1ff916874422f28fef4646eb23f3076225fe7`  
		Last Modified: Thu, 16 Apr 2026 00:42:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9dc3e952daabda2e1b798f3160d6f101574a6bc3a8be6b5f01457cc180bc69f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d7c2ef0b5dada35937386833dc9aee8236d5acdf2d0ca499e08d59951973c7`

```dockerfile
```

-	Layers:
	-	`sha256:b0f2724d43e36f1ee7be2bbc166001ced565f2808258036bed25cf8433382567`  
		Last Modified: Thu, 16 Apr 2026 00:42:40 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052d7ed46522ad2f98d1da3fe90ee339acceebd4749197c337cf473d66f346d7`  
		Last Modified: Thu, 16 Apr 2026 00:42:39 GMT  
		Size: 16.5 KB (16461 bytes)  
		MIME: application/vnd.in-toto+json
