## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a2c135c324b5c5ff4f56d65d6ea7755dd8304de99ddd398aa652aa0282e330f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d7c81dfea02bb16ef491ed91ad90022a01701cf5965a8422602e14eba15cc8c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282615844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e794439d60ab03255d33466eef129a51d59bcf93f90d2fac3b90e93457f4bfd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:29:47 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:29:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:31:58 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:31:58 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:32:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:32:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:32:16 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:32:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:32:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d9385d4608e531503b27c9f1751bf5d9d34e1278318925ecd583df6963dd5a`  
		Last Modified: Wed, 24 Apr 2024 21:52:38 GMT  
		Size: 158.5 MB (158498231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a187f14fb0d32fe64ee501fe294c9da5762e97fd9d695310e644054b5e36fc`  
		Last Modified: Wed, 24 Apr 2024 21:54:38 GMT  
		Size: 69.0 MB (69017724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de92eaf53bd93a90d970a78f54f52b5655d96315f5d216bf057c4fb142acf2b2`  
		Last Modified: Wed, 24 Apr 2024 21:54:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8960f64af66d2956e840a4464b8585f790ce5b71369d078f67dc57a909dc1111`  
		Last Modified: Wed, 24 Apr 2024 21:54:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8eb9f76b4476114b1d33864564dd4880b14215421ef0b6c96c15bf95496ea45a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279548725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff24495f69467ef3dbf88ba8b08930a32aec5eba29731dde0478c6c05129660`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:13:14 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:13:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:15:00 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:15:00 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:15:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:15:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:15:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:15:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:15:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7477453a8f7ede5b3451af062fdfd3ed3ce2cfea8195773533d15844f17ea0e9`  
		Last Modified: Wed, 24 Apr 2024 19:32:22 GMT  
		Size: 156.7 MB (156665520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca03530537319488ae1a1408f6531b2794f4bd5e02a98505fbef472c87bb9af`  
		Last Modified: Wed, 24 Apr 2024 19:34:04 GMT  
		Size: 69.1 MB (69142225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf87575c0e3f06755d10c0d0b8ada7c750b2c79127c2803eec82def4f701574`  
		Last Modified: Wed, 24 Apr 2024 19:33:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6a539b04dbd76d2469dfb98c55d6760310e4628cf4f03087b6d7cf4f980545`  
		Last Modified: Wed, 24 Apr 2024 19:33:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
