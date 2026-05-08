## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:aa5367be21f5f97af2fe3b550014f2dd629ebeb4732b65628e74624d84e109c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54b83ab1c0d7bff4522d81613ab476641ff4e3e0a5ff5257993514fefb6757a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179616941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9073945ebb382d72ee76104f89e817d8a79286cb5389a2989aae187cff744b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2798e573252c7ddc8331f3ebfe4553695099baf57dc4d88dd4cd4918155942ad`  
		Last Modified: Fri, 08 May 2026 00:28:29 GMT  
		Size: 91.5 MB (91542278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c409f586bf1ceb5bef31040c3d81cf27cb2be3c80bdec82e63baee4baa78bf`  
		Last Modified: Fri, 08 May 2026 00:28:20 GMT  
		Size: 59.3 MB (59331106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c120021c95eeb24c6a90e7a7aedafd0b691b8f6036bc27eef6811e3595d4d`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29dadd62da7afe9120e72d35d4c095da2814505dae45f81d7c2a1bdf2b6909`  
		Last Modified: Fri, 08 May 2026 00:28:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2781fc0c960c5d2cd152c3fbd0bacd03640a458db6226fde5353ca1fd1b82d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59628d864da3e23c6dde9c59d96a9875917c0b7d19f6ded6bdcbee8427a7a7fb`

```dockerfile
```

-	Layers:
	-	`sha256:50e1d6cbbf672b60d68fff9c131898acd843b6f133b5433fd1922e6a13319f38`  
		Last Modified: Fri, 08 May 2026 00:28:16 GMT  
		Size: 5.3 MB (5294523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92df48e4f75d5656fd857b8b8c59628df11796fa2195ff1e539d8ba312ac41b9`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
