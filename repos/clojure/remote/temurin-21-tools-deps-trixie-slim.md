## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:1665c105c10ba75704a18c80cab55b2097b430beeb7d7dff55172ef884972ed9
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
$ docker pull clojure@sha256:0960132edbc6aaa232a08b6223bed147d24b61aa383167ab24beb0e5c80c69ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259419647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86686df1f1591c19fc588cdf4627b4712ef25b03c8f3b5139295da46f4e808c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25afba0d4c3a296487c6aae63bb53b0a61006cab99523dbaeb9d21bd07efd8a9`  
		Last Modified: Wed, 13 Aug 2025 07:09:47 GMT  
		Size: 157.8 MB (157804777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d3b38a4f5c604cca7d7d10399c5b3a2243061d5d239f75f58061639415951`  
		Last Modified: Tue, 12 Aug 2025 21:37:45 GMT  
		Size: 71.8 MB (71840545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcacb66b6a4a24bfb09f51b1db2733390d5cf3f1459ce535bc8b9a0711e534f`  
		Last Modified: Tue, 12 Aug 2025 21:37:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f00e5af7edaa6a5b8e484c55ebe8104a5c856759973d53141560d961e04e2a`  
		Last Modified: Tue, 12 Aug 2025 21:37:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2312453e91e79325b99541c034f5fe8816e0da96ce42cdff10b563df7841c5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb7556e8ef4415ce94cf6c59ef6b6c225598b74a1a6e9648e0c0b0930cc9a9e`

```dockerfile
```

-	Layers:
	-	`sha256:3b5d942d7e733e304ac02633e9c14cf1e8693bef1d948da04f3f83fc8b2829bf`  
		Last Modified: Wed, 13 Aug 2025 00:39:26 GMT  
		Size: 5.3 MB (5258998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc38d7ca92ca491c9219b9164343480f2fd9b619f73b53c312e693ca92399a7f`  
		Last Modified: Wed, 13 Aug 2025 00:39:27 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc5c52e9409c7471b54d380ecd2364a7acd6ac01eb169f06ccfca956f919c489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257881756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9014c690efc30db9669c0cb62548b00c5308d0dd4ee720d2cea60359023041`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f7d6de78a1d66be999139f7c7f53d45593e354edd21dd0c3e2c38323862235`  
		Last Modified: Wed, 13 Aug 2025 17:26:23 GMT  
		Size: 156.1 MB (156081254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e1891fbf8bcc4d2c0e689322595c2f86782115badae2f595acccc00cf5a695`  
		Last Modified: Wed, 13 Aug 2025 14:40:17 GMT  
		Size: 71.7 MB (71663418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5c6d02396e37622f1d67681d4d5494987010c25d82e725028456f83e4e0ce`  
		Last Modified: Wed, 13 Aug 2025 14:39:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc88cd999ae1c0e87728adf508374565d0c49e34dc6a3307e0f044c19183500`  
		Last Modified: Wed, 13 Aug 2025 14:39:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16ebf8fff4dccdbdce4536acbaaee7ea9599ace54d4fb29793eac912e36e8c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8335f0dddf707326614074bf7066576bbf3579fd970a506223517a1a26cf820e`

```dockerfile
```

-	Layers:
	-	`sha256:cd594c5efe53ebdf210499becc678b7d5ef6b37e2d1702537228616e1908eeba`  
		Last Modified: Wed, 13 Aug 2025 15:39:57 GMT  
		Size: 5.3 MB (5264791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931cb63d43676e455a482fe345337f8d6fda1aa4288c4ba2f96ca6250f7c684f`  
		Last Modified: Wed, 13 Aug 2025 15:39:58 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:de2ac443284aa3a07422d60da3aa8156f112a73010ddd0592302e8e256498a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268804377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b848163881be6fe6edf9ed69ad2121ae619898bcca57aa613f5fe6e260c66f7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c919288f6e76487af9f70a09f762c3232e64134fcf527965fd7185a98ef5e101`  
		Last Modified: Wed, 13 Aug 2025 20:08:16 GMT  
		Size: 158.0 MB (157963474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe9f292a1d6cf78060c7258f3a7c2abea7eaca24ca42f5a642df8c73c7d2bf`  
		Last Modified: Wed, 13 Aug 2025 20:15:58 GMT  
		Size: 77.2 MB (77245652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efde59c477634f55711c48f54e34ed31c2960542e2888c081b62e839fb38f4c`  
		Last Modified: Wed, 13 Aug 2025 20:15:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652fc1a0506a4e89692de7352468b86cac6fdfe62504830400c9295a8ec0292e`  
		Last Modified: Wed, 13 Aug 2025 20:15:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0877321202f0b505eb43dc097beb857aac47d0b5f4b9d90aa041eb8aa0ccf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d6bdb5a654755e6df36abbfcc21fce1672b7c504e997222d405717332baeef`

```dockerfile
```

-	Layers:
	-	`sha256:2300929476fe6ed915f97f92255e28017775efddb333ddc6f50f07812802dd7b`  
		Last Modified: Wed, 13 Aug 2025 21:38:40 GMT  
		Size: 5.3 MB (5263381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2432e804dabd927a501775d1d1c2c86ed027b87690d47a68f3ca0dbd2d515e42`  
		Last Modified: Wed, 13 Aug 2025 21:38:42 GMT  
		Size: 16.6 KB (16603 bytes)  
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
$ docker pull clojure@sha256:22d429b858a7d6d22e9325076da0eb9e89569894c418b85a0ff48461dd592441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249665388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475744241f2a3516d79f40eadae3997db07c6739b0a2c76d4948a9381c7c62a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00a1a149145cfeea8f73610ae74a2f50032b6913ee48f0385a12830a9342790`  
		Last Modified: Wed, 13 Aug 2025 17:27:34 GMT  
		Size: 147.0 MB (147026944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d06698ebb54ca5aec988c391b56ca143949c9102dcee11defc08b31ef44c8`  
		Last Modified: Wed, 13 Aug 2025 17:27:42 GMT  
		Size: 72.8 MB (72804344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214e269339c8d1c202d5244631d2d952ab632bddd7af49002088d8f0ddf2094a`  
		Last Modified: Wed, 13 Aug 2025 07:25:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648e89dc20d3e6025726d305984ebf4ba6a5c999857e3b6a24eb7bdb628bb8ce`  
		Last Modified: Wed, 13 Aug 2025 07:25:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e89a6204650d3a9555d520536ce4b49b3e83b956e8916068fa99eff646931605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8435fa6bd4eaac702c5c62444d6ad7f5782ddde9ae73b84e3459b0762a59df`

```dockerfile
```

-	Layers:
	-	`sha256:83b1c461178b696ffc8ef82e54fe70d04876eb566fe0f8044ca6ddd0004575a5`  
		Last Modified: Wed, 13 Aug 2025 09:38:03 GMT  
		Size: 5.3 MB (5254922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e7ef27de80b9d8feb71adec843035779b97edc3637754b0290641f3196658e2`  
		Last Modified: Wed, 13 Aug 2025 09:38:04 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json
