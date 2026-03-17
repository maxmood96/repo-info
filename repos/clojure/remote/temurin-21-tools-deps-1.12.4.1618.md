## `clojure:temurin-21-tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:9e24a8f5c6c14bd35ff5777339dacbc4c762dcfb5616b2ff7de79ade4c369ea7
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

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; amd64

```console
$ docker pull clojure@sha256:8aa4534ac7e2aebe859529663871fd4ac41c51c83fdda6fc31e30d84777f7eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287525436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c8cd8e3aa93dd7cdb49ae1f91eae0b61d6ed9cd30c53eb59a5212bce9621c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:59:43 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:59:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:59:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb2fd16fe16484060bb9250403eb292af88d61d999e4518f1e36f92bc848203`  
		Last Modified: Tue, 17 Mar 2026 03:00:24 GMT  
		Size: 157.9 MB (157857091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54d57f4be907ba372ff592b7e1c9a15a0785bd96e85a70b05a2dfab32941f3d`  
		Last Modified: Tue, 17 Mar 2026 03:00:23 GMT  
		Size: 81.2 MB (81178721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc590eeab816d49db4599ed2a74882a3db40c11b570aa10d268e55b05afb67ee`  
		Last Modified: Tue, 17 Mar 2026 03:00:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2123ab178939d8e16e5ffb28b823ffa270bac15e4e095320139a048dd64540`  
		Last Modified: Tue, 17 Mar 2026 03:00:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:b64f252aa47ffceab22dd9941324fac8aa391a2bee2a24373c070ffa7f9d1d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3081f5c5040396e82c3e1b6475519924104d0d0d9588d43f1dd4cd3a97aef18`

```dockerfile
```

-	Layers:
	-	`sha256:6c8f6812720f03dfb2015adef8e8e5f0a83fce5df776a61a76ba3256b6c4b6c9`  
		Last Modified: Tue, 17 Mar 2026 03:00:20 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac07b2de53bb429db8d35b72b762d432364a839b1b1600d5cad1827c06f9184e`  
		Last Modified: Tue, 17 Mar 2026 03:00:20 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b240b1bfb4186ac425fb64ce0da7bdc923660eb9fe173f923bf23bed0ec3833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285665484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa52683f97612374025b0c49e064eb2b7283029f3fdccf3386a67004e10f751b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:04:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:04:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:04:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:04:22 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:04:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:04:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1a5e0cc45268b1422d4a1a103d7ef3978f4ffb81e6ce948bbf097442f49120`  
		Last Modified: Tue, 17 Mar 2026 03:05:02 GMT  
		Size: 156.1 MB (156133026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5ee8c855f30145d2353b7122c4ddfd4ffb8a4183db7096f2d3121bfe3e446a`  
		Last Modified: Tue, 17 Mar 2026 03:05:01 GMT  
		Size: 81.2 MB (81158384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d71c65841b8293c00d5d6c1ad03a50771c0cedec93dca3174a57b7e618fe75`  
		Last Modified: Tue, 17 Mar 2026 03:04:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2665c9e3b1625a47b69394459245fd1d3f53b1ac4206bd5986abdc7bde43da`  
		Last Modified: Tue, 17 Mar 2026 03:04:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:f1163a44ded2591a5f6d1db630107f9f7d75546a74ca63e84513678d8acc4445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02adf5786e7b6af9aa79ef61d4575d87717d3ca60f14885764fc7ae9e61d33a3`

```dockerfile
```

-	Layers:
	-	`sha256:2509dff23b5cdd9fac71fd8c66be06f12fbd6e9cbbf49865b06797a6804e3ce8`  
		Last Modified: Tue, 17 Mar 2026 03:04:58 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62f6e51b7bebe7c6e0880a7e651d4e1d5dd62173188e19f3a44d81977d60928`  
		Last Modified: Tue, 17 Mar 2026 03:04:58 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:e5770c1197675761e6b779e9122c9fbc7c77de498304ccbcc61833b7e5d9244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297315597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33c11e7d85c60ad6f7d46da29597690aafab75d01917bdb2b3a43a755dcdb3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:57:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:57:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:57:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:57:21 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:58:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:58:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:58:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:58:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:58:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa55a66ef4e8dff32d0371fd3807d5854e51d4a75ac606239492131837d03381`  
		Last Modified: Mon, 09 Mar 2026 20:59:47 GMT  
		Size: 158.0 MB (157977536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac930b650181bc323783cddf5508c88741a644bddf638c409284f9839621f0`  
		Last Modified: Mon, 09 Mar 2026 20:59:45 GMT  
		Size: 87.0 MB (87000222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3664d8f6e485b2ed7c7f05c7935594805f186b674c0fef2339157b2fd4c0d44`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a414f10948b4dd5a581827c41bd82ddfa0b23d8dfbead9546e4e448c9ef2a00e`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:0944f56db65087474d372d341a37b350353254406b853f359a5db1d95e699ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b33de67073feb39730c68cc0637f025c4e492daf8e04459874aa13db8dc00ab`

```dockerfile
```

-	Layers:
	-	`sha256:09762b62ae99b5f8ce95681b9cb7bc0e455a9f5d51f24990bf1f71550d10e8f0`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d9c282558e075a4300746477ac118dbe930e5e6fb5e1a8f22670201614d46a`  
		Last Modified: Mon, 09 Mar 2026 20:59:42 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:e5021884bb61edd0228615e3b47136ceeee4022f74ec9d7a478e175b5237cac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274242252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b820547fd31a7babb44d8811cff342dd14d86bec1f237dd754f9569ca9d220ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:40:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:40:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:40:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:40:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:40:43 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:41:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:41:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:41:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:41:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:41:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b161d0356caf3a018526acb56d144635fdbd5223d94b2c955348c888ba2c4966`  
		Last Modified: Tue, 17 Mar 2026 11:42:03 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80629a3b5c03f459fa8b92807063b063e5b75572c95318a3009fb5e0f9a95fc7`  
		Last Modified: Tue, 17 Mar 2026 11:42:02 GMT  
		Size: 80.0 MB (79988078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e14373520566f5cbb44c36dd9ae544e5fa118a066e999bcfc50a16f8641a00`  
		Last Modified: Tue, 17 Mar 2026 11:41:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8362ce7cd7991373801164ba23179487a8c32cb3f2911a2c13074411cfd1d2`  
		Last Modified: Tue, 17 Mar 2026 11:41:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:daab9d255523991b64b7b9e1fe4ed1594a68483108905de8eddd7f8e50ef34b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff897e1a39b54074a8836945e239ff8c9839895b30eb424c37174f53f2f581a`

```dockerfile
```

-	Layers:
	-	`sha256:8953b793eafc062d8f06c23914edeb2b1200d334470963d1fc7d47d38d18754c`  
		Last Modified: Tue, 17 Mar 2026 11:42:00 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59cfdf81af11796318c29fda64c5e5daff9115254cfa3b9e522756012470068`  
		Last Modified: Tue, 17 Mar 2026 11:41:59 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
