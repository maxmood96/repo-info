## `clojure:temurin-26-tools-deps-trixie`

```console
$ docker pull clojure@sha256:1ff98ca029f431e108a8bbc4ba0cc603e5b041980f060a8637fce48732d2d9b3
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

### `clojure:temurin-26-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2db79a48a579e40073c57fc6e854098d8674aa6ecf712ace646385b9113da90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226361719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676b09227409b9b50b827c7618c79207c470900e43d3c720f0ebcc9eb055ef42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:22:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:16 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:16 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308026d36d3c4bed53a011f03b31493f065abbc0560d4f0bdbad0e18bf30803f`  
		Last Modified: Thu, 11 Jun 2026 01:22:52 GMT  
		Size: 94.5 MB (94524364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884efc20b00da844258183f3f681f9d96cd838e18d0a6c71a700761f82189124`  
		Last Modified: Thu, 11 Jun 2026 01:22:51 GMT  
		Size: 82.5 MB (82519200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d67b67864a123fca59d31d6cd00396c417f1f54e63fad17fbe5106de75e82bd`  
		Last Modified: Thu, 11 Jun 2026 01:22:48 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b971c7f14ae221e1441c07f21147c435c45b8f80229d9c93f071bf5570b4e57`  
		Last Modified: Thu, 11 Jun 2026 01:22:48 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5e4da023743e8ccf9477d75b478e70826c865a35d7ac937db2defc59893ef1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eca96d0f76cfdccded0b648212694d20da66adf2cbf025e6e0edce68355aea`

```dockerfile
```

-	Layers:
	-	`sha256:3d92b6ac3e3ef6f77beb560664d614875861f934b9be3039b955831207f2cb1d`  
		Last Modified: Thu, 11 Jun 2026 01:22:49 GMT  
		Size: 7.4 MB (7433662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daed9502cb966f37c42e1940d54c24b07e265fb7e510b678872d0db0432a2dc4`  
		Last Modified: Thu, 11 Jun 2026 01:22:48 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:297019a7aace1697ec08757a3f37fbeba6082d9ae0f13369da8d4a11f0115e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225522228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c88009fd91e379b22deae5b38f1ea311532783b96e594a316035b16e7851210`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:26:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:26:23 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:26:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:26:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10946b24f56c2612fded382142be8da46f8cd4f9a32fa056ce3336c15205a91b`  
		Last Modified: Thu, 11 Jun 2026 01:27:03 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9bd65990034a2d678b9c39e79a9ae06b6c110416bc59bbcde690febc3cfaa3`  
		Last Modified: Thu, 11 Jun 2026 01:27:02 GMT  
		Size: 82.3 MB (82338672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4074d65f2e91b90af3344305ad2b6d2b1d7fefa1fb89f6f6af8132ddb225fb1`  
		Last Modified: Thu, 11 Jun 2026 01:26:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54086e76881c56f4f01063cc31a9d0ddee6f3fd6ab0a623160fba12dabd2cb19`  
		Last Modified: Thu, 11 Jun 2026 01:26:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3cc48fd094763c3265e6f7ea4e01f32c68097d27ce9d9c2f443d8d0cd9156eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66144e522080c5dd0b9522ee0c8ac4016ec1be9dbcbe9aeac75c15b1fdad3c9a`

```dockerfile
```

-	Layers:
	-	`sha256:d4b8566f26a4466a521b71c209767ec2a1290cf12d3bf3ae9c06c3e60ab0b97d`  
		Last Modified: Thu, 11 Jun 2026 01:26:59 GMT  
		Size: 7.4 MB (7440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedb1bcdf786b43da3c19b391d02b6590e66a666328c74f6254b950cc86cef42`  
		Last Modified: Thu, 11 Jun 2026 01:26:59 GMT  
		Size: 16.0 KB (16019 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ac500104ced796040f991b5ba712f63d294c52ce1eb2513a3bd1af28a89eb415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234973488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa9e070b9b06138be788576113dfb5ee57c644162a33066095914155d66114a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:11:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:11:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:11:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:11:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:11:26 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:12:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:12:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:12:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:12:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:12:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d4e5a75672764ebd26ebb0de7d78defd969db6824877814166a298385cb200`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 93.9 MB (93902050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291ae22018110ab9bce3bb8813caf4eee8feb3c2c48bd1f54e979489cb436c8b`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 87.9 MB (87938213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab5ea81211e2241017d3225c63fb61be8d8a1754612f9ff8655da04e823cbb8`  
		Last Modified: Thu, 04 Jun 2026 18:12:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc91a3f95ba8c0ec2fc60a9dbf98bc2a5200c2a32ee85914e9769e967dce6698`  
		Last Modified: Thu, 04 Jun 2026 18:12:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a4c154ad51c094f69967716e626f84275683a8e6d43469f3e2a49f9dc274b6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f17b755c8ce51aac546db7827e7009f7ab020cf04428fef2e772b55f74f9781`

```dockerfile
```

-	Layers:
	-	`sha256:c0adb965c84ce5cf5e6a0a702220227d8446768a4860e6de4c6c952504f205fe`  
		Last Modified: Thu, 04 Jun 2026 18:12:51 GMT  
		Size: 7.4 MB (7422019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f538b178919a9db2c3e8575fa09827dfaf424778b36748b61b899a14855dd9f`  
		Last Modified: Thu, 04 Jun 2026 18:12:50 GMT  
		Size: 15.9 KB (15949 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d279205cabffa538c5ba7f0882347406005151bbddd8747ca7d33b9994589bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223424340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70afd8cf5b8606845ad198f130a6d322f0709e701aca90982274aa0d438304c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:15:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:15:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:15:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:15:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:15:37 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:16:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:16:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:16:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:16:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:16:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cff8bbb29e668e8dc090e00a7af5aee6abd7ccfc1db8f297307fd489ce5911`  
		Last Modified: Thu, 11 Jun 2026 03:16:21 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09273ede4db3987de2bfcf59c694b0edc68fc4322782bae2117880b8da15f4d9`  
		Last Modified: Thu, 11 Jun 2026 03:17:23 GMT  
		Size: 83.5 MB (83500438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f478d31cb5a9965020a58e7eab312d870acadfb4d172bf17182477b5349c7ea`  
		Last Modified: Thu, 11 Jun 2026 03:17:22 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f2c2a02ad695f8145fd81d577846aba7627e80cd98129bf6b68343f1eb6ff3`  
		Last Modified: Thu, 11 Jun 2026 03:17:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ab46c5507b737a2d8142b2c4d27c6d232d35d137333ec5b9a1f3c408efef8042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c766d7851144b6eab89aaadd42918b99d734cea79a99a36e0d2665dfa2ef0b9`

```dockerfile
```

-	Layers:
	-	`sha256:8ece6c48fd454dd5506d85fa5d0dcca6f9c8a66fe51b23ddf285aac7e24f5a44`  
		Last Modified: Thu, 11 Jun 2026 03:17:22 GMT  
		Size: 7.4 MB (7414770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad23db246493f6763d8913d4bd2a1110e9b7e6eaecca519bc49d1998983a1664`  
		Last Modified: Thu, 11 Jun 2026 03:17:21 GMT  
		Size: 14.9 KB (14948 bytes)  
		MIME: application/vnd.in-toto+json
