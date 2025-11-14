## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:db970cae3d17e09af198107e3ed42ae8b7ed8d492a4b8cdebcdfd255fefcb6e5
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
$ docker pull clojure@sha256:284c750db895c46fd3f7c883ca79e241becd7268b0232a176dcbc8acbbd4b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287454264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df921e02e3ef0c56358c8aea401ab0cf0b2cd3f7eb8ba8acc8e4a0d18ea0d06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:25 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a021455fa7ddf4a144a574fdefd0ca9b6fdb5640391eebaecda41c115781113c`  
		Last Modified: Fri, 14 Nov 2025 02:04:27 GMT  
		Size: 157.8 MB (157825964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d5a5a65af4ab56a6d4d5a8bc01580c49f358d83e9fd0be8fd67441d72f890`  
		Last Modified: Fri, 14 Nov 2025 00:55:17 GMT  
		Size: 81.1 MB (81146199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25cb6829a00e4c34bd114daccf1158cc99da7de4d48e5856107ac70b93114f3`  
		Last Modified: Fri, 14 Nov 2025 00:55:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa0bf78b7eb8c5254a1deb3ee4fd2d61e13dd56016b113da78189b7266c66b`  
		Last Modified: Fri, 14 Nov 2025 00:55:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cdb00f60aa8ce1adff6c6ac352c6a1cdd6a4937c5b9ee540b80ab63009cbce3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e001c57d55a1774bf60a69a8ef139deff784934ca1eeab18968e566bc4440c38`

```dockerfile
```

-	Layers:
	-	`sha256:096165fed6cab3b8a3b51dea393ae00c86c1d63f79a60502f9a0573dd725a23b`  
		Last Modified: Fri, 14 Nov 2025 01:45:57 GMT  
		Size: 7.4 MB (7378678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:256eba9bfe469f7457e128f2415087680c8dc8f0b8bad72883f1adbf289dd6f8`  
		Last Modified: Fri, 14 Nov 2025 01:45:58 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c672482709a33f864d5acf66465856e5cb8ad7be8bfde512896a7ed515a2ada4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285499026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36aab2d6decee35c9b17788c302faff047670c67d78dd2c2114efe0e80e8859`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:43:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:59 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9defc4f2cd147898542a776a6853d1a1f802b01559aaf44a50f9c909c017be01`  
		Last Modified: Sun, 09 Nov 2025 00:14:08 GMT  
		Size: 156.1 MB (156107602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb3bd089a7d8323c7d715139d0ad0f0b658b7d2f20bdddace41fda708cadce`  
		Last Modified: Sat, 08 Nov 2025 18:45:02 GMT  
		Size: 81.0 MB (81030908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bb0b1b7b25296a0680015122c44e268a631008f0631b54426f52ff8d43c039`  
		Last Modified: Sat, 08 Nov 2025 18:44:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd9b5d208d4c9c773c2a0cb617327fd90e2eeb961ff424f5b8f77f47ae35f04`  
		Last Modified: Sat, 08 Nov 2025 18:44:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4abba77b88397413911e9bd7ef03ec4367126d798b836e0fd33bf31d5efb85e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb00082e0f9216c7fb2ca668d6b7c62d82f79cf8117753f27e0b0d0072b7c9a`

```dockerfile
```

-	Layers:
	-	`sha256:3c9c831624d6f3f345ad05761eb93a7d8d76a0c2d0259b5a18f774542c7bed91`  
		Last Modified: Sat, 08 Nov 2025 22:46:04 GMT  
		Size: 7.4 MB (7384465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:087583d2768bd7b1a2e080e8a05b9ca5aa7ac92df8ca1da48e93d260193eb999`  
		Last Modified: Sat, 08 Nov 2025 22:46:05 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:17046d8a12ae2ef35c8952c23ce6ccea9652417551e2e0b43ddd3d4feecbe14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297257422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d052781d31f5274a3da26d76356bbfa2849547e48f394ce91a6d03cc1c78bff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:30:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:30:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:30:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:30:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:30:07 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:38:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:38:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:38:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:38:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:38:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df5ddb30da5ca300b505c1a0ec8b4685bfad9925d2d21e6e9d69e16d2ad89d7`  
		Last Modified: Sun, 09 Nov 2025 16:12:20 GMT  
		Size: 157.9 MB (157942894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5524c4c3df17f9e53da208b38723eafba630f8b42900118ab5849ba245f42d8a`  
		Last Modified: Sat, 08 Nov 2025 21:39:15 GMT  
		Size: 87.0 MB (86986206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44934b50dce801c63d8b1fdb255bf7f75557a5d1af203f041be736bd8d77f53`  
		Last Modified: Sat, 08 Nov 2025 21:39:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f25a95d425a6d747ef74344b16bb695edbadc474ae00dca08af14ff2696ac2`  
		Last Modified: Sat, 08 Nov 2025 21:39:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68d76d48c2ca956618c243a69ee9d990b12b3415873ff4e178544d73f8c62128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2def9be1c873c78d48b8319f1eceef80e8f08c12c7b2a8374dd6dbff3dd9ba52`

```dockerfile
```

-	Layers:
	-	`sha256:30de8d4bdcf5817c619d13d404a8cd1cadc0cddaf992da3509521b174330f5bb`  
		Last Modified: Sat, 08 Nov 2025 22:46:11 GMT  
		Size: 7.4 MB (7383904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983ebd6317f0893ccb8d85df5b338ec2c7c79b3b37413807c305ad4de5f20797`  
		Last Modified: Sat, 08 Nov 2025 22:46:12 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:5685ad58deab4e119c1b2e850d4b27ab83bb9748cf186569f99983715496ab98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274165441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca5b447efccbbb9d96c7d38b01d5d79840ddc66c3d5054105ff2f3552c204d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:59:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:59:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:59:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:59:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:59:02 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:01:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:01:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:01:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:01:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:01:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462e287a2a6a2037bb196d8c5445c5c9a076e490ff81bbdc85238b6e72cd8f3d`  
		Last Modified: Fri, 14 Nov 2025 02:05:16 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c4a7b2980acc5e288f2e186c1c08ce1cd0b1546751a3a5fbbfb1827850836`  
		Last Modified: Fri, 14 Nov 2025 01:01:44 GMT  
		Size: 80.0 MB (79956476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b0f06652b19f37669d9480b515bc51d80b0af5e53169739793526785b086a6`  
		Last Modified: Fri, 14 Nov 2025 01:01:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c64993f8968364f16f8f8d6c5c13f624cfd5226d6d87d28eb7cfe34cde6fbff`  
		Last Modified: Fri, 14 Nov 2025 01:01:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bea0d744d7ddec9e9b5e06d6f712226cd7ee4b7cfbfe45fba157a84f9201c618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e30a94ef0c04aee51fe3c0d2bbb2a7662292fc73842d8e4ae759787117ea15`

```dockerfile
```

-	Layers:
	-	`sha256:b9b7cab41f1581b72c6cf3554812f4ab4018d1f0f77f25f2b229951ccb855ef8`  
		Last Modified: Fri, 14 Nov 2025 01:44:32 GMT  
		Size: 7.4 MB (7369997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f008993294d6d87205790ac457621302847a383ef1fc912dcbf6041ba706c675`  
		Last Modified: Fri, 14 Nov 2025 01:44:32 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
