## `clojure:temurin-26-tools-deps-trixie`

```console
$ docker pull clojure@sha256:f2fc81e7dc64d8d8e0f906065a96a90599746cd6f69f4e11a06a309362c988f2
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

### `clojure:temurin-26-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:7322c1fdf3ad77b66517bd561d1712541e8da78054d6bcec6f9a1f2d95ea009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229329283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109f396ffb689af52aff75cbed72abc727e43954ec3120defe0510b76286c1a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:08 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a02e159f63d243efd4dd0ac758e85d25fc9f1bb227e9bc74ede8facc7f50cf`  
		Last Modified: Wed, 22 Apr 2026 02:22:45 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03bd49fedd348068c4fa1ee7456e8c802c0a20c674c9e987ebd1f55b86fa1f9`  
		Last Modified: Wed, 22 Apr 2026 02:22:45 GMT  
		Size: 85.6 MB (85570452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a04d8441932c057fe76fce898edb76af6df6df05e76897cdd604ea17c3809a`  
		Last Modified: Wed, 22 Apr 2026 02:22:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf2e4c3eb7cab15095bb946c7f9a2e008b65cccdf43e094d911ad56394247b9`  
		Last Modified: Wed, 22 Apr 2026 02:22:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:94f9319dffef5e43cc1470882e25b34a2263ea60b25b4fc167eb3873d48ac470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaf1fe3f8634c18cf30e231761be3299b8ab6a633577585dbf2e2b8ec753842`

```dockerfile
```

-	Layers:
	-	`sha256:70ec719fa3feee96349da670d9e12cd5993768ec4b9f24e26476d5332815f741`  
		Last Modified: Wed, 22 Apr 2026 02:22:41 GMT  
		Size: 7.4 MB (7436225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad3f5eccfc27bad3f06a67611d0f67d551aa13cde676995b8c8b5f3383f7407`  
		Last Modified: Wed, 22 Apr 2026 02:22:41 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:565d32a6aa7f4b1435253e9984d8c1557486c9a5f1adb25bdbd53d623bbdc8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228448867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202ad2f8b52b952a388590db17d98d9ffc439cf977069c1fb68124e9f6051e63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:25:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:25:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:25:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:25:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:25:11 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:25:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:25:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:25:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:25:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:25:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa136f7c2dd026423e4b6e09ec4786cb85232106f928b3f1bfc10459f8af43`  
		Last Modified: Wed, 22 Apr 2026 02:25:53 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b647a91c528ff3c0cf5a4573afd500aa756b367b6a0f6418d41048af22f9c5b5`  
		Last Modified: Wed, 22 Apr 2026 02:25:53 GMT  
		Size: 85.4 MB (85383414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55cd4ac95b97b1a4615b95df128c7558fce85d195fce918a24fbf2259d9c2e`  
		Last Modified: Wed, 22 Apr 2026 02:25:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68491b9104e8f67761c524bc5af82aa255dc3d745287b93eab755aa4a8ece260`  
		Last Modified: Wed, 22 Apr 2026 02:25:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a70a01fe9e971fa43fb5b0157c1e05c72b2d94ad9c6722d1e970a968be13859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3dcb4f69af0d4f0a9b2307716ac644d858e17862bc4a6387c1fe9cf5942c57`

```dockerfile
```

-	Layers:
	-	`sha256:887f941b378da6ce5d361e461b7762ecd7f140d47a8d395349ceb71b136814af`  
		Last Modified: Wed, 22 Apr 2026 02:25:50 GMT  
		Size: 7.4 MB (7443252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:826d7d6a6a4581fff94e20b87fd0cfe1e263ad9d2a28bc9243e6cc48133d04a0`  
		Last Modified: Wed, 22 Apr 2026 02:25:49 GMT  
		Size: 15.9 KB (15865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:19809acab965cf88932deb40687e2f86da54779f64aebc7a253b5e2ba6c95650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241623565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afe13a4362078a7cf0d98f867d74559f3874f85779b6698e125b9af7f02d13e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:52:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:52:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:53:00 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:57:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:57:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:57:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfcead13693a6857ab51b621e372876765c71adf46e88c3448e530a15832886`  
		Last Modified: Fri, 10 Apr 2026 00:54:22 GMT  
		Size: 93.8 MB (93781469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22186d8ac29b0b2af7f835c8bb05c3caeed1a6b7e2cb5e1edcc000e6be99b8e`  
		Last Modified: Fri, 10 Apr 2026 00:58:05 GMT  
		Size: 94.7 MB (94722382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cc08ab0b0863771c35799cb1d43a29ba96c4144d1f7011fd03fe61546e2cf7`  
		Last Modified: Fri, 10 Apr 2026 00:58:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19986828ab8b1f3264659aeed9cd5d1d8a035591c55dffab66c7416e31b7bf1b`  
		Last Modified: Fri, 10 Apr 2026 00:58:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fff8b207416fa203c5f91bf0fe024f523989baadabcfca16145c0d8d352f9518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48aad4ff21a496225c2ce01e3e6d0a3c1bc5e48a117cffda75f7cd4278c2e16`

```dockerfile
```

-	Layers:
	-	`sha256:6f68bc143943f78be42d38539090a1f8364188b157f740bd9efb1643ddf96781`  
		Last Modified: Thu, 16 Apr 2026 03:17:59 GMT  
		Size: 7.4 MB (7424528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a483f0a4e88df7e803088e4cce1f91ca6717bcee1b42474ca393acc3b383eff`  
		Last Modified: Thu, 16 Apr 2026 03:17:58 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:8c5ef83225f0e612b4d0f8dd10281087d7135ec8fadd51f90e1b484aab48ce8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228432795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4da05e0f9e2301c291e3d504edb8f8299b1364208fc91a7d1a1660c7dac85f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:49:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:49:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 05:53:46 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 06:11:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 06:11:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 06:11:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 06:11:55 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 06:11:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90d8e4f2f94de58856173d1d55466c632c6602bdea8fc895ac0398eaddfdb2e`  
		Last Modified: Sun, 12 Apr 2026 18:55:02 GMT  
		Size: 93.0 MB (93008107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1379ffe5e5d471ba6a109f0ef466806f5dce61841a40fcd1dd6ea4cfb91003ba`  
		Last Modified: Sat, 18 Apr 2026 06:16:18 GMT  
		Size: 87.6 MB (87631019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f112429c33ee9d16b9533d4435a459e8733fb72edeb7c170130cfe3f03785c53`  
		Last Modified: Sat, 18 Apr 2026 06:16:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2667189cae87fda34f14d0796c54bf3ff30a75d20eb9d55c5b059a6c3f1c56c1`  
		Last Modified: Sat, 18 Apr 2026 06:16:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fb239f09ea6ca33cb8dc2ac7bdede657129cfa2442e910499d82fddde46d39c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee47311473e86ba803e41576e9e9ceb40cb346cc3ffd0b4fdd2feab16dea0a9`

```dockerfile
```

-	Layers:
	-	`sha256:cd07cf40ed3c4be434fdd169bb3742dbc631bc98767a16d1a1448a04826bfd23`  
		Last Modified: Sat, 18 Apr 2026 06:16:06 GMT  
		Size: 7.4 MB (7406721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d1be441bf3c0ef41c7354ace37e50def84767cb5912f3e9de46562f1c3fd0d`  
		Last Modified: Sat, 18 Apr 2026 06:16:04 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8751d9a65266fc354f029d9df9789263ffc437ad8841d2f7340cda6fc8099c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229624354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667aebb0f1196fad4a8fe1943914efb21aff62e7bc7c36e048f0d3193f3d8f41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:45:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:45:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:45:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:45:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:45:23 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:45:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:45:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccc9384a3516894cda80cf7c376f24672d63213432c362fcc78f0d0126929f8`  
		Last Modified: Thu, 09 Apr 2026 23:46:16 GMT  
		Size: 90.5 MB (90547699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7efddfb50bac93e7e6398a131df7c6a722ef89526e149dedd8dd4aa59af6f4e`  
		Last Modified: Thu, 09 Apr 2026 23:46:17 GMT  
		Size: 89.7 MB (89710509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed73bf9785d56cb42d8741f7d1f08071d9a552e54ac3078e1c825b8cce01a1e`  
		Last Modified: Thu, 09 Apr 2026 23:46:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195786e757d7b839159bf0e7cf64c9e873276967ffcdccba80431212915ea3c5`  
		Last Modified: Thu, 09 Apr 2026 23:46:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2007cc8eb169170e8bb6db55bc581bfa803ec834bf8d886f9ec09063ef24b3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc43df4efec94cd4b78d40a9c6fcfb44f3a35b5d7f9ebb583560ed3aeef17e`

```dockerfile
```

-	Layers:
	-	`sha256:5b1227ab20a2a0687fec6d0e1eb6d10fb8861d355d6ebccb6a83c7d227884e67`  
		Last Modified: Thu, 16 Apr 2026 00:47:44 GMT  
		Size: 7.4 MB (7417279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992f5ae2e075b5e38587320d3d375635b5595adcf1efe340c38d7af0a1b97c5d`  
		Last Modified: Thu, 16 Apr 2026 00:47:44 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json
