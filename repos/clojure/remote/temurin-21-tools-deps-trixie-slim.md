## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:c3495300cbf30ce4cccce1b2440d7bead14cf8ad10b7690ecad1d2604a0b2946
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
$ docker pull clojure@sha256:b3a6963fe3db0a764120a86f3e1414a0c91f04f658f35b75c5f8cac34e9abc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259959758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07dbf3b7df9843fb51fd96ee483ead4abe14f780f16bcc441795488324ff880`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:18:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:31 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:31 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:18:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:18:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f22c0f9a85817ffc752cf8c9a31b59afec684f053541207f49ed82e2af3214`  
		Last Modified: Fri, 08 May 2026 20:19:12 GMT  
		Size: 158.2 MB (158166936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc8af18291eee122069892d18bf3d0c310747dc0703ece0676d84a912b54639`  
		Last Modified: Fri, 08 May 2026 20:19:11 GMT  
		Size: 72.0 MB (72011556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc49630deef7515bc082813e8dbb7a8dbbe50b8760875e06f32ef206515eb0a`  
		Last Modified: Fri, 08 May 2026 20:19:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad0229e3d5f80cf894f61889ffe19d0d805ed8be6eda789451b5765a135004c`  
		Last Modified: Fri, 08 May 2026 20:19:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d26d0020a291b29a74d98cb892606a4a90a2c143e0944451077083be0015764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a98a6972e6140705cdc5871447948f5786ddd17fe28c0cfc68beeed0b7679c5c`

```dockerfile
```

-	Layers:
	-	`sha256:448858044eaf5415d6912678c2ec6601e1559cc5fc7242da5ca5131607b9314c`  
		Last Modified: Fri, 08 May 2026 20:19:07 GMT  
		Size: 5.3 MB (5261671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687cdc8c21934c9db296109f4588bc7006edec6dbd7a8d82023323daa38f52d6`  
		Last Modified: Fri, 08 May 2026 20:19:07 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a1020ba0c0c84499c5c637e3c1db8962ce4f0b12a126553a947fc272c05ec658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258437617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b2425f0bc518c4e088493ad42cc25aa5d12870f6a693f22de03c1b77c12447`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:22:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:23:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:23:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2791b5613b3e06ddfe0fe7e1045d076f75381574c0b9e03accb8850eb386cf3b`  
		Last Modified: Fri, 08 May 2026 20:23:38 GMT  
		Size: 156.5 MB (156461132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861efeb213ee72198c15f32bcd6252666690b4def5b91306c82882e609e7e821`  
		Last Modified: Fri, 08 May 2026 20:23:36 GMT  
		Size: 71.8 MB (71831802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7008d2b282bc3e367bc87cf3b524247a1ec8c305cb0c5a05ffe18e4e33233b99`  
		Last Modified: Fri, 08 May 2026 20:23:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51754e3c4760d46b20b87dc3b00cad21f788c829a2b2480a50d2b08fe8a5bfba`  
		Last Modified: Fri, 08 May 2026 20:23:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:414557a8ef7534f6032c32e3a750e7526ed73de007bc222ec46c43be56a2940d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa96dc08d3e0573ef11443a2952c24073f1d66fb71372d5a51715c19c2e88cb`

```dockerfile
```

-	Layers:
	-	`sha256:d065d509e059b9bf37337b45b42b2308117c7594e28cd275400711cb6e5cb9b2`  
		Last Modified: Fri, 08 May 2026 20:23:34 GMT  
		Size: 5.3 MB (5267440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f9a8445d3b2e38f21fc85c214585d8b222af224e491dff1110b8bad75b63e7`  
		Last Modified: Fri, 08 May 2026 20:23:33 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ad569ca1a4a8164b18f94c58792ba65056f5d5cd3133a0e94db1a073a1aa8cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269370757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5236e5f834e916151bed93c749b68d5dabb9c8c6bd7190a10be8a24de337ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:38:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:38:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:43:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:43:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:43:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:43:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:43:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bdccfa02f117dfdaab6da4f7459875679357ae8fcbf2cafce50f771adcbf9`  
		Last Modified: Fri, 08 May 2026 01:40:03 GMT  
		Size: 158.3 MB (158343276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72a100c5b508f4ab7a4d7c55049ea73eba39e81620ab5e1c1c64825fb2b78f0`  
		Last Modified: Fri, 08 May 2026 01:43:50 GMT  
		Size: 77.4 MB (77428407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cad1daeb3f63f143955f66db15d904595e502c6a98eb4b66962da785e795ba`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0110f3269e641a29d815ab6522158ba27837b3152fe54c068ff06cb11a4c8b8f`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:667b614e3e69dba2ecd973eeab0f93a36b420eb96c08d6f3a3fe9a062adde695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e7b8a463eb6583d6648784a579967cab4a90d49ea7ed5b3dcb3ebfe457008a`

```dockerfile
```

-	Layers:
	-	`sha256:2334dba447e7b3106f18afe6ff3bebb907e662f3ca48ad9ebcc73a701b749440`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 5.3 MB (5266042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ded831f7a9014f3e75a3dc0c9f51bdc4d56472de24de937e2633fade14c4a82`  
		Last Modified: Fri, 08 May 2026 01:43:48 GMT  
		Size: 16.0 KB (16014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e6d432b91d36cd2b88b5455fdafcac9c13289bcd95f8b9356be3cff46d87f204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256399009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fe55935cdf2e86fbad57699882820ef392e62a4126707262cf382ea01d70f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:16:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:16:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 18:16:49 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:33:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 18:33:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 18:33:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:33:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:33:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad178a1c7448a34e9758387fe35c9fb467bae057770eff7c342592f312ccf326`  
		Last Modified: Fri, 24 Apr 2026 18:22:57 GMT  
		Size: 157.2 MB (157216929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4485bc2d2d4e9d9b14618767c526aaad37b1c9472f8b95e2e7b23960e4058890`  
		Last Modified: Fri, 24 Apr 2026 18:37:35 GMT  
		Size: 70.9 MB (70900843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae62c404a6f55650f01f12b354e9822d5b9493c881275d1223b63eb371682c18`  
		Last Modified: Fri, 24 Apr 2026 18:37:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8432fbb1b29e2115e227edab6b25238e1ce682fcfe4fee77ca3adce673515de`  
		Last Modified: Fri, 24 Apr 2026 18:37:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:262c1c3d07d5e8026102a41c1d4ae8a94db44996d7c0bc8d1df78774b8f384d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbf695ddc49d9cd3757d3374b562cfe76b8b2ab6a9abedc7e116eb1c8b6ac59`

```dockerfile
```

-	Layers:
	-	`sha256:7375f39b227c4d8068a20126d3c4d39b4c8be91acc66e87dd9be88778a52485d`  
		Last Modified: Fri, 24 Apr 2026 18:37:25 GMT  
		Size: 5.3 MB (5250508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531bf999926f50cf962a1cead605783cc6fa62497d88966af945f38372572747`  
		Last Modified: Fri, 24 Apr 2026 18:37:23 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c3db98616394cb5a01b326c31dd1a3f11f5e7eea80854fa9a36c965a37e71a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250216973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db256d5132303cc9423cf3145e66b9dc3f85567b614899f50bf5946263ef058b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:17:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:17:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:17:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:17:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:19:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:19:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:19:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:19:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:19:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322bcf3d705f2cea437ef1917f9da7ff28c4e9884b7d8a103b1f9bdb9098e5dd`  
		Last Modified: Fri, 08 May 2026 22:18:28 GMT  
		Size: 147.4 MB (147388345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34219297b07850189c7565bac7918b2c04ddaf43c627c482cad31e08d184f66`  
		Last Modified: Fri, 08 May 2026 22:19:26 GMT  
		Size: 73.0 MB (72987238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81350e99bd276a5f38af94e2fbdaa7e1046a4bb426b2d3f43d7a92754159258b`  
		Last Modified: Fri, 08 May 2026 22:19:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b2fef850ce0402e157d1de2b92193b6732a106c8dcb497a37d4ca183f6a365`  
		Last Modified: Fri, 08 May 2026 22:19:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65ff652d9394be5eaec05ce358a948d75ab7fb19ac82a25b733375dd0ec4ea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de672dfa816215e1f8134de7f162f8f5b05fa53e52f5b4b4edfb881f2844913c`

```dockerfile
```

-	Layers:
	-	`sha256:5bfa760d8d78a152e8d70a0a5c16cfa8476ce7eba462b640a8a3a4797d9dd753`  
		Last Modified: Fri, 08 May 2026 22:19:25 GMT  
		Size: 5.3 MB (5257595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b05071227b51cf278df5bf865331eca4213c3493c4374f920b002c600a8df0c`  
		Last Modified: Fri, 08 May 2026 22:19:25 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
