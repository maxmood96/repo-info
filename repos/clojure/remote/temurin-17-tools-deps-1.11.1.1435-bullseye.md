## `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:d8f07b8824ee119b3fc31a86f651c122a5d4a41c8ad0da4fe6bd704ac483cc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d891264e7386d55b9215fb03d720bd845d047997884be04b52cc2c74d37894d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268994902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3502d776aad8de26bf1e08c65d1df60f4236a0c9ccd43b4a92204b17ec454c5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:22:28 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:26:59 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 16 Feb 2024 05:26:59 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:27:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 16 Feb 2024 05:27:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 16 Feb 2024 05:27:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:27:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:27:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868da7564e4b1e4da0fe7d569a33bd39a03d781e42fcb9924379b0ad8881c350`  
		Last Modified: Fri, 16 Feb 2024 05:37:07 GMT  
		Size: 144.9 MB (144892562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ebbcd2173c43321c35124f4662b1f2e97b56c7cd419026c51992053ccf7f0d`  
		Last Modified: Fri, 16 Feb 2024 05:39:32 GMT  
		Size: 69.0 MB (69016485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e8c1f55bb4e1cb1b8cddd9c97fd0fe78af892bdfec9475e707bf0e3b48c80`  
		Last Modified: Fri, 16 Feb 2024 05:39:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9094456347cc812a3d43b505701346006b6fecabd1cc780390423e016b62621b`  
		Last Modified: Fri, 16 Feb 2024 05:39:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbaa7eebd48831ecb6f331a438ac6212ca55174d352c91694f8b59214fedcaaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266585288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1f7f73c26385a891805c506d7cc8b12b725f1034f255182f744fd08a8160ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:59:16 GMT
COPY dir:868002d69a8870cfd22502db6415e3cd8591d5271a62d90057620eefd5ce7d20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:59:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 08:03:10 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 16 Feb 2024 08:03:10 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 08:03:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 16 Feb 2024 08:03:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 16 Feb 2024 08:03:25 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 08:03:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 08:03:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e526ffefa8998fd08362763c71e6372b2c72a620786af9e0c0b878140288c6`  
		Last Modified: Fri, 16 Feb 2024 08:12:01 GMT  
		Size: 143.7 MB (143720918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0706ae994bbc7b1b58dc2532e3fc8f842b77b9c1e04f2462b0193435a18405f`  
		Last Modified: Fri, 16 Feb 2024 08:14:15 GMT  
		Size: 69.1 MB (69141867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d132f00b0ab28459a755b74f7e8648599753cfde51e7d1659d0dda57982aa926`  
		Last Modified: Fri, 16 Feb 2024 08:14:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e750878d6f0ba31f670175d110875f71089b183dc684abf61338591be2d47b9`  
		Last Modified: Fri, 16 Feb 2024 08:14:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
