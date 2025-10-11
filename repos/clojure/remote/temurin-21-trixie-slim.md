## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:7aee437356a95ec132519c3ed254f860c5d41ad176f634ba956a6caa014aee69
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:08ba3cc08039deafdd8c9143e26732e6c70f0703220f8b9e2555713cbcef1481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262522135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c404a99ef75cb8548de461c6d3c05c7ff1558d34c4622500a17b650b7deba03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015105d4ad08a527c7abe2fc6fe7ce367397bc86c2a8f87d60d727021fb38c5`  
		Last Modified: Fri, 10 Oct 2025 07:10:45 GMT  
		Size: 157.8 MB (157804775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d7d9f272c867c88080beff3a2ef0ffa8f508d283f8bb0c2768b4b960ff9b2`  
		Last Modified: Fri, 10 Oct 2025 03:51:49 GMT  
		Size: 74.9 MB (74938550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90335e97dafe215bf6e53bdca80982f3ffc050ecb14212b6b486019a1bf6e8a`  
		Last Modified: Thu, 09 Oct 2025 23:13:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096c6ea94ec45400fcda446a55edcb46db610a9cd7a387f6ab2af17569507122`  
		Last Modified: Thu, 09 Oct 2025 23:13:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c35fe518b14f1550069ccef1ad49caeb44534d941f1d13ea5ea05e3159acece5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6c8203b1b4651969e01d539ef42e4590a3b8b98d333b464129da415aaecb77`

```dockerfile
```

-	Layers:
	-	`sha256:ea94878a60e301d62aeecbef9043d8e9556cbfb480fec990e7a87a142bfc4185`  
		Last Modified: Fri, 10 Oct 2025 06:46:29 GMT  
		Size: 5.3 MB (5259269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3615a2381a0bb814d49b9bfeeb44763d3f15a50c44a76d0974da61e4258d5a8c`  
		Last Modified: Fri, 10 Oct 2025 06:46:30 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f8d715a37fc01d4d77500bbfff8da4d5b2825366bccf0159d60d4260bc9552fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261347824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3a0262e8d993c083262ce921493114b7cc576dbc2bd8266e6b038c7bc6635e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2495783543904f16bc3cd50dd5a15ef9bb79e3d287f27f121a68a3d65cc6d4c6`  
		Last Modified: Sat, 11 Oct 2025 02:48:46 GMT  
		Size: 156.1 MB (156081276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fe47692ff5649b27fef4f807b1d55de2573b9eb734bb2e02ef417acca7331`  
		Last Modified: Thu, 09 Oct 2025 22:30:27 GMT  
		Size: 75.1 MB (75124665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffac30baa67766543e272b44ff1b7e6d737835cd293e34a9edcb063e070a022`  
		Last Modified: Thu, 09 Oct 2025 22:30:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ea952fd3faa221995cd8ccefc2c4c2154d07aea74be4a7e3677a3e6515363`  
		Last Modified: Thu, 09 Oct 2025 22:30:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3d0ad8fafbbb0fb5691b2ace6689a6abd6b5c5b093cb89cf67d384f8ab736f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421f6fc4a4de4c34d17292a195658eff7f7ef0729059c0a327f1a4e97eed35a`

```dockerfile
```

-	Layers:
	-	`sha256:ecf9fdda54604a6dddda36c70a88e43ea73f58fcdf6b2d8f64ebb82533f640e4`  
		Last Modified: Fri, 10 Oct 2025 06:46:35 GMT  
		Size: 5.3 MB (5265038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e288fdf8cbe9feb4ec5cd51ed6305539323653257dd3eccf9f1fb48a83c8c91`  
		Last Modified: Fri, 10 Oct 2025 06:46:35 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0f1c18464a1cacfecd5c3214434d79ceb6c48594982509b539efd5e56f8c59d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272151125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d1e4c8b7830a6b561b682ae0f5c495fdd7c19faba95eb1c20482ac98db7963`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421baac9c672c32a7746c4e3eb8dcb8fbecb71202333b33061c0d216d401539c`  
		Last Modified: Fri, 10 Oct 2025 21:17:06 GMT  
		Size: 158.0 MB (157963476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a6e0d25f089da954bc96594bd837f3a45fcdf22ce2ae129203298c96d3666d`  
		Last Modified: Fri, 10 Oct 2025 05:50:14 GMT  
		Size: 80.6 MB (80588155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3d266e56dfb8034580834235a20704b23c01b4c406c2030b003ed05c883706`  
		Last Modified: Fri, 10 Oct 2025 05:50:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede6d53911e9c93f4e2929b4cfb580aadfa954e2d1283311a04157335a80d5f9`  
		Last Modified: Fri, 10 Oct 2025 05:50:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e6f6530f27e50f01c806f7c2b01e71cd1d0621fef48422b3f9e3c411f84fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ec90914a6b925df2e08c3c34ca584d10035fa8d47ecef85605712331dbd4f2`

```dockerfile
```

-	Layers:
	-	`sha256:7495deaf76ae69bf074770335baf81a39a77a84773afc09f7c1490ee434e7d3b`  
		Last Modified: Fri, 10 Oct 2025 06:46:40 GMT  
		Size: 5.3 MB (5263640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e1a7d2ceeed2f9993969214c99aaffe66e0679f36516f0df23bb3ec22c92eb`  
		Last Modified: Fri, 10 Oct 2025 06:46:40 GMT  
		Size: 15.9 KB (15902 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:ab68810c3a4189df23e5332233c85aca6ac8e109fadd974b65c3d7d121fd4abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255358389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f744b865b5a1a76c0189c3800b2b57f6dcfe45d646acb18fa0e0567fd533fc82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea379b0ffd23e01d5269daed7e5472c408f4f24f97c5dfbc8867e5b4a5eb3893`  
		Last Modified: Sat, 04 Oct 2025 20:49:03 GMT  
		Size: 153.6 MB (153593448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3abb0efffc317c91fff74521aa1ddfc2852431d25a825f1f34dee58f5a88d7`  
		Last Modified: Sat, 04 Oct 2025 14:57:21 GMT  
		Size: 73.5 MB (73488398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ce7da93691e4001e71a39331fc0debc216f5f13c3f5022ae3dc51f6ba157ba`  
		Last Modified: Sat, 04 Oct 2025 14:57:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308156d6a3d9d03dc8f9ebc1758c87e7ab8032595c4f5f398a1a07916a68b431`  
		Last Modified: Sat, 04 Oct 2025 14:57:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4ebca5d4b43e3366523b8d8af4fbe3a1389ab0e6f99c3ea8ef7f4afa901375b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9074d0e31cfc82e33e05d0db83dc3d60bd7dfc1d6839b632d5adc84e16cc8`

```dockerfile
```

-	Layers:
	-	`sha256:495ce9069351cd376f04619c10e97f09657ecbe175178158e7cced8f04fb11ce`  
		Last Modified: Sat, 04 Oct 2025 15:37:46 GMT  
		Size: 5.2 MB (5248733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3205bffcc2884523e1bb6e9fa35732a92e480fd2953f760cb0a5b20713d17376`  
		Last Modified: Sat, 04 Oct 2025 15:37:47 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a8ba3da828bc578fadc491a9426ff10bfdb61dcbd7e2642b917ffeff67d9edd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252428571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29fbd15fd8e77afa3b3176e4ce0defc8b92f7a9a8dadc360b50556c9a61ddb0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947739c3bc23762acb7e455b7196ef53ee1ddaed39284ba51e403c0193a3557`  
		Last Modified: Thu, 09 Oct 2025 23:29:47 GMT  
		Size: 147.0 MB (147026921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35884d8b664f48739ace031c70f76d26da35dbc66f74db0a56e95f3731020970`  
		Last Modified: Thu, 09 Oct 2025 23:36:11 GMT  
		Size: 75.6 MB (75563376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef7fc0d72ae8c0c589386107c2329e275d181b503363989340a6d5a2459786c`  
		Last Modified: Thu, 09 Oct 2025 23:36:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4416e6d9ad05c3cd04dd1dbd55cb58e2d54d81a13e20f5ab44956a9e1da0c747`  
		Last Modified: Thu, 09 Oct 2025 23:36:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:103638916112bf2390b68eeed3b2cfb94f094bea593a22eda1472199eba7d38c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db2e8f6b307de9faad45ed1b8f985d4f8ed621623e6c964b161924b4f0b678d`

```dockerfile
```

-	Layers:
	-	`sha256:42b5fd04c7043e5ec6b71e54436df306af3e6e32f49b1e99258cab1b09efac66`  
		Last Modified: Fri, 10 Oct 2025 00:39:59 GMT  
		Size: 5.3 MB (5255193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a195b8367162213ff05a6c5da771f467a59ed538f9d200126603cd41c391844`  
		Last Modified: Fri, 10 Oct 2025 00:40:00 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
