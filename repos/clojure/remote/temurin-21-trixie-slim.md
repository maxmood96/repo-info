## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:43164b84f999b12466a28fff69d924ccab137299d497e0c950115c1cde88551e
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b6f5c48b17cb0c1e2b0bbcc7e481e94b1de5336a1499ceccd82a086aa2935f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259208522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c66d6732c3e6740ba974e55e082cd217a824e0611e3a165cb02726b5fd0d0de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbf043a204d12486f78a57a85e3b8c30cae9beadc95c3a9ad6feeac5480e8e1`  
		Last Modified: Wed, 02 Jul 2025 10:48:08 GMT  
		Size: 157.6 MB (157634482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caebc59988175135dfbc46fcbf2e2196be6a688996a30991c7ffbb2437e0dc0`  
		Last Modified: Wed, 02 Jul 2025 04:17:19 GMT  
		Size: 71.8 MB (71811896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a0dac1d9f7cd5ec78f93c97fcf949d411e0eaf393f179cef85f5b202ba44d7`  
		Last Modified: Wed, 02 Jul 2025 04:17:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9853b06964755001923b1ac56cdbd81cfa99c17fa2d15c07acd46437c0055c1a`  
		Last Modified: Wed, 02 Jul 2025 04:17:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38fcaea237c50965f025413cadb5226f2470426e2a1a7b1b6222466b639aad88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049fd943aac8cbc1b977c1f9e3a000a0bef05d678378b32e4e5a3219748fec47`

```dockerfile
```

-	Layers:
	-	`sha256:3ad3e2681522368673a7de68ea0b8a342f4706c11849c1207d3eac70f2e67867`  
		Last Modified: Wed, 02 Jul 2025 06:40:37 GMT  
		Size: 5.3 MB (5256592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd742319ba8681da1aaf5f0570c70bf9f7ccfca9ca42a534a2214560d66cd597`  
		Last Modified: Wed, 02 Jul 2025 06:40:37 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f6bbfc487038fec03c56288a3a9c99f5be0ab213968c4672ae39a9b5bcdc75cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257699434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c8ed72d1b608bc19649a22a3f22f9c5714404e0a750c6af72c5556eaa5e5fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33408eee024be9f3a1569105d39a418b9b3006a0916ce219dbeccf4c776b3220`  
		Last Modified: Tue, 01 Jul 2025 15:56:38 GMT  
		Size: 155.9 MB (155928844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e35b813ecf57e2a82ce296108280dd379e21bf0f8e717eac8effe4346ffe15`  
		Last Modified: Tue, 01 Jul 2025 12:36:04 GMT  
		Size: 71.6 MB (71642686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f8db61ca3ba8aa3513098ddfe7299a36734c9ccfe6c93876d55c2ce7c3ba11`  
		Last Modified: Tue, 01 Jul 2025 12:35:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3f25188028b5439c54b181b1dfc9024e73b3e4e0e9860a2ad1a7d4ae1742c8`  
		Last Modified: Tue, 01 Jul 2025 12:35:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:940e157590a2eeb3fd2da4af80058ad2fce181f9de93b8a6408a39b7f0762bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8690591c5ceced56519682451ae34b6b2bfc32825ce1857d3b6c8ce093e5c4c9`

```dockerfile
```

-	Layers:
	-	`sha256:b300fc965733fac67e35717893d55c2aca057be72185918880d12eaf37832bfa`  
		Last Modified: Tue, 01 Jul 2025 15:39:28 GMT  
		Size: 5.3 MB (5262385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d67cadd1a9faf4469c886b6c63717847a19e2b138708249910b9baa4d9ce64`  
		Last Modified: Tue, 01 Jul 2025 15:39:26 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b227751c68cc3c3b44ad9e321d47aa66a9dcce005f8b694684276ffc93f647e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268625008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5f393cfe9b23252645f4316b8163778e2cbcedb4976da1d9ad6d0fa29a5a8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae953f03f2b72422dc965731d45dcf8ea88df04b6dca42c91876de676d5df888`  
		Last Modified: Tue, 01 Jul 2025 13:32:13 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7189516ae1ccf60b731ab138f65d2a93db9bf3a6b22ba3c0cad1754b58731988`  
		Last Modified: Tue, 01 Jul 2025 09:07:28 GMT  
		Size: 77.2 MB (77233027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8b2a6b76ce57281a56c441f648356c057bccdbf33ec67a0e5ab1f7fb69a68f`  
		Last Modified: Tue, 01 Jul 2025 09:07:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1bfd0aa86122754f29cd73e88cf4f091db8f84fe067690533ee08698d774e1`  
		Last Modified: Tue, 01 Jul 2025 09:07:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88a6108f30413ceb3756d162b6b252c12dc45ffad3bef8a3998f5e4508e9876b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4106c8c2b10d8c155c2509e5389218825bec5dd952b6c2e23dd5c2bceb0c61b8`

```dockerfile
```

-	Layers:
	-	`sha256:75e538c4b91e9aea32d252ef7fe46f1579ba10f5ffd16dd373ab7e230bdce850`  
		Last Modified: Tue, 01 Jul 2025 09:40:11 GMT  
		Size: 5.3 MB (5260975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c0e32a18ff7603ee97f623b379878c0e4852bb5518b6c743857ec649dea26e`  
		Last Modified: Tue, 01 Jul 2025 09:40:12 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:70b1a7043b7cf4c72ddfe6413b5fe7e16142aee6c34c7ceacfeb5d37ba5f098d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252413181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7888e3aa7ccc71a1215df6a48b29a39c46db9fa96710ecdf42cdcd7b1d8fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8616f7bedb56894be7fe53d122ffb03b37e9993aa4c114656ea59dd01cb38176`  
		Last Modified: Tue, 01 Jul 2025 13:21:21 GMT  
		Size: 153.4 MB (153449650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af318ab6a70500e9f73e09addf22a7ee42a01065a08d029534a1d7116e26517b`  
		Last Modified: Tue, 01 Jul 2025 03:25:15 GMT  
		Size: 70.7 MB (70703521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7559d357ed5b8676e56512a4bee290f27190afb11f0e2ea7a4c9ab9adb65bf4a`  
		Last Modified: Tue, 01 Jul 2025 03:24:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ecc037f824488fad2fc66ef59b36689e8b95302419172b397631f0062ca2d3`  
		Last Modified: Tue, 01 Jul 2025 03:24:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59435b20bfadbc4f22084fc8b672f97afb1628957761a3bae6cd518721ed1d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cb65f0944d1cd0143fceb6f4f914ac0ddb1425affc0da6833f0e0376738737`

```dockerfile
```

-	Layers:
	-	`sha256:5f1505d1f62341f4800b88c82429be5330fa481b22a6ab56fe9c4507e0a1e63b`  
		Last Modified: Tue, 01 Jul 2025 06:40:11 GMT  
		Size: 5.2 MB (5246068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee36271a7d0a5d62557d71cf8262d2b24d0ed07631786c2c17bfa30d65a5e2a`  
		Last Modified: Tue, 01 Jul 2025 06:40:12 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e7e560ca52226cc68581fa910e16fdd55d6594a11e2c62babf07790676a60b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249552776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1cc3d4c5faf90eeeb9dd4aa3ca80afc12ae369c880f9cfb442343918e8066`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3de81f4a29affad19a69c6ea53405aab7b55e447a36696f72bcf8c5ff83f16`  
		Last Modified: Wed, 02 Jul 2025 06:49:21 GMT  
		Size: 146.9 MB (146911007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744d75a25197dc35b5be858fd176b5d2c89d99bb30812a0a5cde2cd7acd5d139`  
		Last Modified: Wed, 02 Jul 2025 06:55:02 GMT  
		Size: 72.8 MB (72802385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accdb3c0b9f6c2e3b93de053b294ebed00037a50b0fa1829ac00529b0d7781d5`  
		Last Modified: Wed, 02 Jul 2025 06:54:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a213f6638ae4f3a230c3b203b3e59781b80e01bd39a822e9a216a76dc915ce1`  
		Last Modified: Wed, 02 Jul 2025 06:54:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:664c14df8f2cac3bfa438da6229cd5c89f1a342d9b6b2e421dcffe14236f995d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36522f84219bba176ad59f3f99839014af59b3a0d56faf57206a4d98c6ee131`

```dockerfile
```

-	Layers:
	-	`sha256:6746f8c8005ba18138207bad45257890566591c39eb68f4d71f68a6fa1348814`  
		Last Modified: Wed, 02 Jul 2025 09:40:12 GMT  
		Size: 5.3 MB (5252516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad6df8cc155143f8d76de5cd6ac137029dd97ad753e8d2fbe52db146af8ba95`  
		Last Modified: Wed, 02 Jul 2025 09:40:12 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json
