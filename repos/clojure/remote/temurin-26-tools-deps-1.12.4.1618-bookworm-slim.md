## `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:218f0f609aa02d99448d64476672a1ec970aca1702fc2f373b4f813d94a37c43
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8263088de0e96c98c7bc2235d2c4bf0aa928082ae410f05bfc710a2d2d18200c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192392147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb123a9ba46c53c3e018c4b36aa5644f998a45b9c42c3e4d31da69ccf9f3b367`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:37:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:06 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04bb8a65b39d43f067afd694c906a3542720a7f89dc736210b081196c55d634`  
		Last Modified: Thu, 09 Apr 2026 23:37:43 GMT  
		Size: 94.5 MB (94455698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd053d2106e59b601d766938fbed04b40f39331800fceecc272c014f6df294ec`  
		Last Modified: Thu, 09 Apr 2026 23:37:42 GMT  
		Size: 69.7 MB (69699074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99af84177410b5a3977677d522fc769a1bd212d83a0a3512660e10bf8c3b5184`  
		Last Modified: Thu, 09 Apr 2026 23:37:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced9e4aef29f5e0dc1ef89776eff1e2e41cb31d4025bf4f89c2276feb1eeab75`  
		Last Modified: Thu, 09 Apr 2026 23:37:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee08a32334303c1269b88d00a09266bef6fd1e329176f01962670dd8c8b148d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e4f8f035bd5abd2667e33d97f3b4e95fd22a53a98e47f20a4e956581f20200`

```dockerfile
```

-	Layers:
	-	`sha256:203dabfd1cec39bd5b9b9a2b16dd68fd38f9dc5f78ee1da86bb6809c9f9a1e21`  
		Last Modified: Thu, 09 Apr 2026 23:37:40 GMT  
		Size: 5.1 MB (5081671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc46e166ced13d5e73e4157d4c5282e77f82d1eaa1b2bdae117258fdfa13e837`  
		Last Modified: Thu, 09 Apr 2026 23:37:39 GMT  
		Size: 15.8 KB (15828 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:287e0d8c6f29a5025472d558d775f7f5282b271e83e66770eaec3e324d53ff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191204940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80581affd78c3f3c29369be34177b63784e650282f2be53c9b26f1b4eca9a336`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:36:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:00 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f9ef63687cdd1afbb2cb3db99b44a750832b949f7f5ae115b6905380c3e240`  
		Last Modified: Thu, 09 Apr 2026 23:37:34 GMT  
		Size: 93.4 MB (93395164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683e5304a524cdf5acaeff7d513e2e5830c6ac6a1b4c71206189bed8ec763abb`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 69.7 MB (69692569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634825fda8f6645923a9c4b2761baeed0ecaecaed4434775d57268584078d728`  
		Last Modified: Thu, 09 Apr 2026 23:37:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a07c11c93773af4242d7b701d6294a8920eff78c97bdeeb85dd6b5b9ce051e`  
		Last Modified: Thu, 09 Apr 2026 23:37:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:106bd31260102674decfbbbf5f3c1d18acb9e60e7fe3c7df7a0cf0dc043c6b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d60bd58c08b9e750696d42dad18213b0faf57891f83c56fe8e356a72a028e7`

```dockerfile
```

-	Layers:
	-	`sha256:cbcf0fb024fa7a0fa842514576bbd215f8ff370fc22efc20dfe863884ed91114`  
		Last Modified: Thu, 09 Apr 2026 23:37:31 GMT  
		Size: 5.1 MB (5087429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156824fce86cc33ca915aec836d5d210a122828bc00b7453d9d0ca46fc447eb9`  
		Last Modified: Thu, 09 Apr 2026 23:37:31 GMT  
		Size: 15.9 KB (15945 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

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
