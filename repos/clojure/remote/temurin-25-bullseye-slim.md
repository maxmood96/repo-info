## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:ddaa92d07f8dad41c08be79fc3db8f86dc81586c0b8a03dd353e708c5bc252b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0bf879cdf5376eace4002a52c575c029091415ec36d147fc231610df17f1af06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182019816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7450f8758218f8993b7972f42292c10be12b762e43911e95b99f2ed66861918c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:35 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac83709ef30b76f32ed2a79173d6a0dab104907f0fc52e75521ae87d7246962c`  
		Last Modified: Thu, 30 Apr 2026 23:54:06 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368016a2f3fcf63ab1d97ad82e7997212fd68a001e1f6d9e0b6b509eca6c171`  
		Last Modified: Thu, 30 Apr 2026 23:54:05 GMT  
		Size: 59.2 MB (59186244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99e3c2f0300e33fdc016422bc5433f1741148b035395c95ff14786a7ddd5249`  
		Last Modified: Thu, 30 Apr 2026 23:54:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12315491fcc36108c9a87601cf7495d7f62284adb00f6e1f7817887af8ef7fd9`  
		Last Modified: Thu, 30 Apr 2026 23:54:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a16a2120b5319d5b7d2ba217627a00f8848df87242e9f2b3d44b7ef15c60ab23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6996339dee6aaeba7dba6cc4e9aae9bb01d0f1926727892ba1a0d9fc8f4bf260`

```dockerfile
```

-	Layers:
	-	`sha256:ebd69ea6a82287ae02adda5b33cb8fb60c2f5d4fc8c5132dec10afc5ad9431ea`  
		Last Modified: Thu, 30 Apr 2026 23:54:03 GMT  
		Size: 5.3 MB (5288770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760de629292b736508dfcdb6335af7410e7a475c139052562c492df7a39945ca`  
		Last Modified: Thu, 30 Apr 2026 23:54:03 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a10a67c905fca1abb43fb302c61ecbd5e481343842c6cf8970af30856aaf8964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179616963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96576eafbe10b0c642fc6b2ebb0f036ca133187feecc4de4cca8885c03ba15ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:17 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed86f7ffd3024afdfe890900ac855fe5e5906456edf024d532581ec2755e0c8`  
		Last Modified: Thu, 30 Apr 2026 23:53:52 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cf4c3b6957bbe7cc4b52780751ffa8af870794f23bdbc3462448959087b688`  
		Last Modified: Thu, 30 Apr 2026 23:53:52 GMT  
		Size: 59.3 MB (59331124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b1d23567e1933ed717caed7b14b7f7bf19494aa56f8d4d11b317587e31ca9c`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c35037667e51d379704363ee7bb257631f48a3e592cc47dba29cf7b91ec55a`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4a63fe1c4405f2af9125c1de8c4846a9d3aa49a8df8d75a4e1b91884193b4d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a989d9f76cc4e28ef5f37228ef39229e2b49b999c49b315da5b738c5844639ea`

```dockerfile
```

-	Layers:
	-	`sha256:e0a02d87cfc222c32c3b97d5a10c1d33ac7735b557c9b091b18dcb720f86de72`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 5.3 MB (5294523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8a500a86de48c5268c52212e4f73d80aae7d6eb251251c5625457a732dbb1c`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
