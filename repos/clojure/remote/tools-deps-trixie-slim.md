## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:fa754d5083a7fd5d09edb55bdb7ff647c4de514f0e38d05e2b24b7ff16543ccd
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:478b23e632625a7406e630ff51fa9b8e935ad4afaa81a00538c3148e6a705219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259208491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b40383861a859d22640acc52b2762cd0bdbff3631337a5262e3fa224710d576`
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
	-	`sha256:3aa7d4d69bb1662340c2ed06dd63a27c79e754a7eb1446fdde8f1c96de05b719`  
		Last Modified: Tue, 01 Jul 2025 12:52:53 GMT  
		Size: 157.6 MB (157634485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b3f22c2aff5d8cbfbc910fda7067065e05f32cf21f559d60088ecaa82474e7`  
		Last Modified: Tue, 01 Jul 2025 12:52:52 GMT  
		Size: 71.8 MB (71811859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef197231886b03140d08453ec55257b84c0f59f495093954ea405e70ebe5b25`  
		Last Modified: Tue, 01 Jul 2025 03:58:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b4945aa7117d2c254750dcf44d8e9c4bdffba60605716b06c69d9bd71de24e`  
		Last Modified: Tue, 01 Jul 2025 03:58:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bedc8edf58bcc695d3191db590b57e4f5367d53385c2d2166d728baed7624446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294ee238acf139c6201dce79edc5831f378496f577c36d03352ee5837f9e1477`

```dockerfile
```

-	Layers:
	-	`sha256:a144da80fa6b9b5c8df2fe32f39fc791e95c3aa6cc7ec3e4fe56928c3d11299a`  
		Last Modified: Tue, 01 Jul 2025 06:39:53 GMT  
		Size: 5.3 MB (5256592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e726ce52ef890fd2c9a7042c9a7453648aed8f78019caeeceda6efe4006ef9c`  
		Last Modified: Tue, 01 Jul 2025 06:39:54 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-trixie-slim` - linux; riscv64

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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:937be47f55c745e2da9842e4e19d9fbe9c2df590c7b940810bd77c85cfc0c074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249552792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa27980d221e429dea8612653f2173d94492c513d1d9e998510f70bd63b0cb5`
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
	-	`sha256:70dd568d328953786ac7c9c75198e650ad95784e2729067cd6b7278363d6f13d`  
		Last Modified: Tue, 01 Jul 2025 08:20:09 GMT  
		Size: 146.9 MB (146910997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf867bc69032ac50127524191ac1b67075246dcb6694266db0e94229e3a3c680`  
		Last Modified: Tue, 01 Jul 2025 13:34:00 GMT  
		Size: 72.8 MB (72802410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b74ff4139f963d10f3dde9d4c77aefba82bdeedb1fc68f710ca7152b48d45`  
		Last Modified: Tue, 01 Jul 2025 08:23:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ebcf373a26d01b8c49a2373d70af997e6e87e954bd58ebb63a35e229a22ef9`  
		Last Modified: Tue, 01 Jul 2025 08:23:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a22de38ee56a1f3db2eaa9a945bdebceaa24e89a51ba4589182789a3a0786b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4e9e8b6289101ba537542c3be9d50da263478d517f2282301a014bea89dd57`

```dockerfile
```

-	Layers:
	-	`sha256:084afbd7015c8eb13247b508e071eb5e2d67a49f83ce0fb5da705f08eec8b122`  
		Last Modified: Tue, 01 Jul 2025 09:40:20 GMT  
		Size: 5.3 MB (5252516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dd2bca7442e504723fc57f3c5b665b0978d2ac6300af00e73f8758d56648598`  
		Last Modified: Tue, 01 Jul 2025 09:40:21 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
