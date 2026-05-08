## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:a61e1f7b4c494342864cb94fd7533ef903e9984287500a88af6793dc49e855d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c1480c0037af3b390356d5f73fcac4942eaa9f1ba153faa085f09b2b7b4ce072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269267206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a765f230f682404b3c13e9e11fd1a7f8df45e0fd0c4ebcf2557769e40a03e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:07:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:07:53 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:08:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:08:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867bb2453c7775fdf3aa07ea5401389ccf4baef69e8b3fa3e000e7ffc6c499a8`  
		Last Modified: Fri, 08 May 2026 00:08:28 GMT  
		Size: 145.9 MB (145905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0777d9f11d035cff555ad1c57fd94d3695bee6959dc0e0e384729e250ccdd8a7`  
		Last Modified: Fri, 08 May 2026 00:08:27 GMT  
		Size: 69.6 MB (69597532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5939fd78462929cfc949aa912978c2b717831f3ef3351c03b1d824d6d849bb`  
		Last Modified: Fri, 08 May 2026 00:08:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e299a53ef2e2b4abb47963761bccbe9780186cb1fccfd40c716d84e55e33a60`  
		Last Modified: Fri, 08 May 2026 00:08:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a7a83af8c37e4a4f01f351ea77de7c0ffc669bf29d457d78910b06001fd8ee77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7424211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b619324b590d830549c632cc3f93aa3f46cffb5bbdf6fb9cad447629ba2e023`

```dockerfile
```

-	Layers:
	-	`sha256:cac5edd689aa1d9e1ddd30029fe609a936832dcbbbe796ede6fc6d460de90be3`  
		Last Modified: Fri, 08 May 2026 00:08:24 GMT  
		Size: 7.4 MB (7408280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12adb767562b74946c36e8c414e74a917f84ef7e94c9afb8ebc39ef2bf7a7726`  
		Last Modified: Fri, 08 May 2026 00:08:23 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:30e96fd66ec807a5b70a11d313a685a3037d98fb22f2b07688ae42374376e8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266716870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3289081c92232a8fb2bd7aa495c32111666ce5ac875b1d88c2e0ec41863963cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:08:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:09:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:09:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650531e3648ee40ea90212a9e49051657d86424f2fde32afb4a93a01e87c0c56`  
		Last Modified: Fri, 08 May 2026 00:09:26 GMT  
		Size: 144.7 MB (144724305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c4355191fde154f6ed2f0104e293e8e9c4c3479c2a40b923d82b083bcad56b`  
		Last Modified: Fri, 08 May 2026 00:10:03 GMT  
		Size: 69.7 MB (69738521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62577f8220b640d71cda0c9effe1c1ec9684889159364ca1e02c48c4296cacd`  
		Last Modified: Fri, 08 May 2026 00:10:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7d827266fcb8ccc050913db3baf0780b103575bec6b4428b2486e1ee6e6000`  
		Last Modified: Fri, 08 May 2026 00:10:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:70dbc2af00873e1bc645fc8752c1401846e47fdb036672fb9455d00e6b6a5e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2703f57470a4a3671b388d37ec71ebbcbee884ef2c69d8b507107ec3d41b8a`

```dockerfile
```

-	Layers:
	-	`sha256:21f7efe80117567ee16a24bb28eb61614c48c2d1ed659cfbb9681cd811aee4f3`  
		Last Modified: Fri, 08 May 2026 00:10:01 GMT  
		Size: 7.4 MB (7413379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4734e6aff5170d3a88d49dd02fad3bb6ba7261a0a2aef716e822584701a914c9`  
		Last Modified: Fri, 08 May 2026 00:10:01 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
