## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:3ef5632fe217cc5412281c1b515e68071b6d5ec938eaf3ef7c3eab20f514972d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:fae319ed005cf8d493c61ff97be1632c6884fecdacb73bcaf92a46b23ca81ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294537393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1efc6498ac1db77ae3765c287c7f2cd2a0b61a033ce89f8613fbb464a056`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebd17a673fc9da8d99cb7f0199f0e2475f6e67e9d2bd0e824d02fc63116fcf8`  
		Last Modified: Tue, 03 Dec 2024 03:26:02 GMT  
		Size: 165.3 MB (165295131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991dc4564803a64fbc02ab752611a757b58403477e4dafbce175f34f95da442`  
		Last Modified: Tue, 03 Dec 2024 03:26:02 GMT  
		Size: 80.7 MB (80744013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b4bb920de7f788fe81f603a77ca1b8fb96ded53ea68c5dad5ad339037bd205`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063805a6d802d52da1d5df697e81a93fb57ebf55e195595980496281fbe9ea77`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:aab2d0a4cae597dbdae0a062912da83da7085c46b5bfeaa90990bc61fd015b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958cbf90119aa085e781f4834c6126febbc11e35bd42e407a649d61c23921ccd`

```dockerfile
```

-	Layers:
	-	`sha256:10972441f75a9997b8dd24202e320b35fce05d186322a9de9a5386d6be6da84d`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 7.2 MB (7186872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ddc96c97a0cf21b93c1e67777d79bc6f1764c51d4bebf740298c6599486ecee`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f41b0f970c1e2991b0b18e632af5c73460af6ba0ebaa3c87c1bf7f95c4405653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293668060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529ec133ed6eb44577dabe31c0daa311d0b2a35fd2e2ee2991bc82da4c33035c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39deae920147b40fe519b6d41ef8d1aa18333b66459594eed15473c7794b25ae`  
		Last Modified: Sat, 16 Nov 2024 05:46:37 GMT  
		Size: 163.3 MB (163281799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8731c564e79d437d930119be5db7c921a197260de4b14d9b1d39743fc949c7`  
		Last Modified: Sat, 16 Nov 2024 05:51:41 GMT  
		Size: 80.8 MB (80798022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f11bc97552923b07c695c910f21f8db136562904ed9a3e0964384713f190b`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455a56b03ee0659c5120a4abc6bf494e604a6b4103dcffbc903297fa7399feb6`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:d79cf9a4034218bc333ab66df58fca9f90bee74c4ac8906bf4c4237c95c95f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e523dd442cd38052b124ff3d5d5fd2008fea8fd266ca19ee7e02507f0f7a28e`

```dockerfile
```

-	Layers:
	-	`sha256:a6521166a761cd35ed562e0a966233e2769b32f0ee901fec1a92361776b24933`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 7.2 MB (7193290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef02329080a1131529385a2a972e7e183bf1b371b49edb989b62acf3ea68d04`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
