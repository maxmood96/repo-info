## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7bc47959df1f0841d44627f2be5d0f2d345bdfec79719c427a213dccfb993546
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0af417bad639271b9b28bb238e67b7c11db14b7f8b0661ba14a21a008c3c7277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215617952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af555f24ee66b030087a40848e034867b5028e0db2bd89c83a10c370ee3fcad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:58 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e156253af272d6f165b80dab642f63e5b2d556c6e8260f25dfb10bf35af001a`  
		Last Modified: Wed, 22 Apr 2026 02:21:35 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173610e0fecad7d3be64922798e72a0007b6dd3edf11d3cbe4fcba17da41ce2`  
		Last Modified: Wed, 22 Apr 2026 02:21:35 GMT  
		Size: 69.6 MB (69597434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4572283015de86ffae84fabfe1ba4e20a019c1475afe83e82ffa8c77c83f1f`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be975924f9d6a80b8b269bdcb1fd0ff380b4e07bf206170fe0e8db27ecdaab7`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1166c1bee2313a0eecdcf1ff195a244a54083bc889825f6d553a9f96e156e4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164fc24399d9f2f37de58d83f49d22f207fedfc325ce9d0d0698b5b802ff3141`

```dockerfile
```

-	Layers:
	-	`sha256:1030eb83052c50147c61797f338206662ecf91231214d424625ec4db62283b2c`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 7.4 MB (7375727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd862e3bc25029dc8f8f6bfba47595e18aeca30c0b58ac44b8e21d2dbcc25d6e`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd6df894ce912e59fd098a663d449a946082d3a5291afe47c92b67bf742aba39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213280776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471882ec6e0f4e3482673f8ec47e1373846731bcc72305b2eb0da03b4c80f692`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:24:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:24:02 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1115e2b759d53f1e56ad1f5c87567693d08ac1820d949e9a182c8ef78277148`  
		Last Modified: Wed, 22 Apr 2026 02:24:38 GMT  
		Size: 91.3 MB (91288290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730f6d2031d89e0bbe506388c8841a3ac8ad67de244d6ecfa157219d221da7cc`  
		Last Modified: Wed, 22 Apr 2026 02:24:38 GMT  
		Size: 69.7 MB (69738446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20528c41536003411324e260b870a971cb8127804ae9f2fb4a3a6885c57451f2`  
		Last Modified: Wed, 22 Apr 2026 02:24:34 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21841a79447c83d1577015ff68b69e18f6f55fee5d7ce869d04c2df4f0efe0c`  
		Last Modified: Wed, 22 Apr 2026 02:24:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b5ef23ba1c1ee4a9d6b6117f05bf849ac94c89327717e2f3fab52e73ef9995f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff6ff28a033f778a056156ef535a53c222295769e5fb41bacf92443b67a4d74`

```dockerfile
```

-	Layers:
	-	`sha256:1897848073d72682d68936d09be8ee4baf397b252992bc91c42626ef73e77022`  
		Last Modified: Wed, 22 Apr 2026 02:24:35 GMT  
		Size: 7.4 MB (7380847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e02cd8a0ea7736d6ec4934623e8fa45b00236428c23acc642442444b45c9ed7`  
		Last Modified: Wed, 22 Apr 2026 02:24:34 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
