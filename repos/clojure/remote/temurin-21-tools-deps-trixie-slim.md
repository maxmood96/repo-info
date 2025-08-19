## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:2cccf3aa3c722e8d9f29da9de05610ec75d77bdb82c8fda5729c007499ebfa9d
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:683e8730f2445db467e7861781dddbddcf3bef9abb9912dc7ae9a5cb44bc738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259468277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6ee6ac4a80ebee91338b00bc13bd6f4476646ae8d001ba10c611db22501744`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3752db42006518488a1cf673651ac77a7505b34f21f140c59202bef5b2f15c48`  
		Last Modified: Mon, 18 Aug 2025 19:44:24 GMT  
		Size: 157.8 MB (157804778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f26964ff372afd4947b74194d22bcb7818b6b24024ad2e40e445d2d12d7d66b`  
		Last Modified: Mon, 18 Aug 2025 16:53:25 GMT  
		Size: 71.9 MB (71889169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc939310fd8751dfbda0ac28ad6386ee784240c8bd9e493c195af4b0165cf5b7`  
		Last Modified: Mon, 18 Aug 2025 16:53:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ddc220e2af95334d12938232f3f0cae686fc4dab8bf2094c0fe2e05405a32c`  
		Last Modified: Mon, 18 Aug 2025 16:53:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1efdfbdea34fc1b6952c06199b1c469ce7a3601c0261aa30eb397be66b40b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d95588ff84d9915c0f223feed76cc3a822b747e2817e3e9e7bdfb5f972341f`

```dockerfile
```

-	Layers:
	-	`sha256:4f4ba0b4b34c17673ef0ee720d94bbb42a1ee39b360d8fda3426354e0ddae2c9`  
		Last Modified: Mon, 18 Aug 2025 18:41:48 GMT  
		Size: 5.3 MB (5259027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7a57f50c283b212a5bbf8821e698c12cc2c3ded969103566438477808212fe`  
		Last Modified: Mon, 18 Aug 2025 18:41:49 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c85f5b266f42d1b58a57ff4d439d24492a680db6210130c5b714603f0c60b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257925092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edb45207180169955a9b14f2a1d4121d3f2784753231d674a9ba3f2abacda4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a56322ce1b94f29786d8f76971f53596ba74b5abd690c1219b73a7ffedee07`  
		Last Modified: Tue, 19 Aug 2025 01:33:36 GMT  
		Size: 156.1 MB (156081245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3871bd30769192ed644379aeb028bca4c01bbc6d11b96344e70037acbd72ff`  
		Last Modified: Mon, 18 Aug 2025 17:19:06 GMT  
		Size: 71.7 MB (71706759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011f1e864520b4c5fee552e8c75433c453f0262b2c45556338d786c2a2d07260`  
		Last Modified: Mon, 18 Aug 2025 17:18:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fdb1602415132ab7830b014d5d937ed1b1c3c582b243c249d5fdf76b5bbb83`  
		Last Modified: Mon, 18 Aug 2025 17:18:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:61e6c5a4706cb565173816b36c011dc8dd0d8df039e3c49c16aeebe4d7762b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd2c5df3899fb926c81bf0d45414872a72497f7a9c7ce8ec9af5b8e9a6fd889`

```dockerfile
```

-	Layers:
	-	`sha256:475f24271b5e92fb8a4525f5007f1c13a517a459eddd04fe3e3484e7400863bd`  
		Last Modified: Mon, 18 Aug 2025 18:41:55 GMT  
		Size: 5.3 MB (5264820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af381ce48ea6a047a02cc1ecbd4b92998e4245f6e23e57b47adf623b04c2fdeb`  
		Last Modified: Mon, 18 Aug 2025 18:41:56 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:477dbe11ef340252649723f5c5ef2be2a75082a79b611b41a339fdf4649298ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268848693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856b14fa2b36bcdcaa4cc0513c9c9ee6547c80951c4d0477e939d9ee459bceeb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76db67347c5c0e38954b6134693282ff85f1bc2687c9bcbf31e1561216ec1730`  
		Last Modified: Tue, 19 Aug 2025 18:06:49 GMT  
		Size: 158.0 MB (157963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fe20c3590179dea93033a43edd140d5e8c47921d36adf1fa7ebf3de0413b4e`  
		Last Modified: Mon, 18 Aug 2025 17:33:58 GMT  
		Size: 77.3 MB (77289979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b208509fae9dc5077ae1462db574ea3ce3db2d87eb67bd025562a15a323394d`  
		Last Modified: Mon, 18 Aug 2025 17:33:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8140e1385a3a47f0891daaa3ec5afffb0532c11bdaa062d93abb3294c6450d37`  
		Last Modified: Mon, 18 Aug 2025 17:33:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ce53354a98b7648703e79d674b73bffc89a4cb8764e2e18122639b1b59bbcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a5ac281dc96deca0659317eefd3fdfa027fe0c5d7b08a0152fcfcb54efbf05`

```dockerfile
```

-	Layers:
	-	`sha256:7faf4c829f8ac3c3084fd3370c006448d2143b8f9b067f064f128b61c562a6f9`  
		Last Modified: Mon, 18 Aug 2025 18:42:02 GMT  
		Size: 5.3 MB (5263410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e58add7882e45c69a2fe38d0d5882a4363e9e0259db5c8fadbf5c72c9438142`  
		Last Modified: Mon, 18 Aug 2025 18:42:03 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:f6eac7fb2bba9ef5c0faad1b36a0814e89942d058bf12431fed69255de7d8afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252597673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d5cbf55815a7b327fe57d05a0656d7280eb46d846c02cd3bbb02fad6115835`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662dba36dcd67f9038af089e56bf1ab19b59362a93936c6c93b038356d30843`  
		Last Modified: Fri, 15 Aug 2025 07:44:23 GMT  
		Size: 153.6 MB (153593494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac05d52cad6714e7b828e367219445c623ae7c32f216c8a067b86a7dc2f75ad`  
		Last Modified: Fri, 15 Aug 2025 07:58:53 GMT  
		Size: 70.7 MB (70731513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff7dd76aff94609b000dc5410ffbce37c920e526f2788c20dd44d2ffcdf58e3`  
		Last Modified: Fri, 15 Aug 2025 07:58:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb62504fa2d8ab0b29bbc5ef2b64e819bf4a6a524ebce87d04494b8d40791f3`  
		Last Modified: Fri, 15 Aug 2025 07:58:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0d91840f13260c7b0147ae80506b1a30c6a6480d7eb20cfcf9df4a304a7c97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d7519371320b129455e36933e82950a679fd7918212b516b4cf39d8c470520`

```dockerfile
```

-	Layers:
	-	`sha256:0a7c7d26203dee6b5c5852b5cf418a11ff1a833df888be3132ad99ebeab6101d`  
		Last Modified: Fri, 15 Aug 2025 09:36:54 GMT  
		Size: 5.2 MB (5248474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96f1855480caa65b09485feac3fde2496e6414541d504f61a2a807940b32e738`  
		Last Modified: Fri, 15 Aug 2025 09:36:55 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2a8bc8157702575ec8bd3eec97a6996c2a4ec6e5484a0071cbde2776128c3355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249711157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41caf566661ed6b0be22a023a3cda22f3a624e16c349ec95b12c9b2f2581c6e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb1da63a2e6ff87dd1df9af5da65d1cb06ecd89a53f42d9ef6f63cbdd40d75d`  
		Last Modified: Tue, 19 Aug 2025 18:06:35 GMT  
		Size: 147.0 MB (147026954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2e6545ffb49e9b0eeaf372c6fb8d4e1078c041737576f288b1cd2fe5bd41ab`  
		Last Modified: Mon, 18 Aug 2025 18:01:09 GMT  
		Size: 72.9 MB (72850100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7c6c7a99491cfb30fdc3c386db656726b6fcfd825179c9b39b85e8ee3c5ee8`  
		Last Modified: Mon, 18 Aug 2025 18:00:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2889d4fa36c0ac22472052bbba58e51e46c38d3493f53384b45c36f11a95cf`  
		Last Modified: Mon, 18 Aug 2025 18:00:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ff0764985222746d42e5b32e265f4a4149043b12b78dfa1441756db50b9abe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89317330074fd257265ef623496eba61eaea10e953b4ef247c7b3e277dd6c1e0`

```dockerfile
```

-	Layers:
	-	`sha256:c3af127d0e70f55bdcda4decf698bf54ece65da4fa076a9e329ecf52d43fc51a`  
		Last Modified: Mon, 18 Aug 2025 18:42:08 GMT  
		Size: 5.3 MB (5254951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30104aabfc3a6b2acfc1c52b15a86947614a64480d884e2d2c8e4b445a8c1112`  
		Last Modified: Mon, 18 Aug 2025 18:42:09 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
