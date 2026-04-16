## `clojure:temurin-26-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:4e3ffd6b2bf72eae411e150231ced1b22fdebdbc97724bff78d667d15bd4c24d
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

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dde400372034db8c085732b8d8cafd0deafd2ac394fe3caa8b0ebc772a96a175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192393214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f93565c62705c6ba54a11e3c0c41f1b5696010fc67436c8873b2c8fc1c99f2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:07:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:07:56 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:08:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:08:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:08:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:08:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:08:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efe03c33c6a9343a3dec7778e25eae65f4aaafd2176d98dbf0c245ad2329bb1`  
		Last Modified: Wed, 15 Apr 2026 22:08:31 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d6daad7d668836fbe537bb9470fd68a99265d716e28239dc85e15d91e8cc91`  
		Last Modified: Wed, 15 Apr 2026 22:08:31 GMT  
		Size: 69.7 MB (69700144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511c12aa113a606c075cb195b570d6910f83e85ffaed8170628048244b427784`  
		Last Modified: Wed, 15 Apr 2026 22:08:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3377ff98e14a97dda318681dd4d04002eb801746e5fcbfaf8d07e6b380884948`  
		Last Modified: Wed, 15 Apr 2026 22:08:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1618dc0039d9930506717bbd4b153ad71f997e250f05ae30c653eeffc4a4c02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40b05f3316cd302bfcf8e4e964e2eab545d8fb000618f9b94bb504498aa2563`

```dockerfile
```

-	Layers:
	-	`sha256:f3731f0d94380e72e0dd9a99e766878ffcfdf82e1c41604365caa0db0cda12e7`  
		Last Modified: Wed, 15 Apr 2026 22:08:28 GMT  
		Size: 5.1 MB (5081671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fcc0b0b61dc8ef0840b55f6c18b8f9b80b956210cfc33f4693b3a35f85ad5f3`  
		Last Modified: Wed, 15 Apr 2026 22:08:27 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:411610dd0a22880e29bdc7d0388cd903d5488ad5d0dfacfd4ecb739342b75a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191203872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d51c0d68c6954be34cd8798b5f70d0696c8e5bae2e84958b340bc3f8c0c4a08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:19:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:19:42 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:19:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:19:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03945b4b75f8774f533c877801bb6d8bfb6bc2ba1b34592dc8da922193ef521b`  
		Last Modified: Wed, 15 Apr 2026 22:20:22 GMT  
		Size: 93.4 MB (93395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39874e975c175f0e4662f06ff43d437aa9c72645978285c3b944e2d3f93eed50`  
		Last Modified: Wed, 15 Apr 2026 22:20:21 GMT  
		Size: 69.7 MB (69691465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139eac42d073f8b8083ff5de8aa588268cad6828227458d0ace66c7f3744daa5`  
		Last Modified: Wed, 15 Apr 2026 22:20:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404b09500fdb85b54cbd0ffa5e498377498118ffc1218f0febed7d639420cb03`  
		Last Modified: Wed, 15 Apr 2026 22:20:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4f4f2d95ff7670e14cc05fb1ade7999f42ca559e2f887077b79e4f46aca184c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0219f8e3030ddc1680cef69915225c397e90966e8a91c98af8343bfa03acf84c`

```dockerfile
```

-	Layers:
	-	`sha256:7732cbdb201f0a61e0ad2a275f20f2d7c7f067dc57b737329ddeb2790462f73c`  
		Last Modified: Wed, 15 Apr 2026 22:20:17 GMT  
		Size: 5.1 MB (5087429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e26188073feecf601480ade002812881d2077aa0a35283ff0bdd5c15a14d28c`  
		Last Modified: Wed, 15 Apr 2026 22:20:16 GMT  
		Size: 15.9 KB (15946 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f3f372e69f6aef5a47e314eb9ad4bfcf48adf161b72ae8987730ca1706d6e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201390478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed3129635f61e1b4a711f1c564488ca874a206c4ee77fd683f5982da9ae015f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:50:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:50:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:50:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:50:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:50:35 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:55:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:55:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:55:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:55:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:55:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecfd0096cf42a4b346149c8884e2883a5327fa6421d13906fd62b73146a1a3f`  
		Last Modified: Fri, 10 Apr 2026 00:51:58 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c098c4db184bace32ba06a24bed28be67d7e12b28d66b1ec7fef1de7045421`  
		Last Modified: Fri, 10 Apr 2026 00:56:20 GMT  
		Size: 75.5 MB (75529491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4974969adc809192268022d639ce3fab8e8ca74fd93f457817f1db8450f6a2de`  
		Last Modified: Fri, 10 Apr 2026 00:56:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae64320daa98e7ec815dfcf1dc194ef59db00a8880216877fc06546ab6220f34`  
		Last Modified: Fri, 10 Apr 2026 00:56:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42bf1591f500adf887a3fd252af5223ce264c48555aaa622498eba1424fcbb2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1c973189743763f267f393d2667b70b1aae6f13ddd772f1c06f01ce0c919da`

```dockerfile
```

-	Layers:
	-	`sha256:fb9532782f4b51b4d5147233214c0c3d3694fd15fba48c7e2896a7cbf0abb5db`  
		Last Modified: Fri, 10 Apr 2026 00:56:18 GMT  
		Size: 5.1 MB (5070765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7bfa8d2e1758131e5b547f8b50c808dcf7e77d5ec6d8eb1d374bdbe98ac191`  
		Last Modified: Fri, 10 Apr 2026 00:56:17 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5507f9dd85eae9c68ef3bf5d1548da3cc79e7d2463017da6ee87147ef651a23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185953075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c1baf4063d98da925b1ef7a2098cc0bb699f4f8aeac833a0581cec287d30b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:45:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:45:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:45:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:45:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:45:01 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:45:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:45:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:45:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:45:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:45:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37956ed1201c9f27285d3d4f966a731d8f7ce39846b58d097d35d447fa5c8676`  
		Last Modified: Thu, 09 Apr 2026 23:45:45 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9054e3f19cae2c70ce0204a7dc36222b998fd342d1fa1bf09e9d3fe36d76d74`  
		Last Modified: Thu, 09 Apr 2026 23:45:45 GMT  
		Size: 68.5 MB (68512704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9992d20695ed7040c9bacf33d5263a75d59ef5948f370eb661cb6f4761a8b787`  
		Last Modified: Thu, 09 Apr 2026 23:45:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd2b60bf4532788d31a75717f1484b987e861e9477cf5ab5f48eb47e4389c7`  
		Last Modified: Thu, 09 Apr 2026 23:45:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:589794190e7fadbd3ee1792365a18dc55ba86e79f467469c034380b185ac801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea23e9aea69f692fccbf39caa3129eed67bdfb424467dce2e1beda103a5648d5`

```dockerfile
```

-	Layers:
	-	`sha256:e4b5b54e89345968072e8a8f421e4c9c2054a2bb7e8398b9e8f70794ce2ea109`  
		Last Modified: Thu, 09 Apr 2026 23:45:43 GMT  
		Size: 5.1 MB (5058178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d350ac9fb0703734bca005a6b5a5573050630bb0c5d0bbabed22acafbc4b5bce`  
		Last Modified: Thu, 09 Apr 2026 23:45:43 GMT  
		Size: 15.8 KB (15828 bytes)  
		MIME: application/vnd.in-toto+json
