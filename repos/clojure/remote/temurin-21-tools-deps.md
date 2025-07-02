## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:22cf0558b380d00671789fa8d07f8458cb2b45863477eb1e01f49c1b36e8de6f
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

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:b5f2697044d8de70441699d8e4c76aefcb9c0d936ba30c967a96d8a7ebadf4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2ba90a4ca377a878c051aa0b981caa07f91145776ffa45bf132c144b687af3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83775a042eea68bab319387a3850ef5d25544f864bc0664fa3b84d1c996e522`  
		Last Modified: Wed, 02 Jul 2025 06:55:01 GMT  
		Size: 157.6 MB (157634471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4ea4c3f988e1cecc927edb0d136c9143bf2d99241507b8bc06952c2881ba76`  
		Last Modified: Wed, 02 Jul 2025 04:17:31 GMT  
		Size: 81.0 MB (80993174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d0823b0e04a15c8ec415c22a754f6b2f187d15c8d392109803e70789e2d49b`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6c5ef3e9ed08ac8c7fc7f04e86b18e4c6cab2cbbeb52c06487c084d6ef31f3`  
		Last Modified: Wed, 02 Jul 2025 04:17:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:89e0c486e5cfdd45ba6a1fca3e3ccd204ed65e8540820604dab2202b19ad1a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cfe92382b2da0d837f769ca395df4ffd16c8b97ba1ea2ff853af28c8a10905`

```dockerfile
```

-	Layers:
	-	`sha256:cb2098c5fbeecc8ac24acd6c429a7f5ea2350a87c7f233784d35877b95e08789`  
		Last Modified: Wed, 02 Jul 2025 06:39:15 GMT  
		Size: 7.4 MB (7373370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c0482506dab8508bc29b8c67d78359a566ca49186359fae4304cd1f4b578bb`  
		Last Modified: Wed, 02 Jul 2025 06:39:16 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83853f26627532f172e346a27023953bfd14000b26a8a59b48548898ac577209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285120840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb9e7a5270a4f259b0d6def75c1ee05569b56f783f18b8f5d163ca70ce31794`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa83dba5e1541c4539ff137e170a211a425262a5378eff87759883e8336cf89e`  
		Last Modified: Tue, 01 Jul 2025 13:11:25 GMT  
		Size: 155.9 MB (155928824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8313e7755ef31f349ec9866721ed6892c5792034038655cbf1c8c986e978b84`  
		Last Modified: Tue, 01 Jul 2025 12:33:10 GMT  
		Size: 80.9 MB (80852192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c085b7a9ddcf68c4e5e216a7fc0c2f97572074628bbfc866fca27908e0ac21`  
		Last Modified: Tue, 01 Jul 2025 12:32:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2239d53d20fcfe216fb05ddc9e1f08005b16bfb39d83eab30727f632a8230`  
		Last Modified: Tue, 01 Jul 2025 12:32:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:ab0254c3a00e193716d6156dfdfb07cb94d18dfe885a6ad4a0bcb1ac124f657a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089a70e1d45c64046d7e697462d578b8e5ba3119672fef9aad33e63375b6fff3`

```dockerfile
```

-	Layers:
	-	`sha256:6c2f566983367da093fa9931087eebbf0d87ece164b60e6f24ad094b044f9ea4`  
		Last Modified: Tue, 01 Jul 2025 15:38:19 GMT  
		Size: 7.4 MB (7379205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28374dd5afd19da6585b234ad7fe766e2371e77e5d2e1a5774483012f1cfeb8`  
		Last Modified: Tue, 01 Jul 2025 15:38:19 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:385da27bf44357d59831bb26077d6afca23ed47c6c0eca452f950424ecaaea63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296962910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568cc11932336b7862bae35ab5ed0c890d8a693d4adc5fd593b373a7685a37d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb00989eb2ecd00cd9ea5051b21c8185732aa39815a0ceb06473d7cf6668084`  
		Last Modified: Tue, 01 Jul 2025 13:20:52 GMT  
		Size: 157.8 MB (157804868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfdd9675151df8f7201d1511a9351309b60faa1e8d916291ed0d5f2979d816e`  
		Last Modified: Tue, 01 Jul 2025 09:03:07 GMT  
		Size: 86.8 MB (86819756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffe58fbb068e44d14db9cd0dc093e8a4749a4938a52b99c1449784c7ef7122d`  
		Last Modified: Tue, 01 Jul 2025 09:02:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767c04bc56a76b4736b5a742d1274ec1881e0d7448df9f4aee39116cb1eb10e`  
		Last Modified: Tue, 01 Jul 2025 09:02:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:7439b919a0ff322981a10d9b2a598d2fc61a777cfe1f8fbda2691ea77097894f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d5aad83a691f1691192feff664ba9abb948ac63606b7234c84b79a7a986dda`

```dockerfile
```

-	Layers:
	-	`sha256:e855903064515039d57bf08e1e29c2b0942035bcece434373c3a51d3d862dc68`  
		Last Modified: Tue, 01 Jul 2025 09:39:46 GMT  
		Size: 7.4 MB (7378610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a81e9ff65f83b4e72dd49e8428a651b47c924e2e1f1757860ce5843530ca320`  
		Last Modified: Tue, 01 Jul 2025 09:39:47 GMT  
		Size: 17.9 KB (17904 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:ac7b21d6bf98b2c1176df4d580471384b793211b97f61bb3e36def21dbda84f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273860830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4001819ce194a5a9cefc1b670af996aadfac3e79cffabd8a7f263981e1efaa86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56a47b9ba84bc64ca6ce5c5309a2eafe1d1c6565b113770245512f1bfe041ca`  
		Last Modified: Tue, 01 Jul 2025 13:21:45 GMT  
		Size: 146.9 MB (146910995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6d6537d8c279e3b7ae26098509441b14ac81762abac0e0503a92e2b2aa9d9e`  
		Last Modified: Tue, 01 Jul 2025 13:22:03 GMT  
		Size: 79.8 MB (79799510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d16c54e4566435b1980b702be5e1808fab2a3d3cc30edddb1a9541bb135ce22`  
		Last Modified: Tue, 01 Jul 2025 08:22:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a96bd86d929de3365d8c19b5e664f8e7ced4813ba3dc27e1146035ee32ccaaa`  
		Last Modified: Tue, 01 Jul 2025 08:22:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:7c9e93451a421856751c751632b116e265b1fb78292e4897c19786e2ade3d885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fe4a8b63ab1bc800ec28a340e64aef2e88bd9ddbbb9a9fa2b1a006e051671d`

```dockerfile
```

-	Layers:
	-	`sha256:ab62f1caaf0333351e65fcbf569bc91ba777aeda98b27754bc2f14a832ba3c88`  
		Last Modified: Tue, 01 Jul 2025 09:39:51 GMT  
		Size: 7.4 MB (7364689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ffadbffa1551def48af560466e59cd4cae9c6f5ad8b284c196ef833a9aeb2e`  
		Last Modified: Tue, 01 Jul 2025 09:39:52 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
