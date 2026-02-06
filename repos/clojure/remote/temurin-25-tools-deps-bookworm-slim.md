## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:fb1a992b3795a8ad297a7ba488125a5feb789db86c2a70cbe6b6ea89d0d739b6
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:49ed7b595421a20a898348f28aed8af2ca2278c3adb4df7167fb99d07717b6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190163541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb2ed84867f1d732cc35da6a5e0d3e263c6d5ed961e34ac1adcfecc8cec7e16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:07:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:16 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58df071c961efe030a0c4ae18eee4f23b7423263fd53ec56c68665e3e498a02c`  
		Last Modified: Thu, 05 Feb 2026 23:07:50 GMT  
		Size: 92.3 MB (92256283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859d7614bd631d7e6e46b884233cca8ef3679fae93e4ab57a1f4722061e9a88f`  
		Last Modified: Thu, 05 Feb 2026 23:07:50 GMT  
		Size: 69.7 MB (69677727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1555eaa2e0b8ab23eaf9108c675ac1ce472774d432924b0a90b1f14ca8a175`  
		Last Modified: Thu, 05 Feb 2026 23:07:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11632a5e59c81af481d0f8107866ef6d52cc1ce9da43d8ff3750a9996f41f98`  
		Last Modified: Thu, 05 Feb 2026 23:07:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e89a1409c7bc269fbc65d8bf66cf28ffbaa38631e1133191ba2b4813475794c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf7448fb5fbd5c2f1e728bd46e9e7581fb26d15dc109a93bdc04869763668e4`

```dockerfile
```

-	Layers:
	-	`sha256:da13882e0ea9aaf4c471d3bc129cf08c4c38a0f925a035f85b865b54e0afe84c`  
		Last Modified: Thu, 05 Feb 2026 23:07:47 GMT  
		Size: 5.1 MB (5082748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd4ceb16bf77345e8de53077089df3a3ce46f68c2dc053af801719e6618f2240`  
		Last Modified: Thu, 05 Feb 2026 23:07:47 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2abed746abb60ef5a7bd1f46258763ee3edd4105fc460d8db0b69fcc188da9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189069851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b07860c46ca144eb07177501bf4a2d72cd66b36bc076edac59b4b2c85e6b43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:07:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:54 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:08:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:08:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a53af2bfac9398498b072ece97861c785b36c6f3b78357eee88b1d54e4bb1be`  
		Last Modified: Thu, 05 Feb 2026 23:08:29 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbcaaa09fdebd19bf42c4328362b76ec87ccf3b489c978a7ecd694dca98a4d4`  
		Last Modified: Thu, 05 Feb 2026 23:09:15 GMT  
		Size: 69.7 MB (69672711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f72d188d731be1f52d8dd14e48feab2d79d2fcf66dd063a106edb6e5b1710`  
		Last Modified: Thu, 05 Feb 2026 23:09:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393214cf53700891dd24db11b15722429a09e91461246b3b328a59f6511a079`  
		Last Modified: Thu, 05 Feb 2026 23:09:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:411d08700232e0b4cd4519149447873c593547c1e44a901196131da44cdab588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cbc8a5d8d9be1da2455921acf9302d43351bad2fdfabfd8f9d755d41f1e065`

```dockerfile
```

-	Layers:
	-	`sha256:7745de071da436a1b38225cf58277c386b108c27190b420e1800ae31513865cf`  
		Last Modified: Thu, 05 Feb 2026 23:09:13 GMT  
		Size: 5.1 MB (5088530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc3bb99876937e3900946a602a7c46c1bbd0cf54d380326dbc8b587d915233c`  
		Last Modified: Thu, 05 Feb 2026 23:09:13 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:83c8eda2a3cf3f6cba32328702fad5059475c851779134c3400873d22213d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199216822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fc958b58d01acd7176e51f6ab2352e48f6ee5282ac77174baff581b6619cf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:46:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:46:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:46:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:46:10 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:51:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:51:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cb234547828975d01511eb3f1e2f07f4c3226976323dbaf0a3fe8832f8431`  
		Last Modified: Fri, 06 Feb 2026 00:47:43 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7d1bff7a7aa17d12bfad8d52d8030be45d899e876e5cf39f0f2c8d9fcfde89`  
		Last Modified: Fri, 06 Feb 2026 00:51:59 GMT  
		Size: 75.5 MB (75514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feea98bb1e6e49d6287c83e30989b16ea90787b12d2ccf31792e8ce47337c41f`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f3e6a206e0bf371d7ecce2d701cc3627bcb799a2f65be0b2b875a0a201c6cd`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6c0830e1dca1578d0a01f0229f1fcce10ca4d151a5e887bfa3d018ebc8b8c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093db5e1b39899cb91fa4a744553f1cdaddb5d215735b0083ad5fb6cb93f236`

```dockerfile
```

-	Layers:
	-	`sha256:ae6cde9575c74875a271958450551dc22c10e3a261966655652c29e78440edf2`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 5.1 MB (5071230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77072055f2f3d6006a364706329fac99df8a7d288c7a6af1a1245872ea7e8840`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5fbb175a189882c3caf62e57e6917acd11bc2dd955dcadfa599e023d505ccf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183609108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818e0411f4af3afe3c851d59b45ff7bc3bbacd76020f715d1969db669d1ff0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:09:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:09:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:09:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:09:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:09:41 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:09:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:09:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:09:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:09:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:09:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189fee1a38e1d1dee751bc8f3d8e5e91fe8fbc5d67b44beaa51e99ba08aa5f8`  
		Last Modified: Thu, 05 Feb 2026 23:10:22 GMT  
		Size: 88.2 MB (88233820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cf95a8e28abc364d5bdd4bd71f6d589afa687e7730b29e8585c87094a96d72`  
		Last Modified: Thu, 05 Feb 2026 23:10:22 GMT  
		Size: 68.5 MB (68489860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc727604941f1a22fe52b9f2e6cf82126c2a0882fa15868b56a02b819eae3b53`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515ac85dd50a50b4ce3946a61b20127660e1bdb4691b4c40d68596e0077d8706`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:899f3aade18d94fa0d2c9bedd9608b44171bfd01520d568795267fca8042ead0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1090f20d039f088668f6a6560e8e017476f91753dd32a9cb2a7bcc0e4becbddd`

```dockerfile
```

-	Layers:
	-	`sha256:c186fe6a5d85db5d3e7648fcf8b249ff4bb26e1e671d40ff5159003bf699e457`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 5.1 MB (5058631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab543f7d36e22564037401796f5af692965e3306d8018098e006979f03a1691f`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json
