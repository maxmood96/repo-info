## `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:a8db37049ff3a3b5053f37ed148634455dfb47d85eb037dc74cde514392d63dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cd97628d213da25a4a8c05bda1219cc3d90091b51171c054996d7bcfc39bfe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267800604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef63b222985d6a0832209b79e68432fdd210fa2049122f8d67c217bc1ec48b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a787045579a90d82732299d78800255641ef4d4459660abb0aef1d5415849a93`  
		Last Modified: Tue, 10 Jun 2025 23:51:44 GMT  
		Size: 144.6 MB (144635013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca8446196f525363f8e83fac87fcb0fbf385eb737a001cd161873e99075b34`  
		Last Modified: Tue, 10 Jun 2025 23:52:09 GMT  
		Size: 69.4 MB (69409768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78be95b0cc5d68f121de24eae4dd358cf512bf5413a9c822eae8cbb4d88b353`  
		Last Modified: Tue, 10 Jun 2025 23:52:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73b2f2bca86d171864bcfa4d423b5713240e19cdbf6a0d7e1f1844fb0d1cd55`  
		Last Modified: Tue, 10 Jun 2025 23:52:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c18de6c9a3bfd92d659729619a558a3c2fd74b292c9e4c1f92dcdc31fd92a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a4329a057298b7bf0cc3186c60d06c124135ed600bd576135792f7f2749a3c`

```dockerfile
```

-	Layers:
	-	`sha256:0e54d4d0f0c131ecde2e0c468a7a05ed1352b726a0358d9789dc604f0356c32f`  
		Last Modified: Wed, 11 Jun 2025 03:36:44 GMT  
		Size: 7.4 MB (7395638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38b547fbe88f2eed1f845564d92f09ac8738d4f581774bd3638da51c9e875827`  
		Last Modified: Wed, 11 Jun 2025 03:36:45 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e25116f5c96dec5df807f30ef2f4c976c3f2d9299c06338c3b80d3732e646ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265299180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17373f385b3f819691db5a179a8f846a9285f11483f5c24b88ec4d4862e03cc5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade6077201c8ba74fe01e7c07b8390be588631d5529c12c56af96a10c977df0e`  
		Last Modified: Tue, 03 Jun 2025 18:40:36 GMT  
		Size: 143.5 MB (143512642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1959a0dcf772ad206f6fa6de31b42b04525694c999ae60e65fb5a1b87583590c`  
		Last Modified: Mon, 09 Jun 2025 17:47:24 GMT  
		Size: 69.5 MB (69537744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3737ca510814d3d9bf4902ea773f2734c2c32b0bce37d7baede2ba12957ebe5b`  
		Last Modified: Mon, 09 Jun 2025 17:46:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470949b4467330cf125ba5fee725113d2631f32b1c90fb8caef9894b274cd12a`  
		Last Modified: Mon, 09 Jun 2025 17:46:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4f96723aa450b72fec2961750aa50795b767bd2adcf50d4d13884fb4c01d332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7418300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2902c7589708d8985125cf696c2330e8c2cd7899c1cf629b969f4535e3993b81`

```dockerfile
```

-	Layers:
	-	`sha256:484a7a7e38c21cf4ff59b12c1a3f36f2f0331f420736140a098676b3dd48eb66`  
		Last Modified: Mon, 09 Jun 2025 18:37:19 GMT  
		Size: 7.4 MB (7402361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9068c2db74d5a82668d3f7611d77f237c809c300c5c56574ca7528ca312b321a`  
		Last Modified: Mon, 09 Jun 2025 18:37:20 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
