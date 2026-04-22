## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:f9c7ea66b235c32950e6f60470005a98ac793f3380ec8aa29bb28624d30deb08
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9c90d81bcc6b58f36e8cc893c7f9677b669274a4dd805b27eb86d45dd831f363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 MB (284009379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd90eb598105b9e7c18eb8929e70274fd6a174fec1ab6704796f3956c48cb9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:04:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:24 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b8ef79b2db274d32acefb5eec08dc02e862b48a65b007b80d97059ccfb7400`  
		Last Modified: Wed, 15 Apr 2026 22:05:05 GMT  
		Size: 145.6 MB (145628761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156a4a944f89992b8a22af0e6b5735176475ac8cf6af2d88688116c19e3c1cf6`  
		Last Modified: Wed, 15 Apr 2026 22:05:05 GMT  
		Size: 89.1 MB (89081742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ac4fe86f7bb32e87a9ccb7cc21d576fd70eb420dfcd9e4ea43e3f5eea67b9f`  
		Last Modified: Wed, 15 Apr 2026 22:05:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2ca02639d1412c865452707474edca7cd091b283475ce0353953c34800138d`  
		Last Modified: Wed, 15 Apr 2026 22:05:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fba4bacde863503f2cb1d08f1fe9b54ed68f6ddce7354c6cf45652a6525e6251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37faf5dc3b46b7d375eb001ce14f9f042aa1725a0499fb78d98a0884deea5b71`

```dockerfile
```

-	Layers:
	-	`sha256:81d261e764cbea3b39243b2160ce46f80b88216d6983abd902be95c8db705c1d`  
		Last Modified: Wed, 15 Apr 2026 22:05:02 GMT  
		Size: 7.5 MB (7470667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72cc485fd9fd9a0b1f2373fc52c6f4354b877c423fd593cfeee752a641d7150`  
		Last Modified: Wed, 15 Apr 2026 22:05:01 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fc24b6887061df4bc5bd92bd03ae9f2cf1661eda794196a29990dd07f9139e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293280260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e0877a2b0aa4591426ffa6d8349b422f5702851abb77e9fc929f40ff018d0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:51:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:51:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:51:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:57:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:57:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d63fa71f8a08634b0312e1df11dd8fc3363471d8c3e45af52999c7c3ba56e4`  
		Last Modified: Thu, 16 Apr 2026 02:53:12 GMT  
		Size: 145.4 MB (145438287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4f8ab741da512d80931a6a079143eadd8b6c2ede80fcd81c7b7fc15028c80`  
		Last Modified: Thu, 16 Apr 2026 02:58:17 GMT  
		Size: 94.7 MB (94722259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd1e215df1b1fc90d8e238c08e8a00506699e11a949d47283f46b167155918d`  
		Last Modified: Thu, 16 Apr 2026 02:58:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045a83e090065c566f36f08d430100cb9bc688b6f69fcd776c3dc42d6d26fb10`  
		Last Modified: Thu, 16 Apr 2026 02:58:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:59ef7dce9a92ae6986910399b37dca4a6952ef4a8f4c886d03d02b7b8fefbfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98facbdbe0b0baecfc782b4c659c74c04e214cafe813c9c3d873063b1c6844d3`

```dockerfile
```

-	Layers:
	-	`sha256:c08fc8bc92a5a7637f03b181c6c29b4a2631c4a6365c0f01c3ab8916eb66f649`  
		Last Modified: Thu, 16 Apr 2026 02:58:15 GMT  
		Size: 7.5 MB (7475088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8a0f943d96b65c3edef091d5f60d82af3c76c357a5b6671f68c5dd752fd8ee3`  
		Last Modified: Thu, 16 Apr 2026 02:58:14 GMT  
		Size: 15.8 KB (15799 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:42baab8fbc4dcd60b3828affb2546af8e0593641560e33cb5920d0f1408aff13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274703642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805dc7c986fe4e912065d9629245c43da138e4bde776a3d082070c7efc6590be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:40:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:40:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:40:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:40:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:40:06 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:40:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:40:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:40:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:40:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:40:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6479948f30389f45be50a1b625521e9d73b9d87a964dc77b74df7d56d2918`  
		Last Modified: Thu, 16 Apr 2026 00:40:56 GMT  
		Size: 135.6 MB (135627004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55540a3577121e5fee641560de9fd623ac07939e4e7e3570fcffafdff4664a6`  
		Last Modified: Thu, 16 Apr 2026 00:40:54 GMT  
		Size: 89.7 MB (89710491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df372882402ad98acee2ba5a63e5ed855db02caf8f4657f81ddc69f3e149652a`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9531fcad809e80f1b7f220b7daa70b184e347e77b4254460c4c6834d8a126608`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0b8bb6c699dc7f3cc4a7e4f28737d64da72761b0f902ddb222a267cb3523c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b695d8899ada382f8f85211490e160669c04bc33ec39256046add0a3c706c2`

```dockerfile
```

-	Layers:
	-	`sha256:d01523b48410813f814ae6305f6ddecf735528552e2b088cc3d874cce41fc7aa`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 7.5 MB (7466589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd63c64633e30285f736b45995fc4eea006337421437474302fe0e26a25b3ccc`  
		Last Modified: Thu, 16 Apr 2026 00:40:52 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
