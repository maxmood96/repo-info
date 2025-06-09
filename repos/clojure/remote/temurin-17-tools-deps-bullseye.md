## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b078c9bdeb57bfd419ed77152f6ca426a58cdab92c69429f520c280ff71df73d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:13062df35400ba148d4bbd890b3fdcf5fd77e39fdff58b2575762812cfe147f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267796090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7505a2d55d64037767157089a6e0f698480551d71299555c3159255a1b888184`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae348cac5dc9e7ea442c18f0f79f58dffb6108e8522802f50cababd4dbe6ff8`  
		Last Modified: Mon, 09 Jun 2025 18:42:58 GMT  
		Size: 144.6 MB (144635014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3852992b66908a51b44e32105ebdc2be989f142088ce9bf2d8da8d436b1c24`  
		Last Modified: Mon, 09 Jun 2025 17:18:37 GMT  
		Size: 69.4 MB (69409839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316a1700837c0e4edeb558010c5a3c2ceb79ef5d4b5085968b767d9640c97b9`  
		Last Modified: Mon, 09 Jun 2025 17:18:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf1df738a07eeb709934d7d9117bf936ae8549e8c41dcc4fcb172b04880647a`  
		Last Modified: Mon, 09 Jun 2025 17:18:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d4bdae4a22f0651a7690bf3069b8d525f654380351eb20e6dec2eb1e0cf353be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b637b80c54487aaf1b833a2b95b70aff87c0b77a1d20025ec507ae2da138dc80`

```dockerfile
```

-	Layers:
	-	`sha256:2640cc97a8dd1b0955047b373ae59564bee454cc3464e7bfe67cf988bc3b3a6b`  
		Last Modified: Mon, 09 Jun 2025 18:37:13 GMT  
		Size: 7.4 MB (7397262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02fec95096efdde5e0281d0100381fe61157aed186bdff0f65474cc0cd5c004`  
		Last Modified: Mon, 09 Jun 2025 18:37:14 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

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
