## `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:cd53f786acead65d3e641eed910d9c1e444333723e6e10c8d655102d473bc50d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e2fe3be1cb2cf7945ca38306c81296bf3a0e8937c57a05e5c48c85b449c0db9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275161941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f1c675b6f759c5fb127fd24afeb04a379627ff3a98b0c4c275129b24af9ea2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569016283d02dc8ce9e9fd364d8a761e1c14edea190e83691f0c2d70f729836`  
		Last Modified: Tue, 02 Jul 2024 03:02:55 GMT  
		Size: 145.1 MB (145095109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6038e3a820b2133d238b8499349b3f2f43d73becf21f819a27d15d9e5eab9`  
		Last Modified: Tue, 02 Jul 2024 03:02:57 GMT  
		Size: 80.5 MB (80511727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc566dce2a5c5afbc993d6533b0f105d562210edd82dcff47766521261958b3f`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dd19befd49eac2e91917271ca23f18f335b2977241f3fc4fa52fb22ab5e7b9`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f78dd569a758ed9cbc3f8e254e0f27618519e89396680f9d6e429c6940e94cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6975400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d6f48ec229c279343b5075b623dac6e5066699e6a479c504c7f443b7ab6136`

```dockerfile
```

-	Layers:
	-	`sha256:c15c67e185b1e83e47ebb9d41c3943958b70490ecde88011d158cfa7c9feabe1`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 7.0 MB (6959961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265fbcbe3e57f4666e0d91072cd26c274451b91cfc9208f6b17f28fbc79d6201`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3545848fb690ab845ead8e6810b14174fccae7a4cc72034a8c9763d94fa4d007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273552456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6379f3cc8c21b03418069dda1a40472a88258c8e3b8a9a0a66c5bfe6d19a5863`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798af59c3dfe0a2333f71d50df86f26dd31e844f8565450854e2afd957021b4b`  
		Last Modified: Thu, 13 Jun 2024 11:35:17 GMT  
		Size: 143.9 MB (143892766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3fc1393c776f72d38cd1a60d48c5ef3c3461661bd48fa34ee590ab480bc4ba`  
		Last Modified: Thu, 13 Jun 2024 11:38:42 GMT  
		Size: 80.0 MB (80045241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a27c7b8f65b1f9338ab38ab5f7e909ca0d1749f984402b4cd11def3d0a11d`  
		Last Modified: Thu, 13 Jun 2024 11:38:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a512b7fe5f9c6f334eec69e60acceef61b1dbd1e902032c215d060eb9fee2d5`  
		Last Modified: Thu, 13 Jun 2024 11:38:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1b1c4fbf89d7e2d2f8725f4c2cfe66fefd1ac312a18cea64bf4edd46f420e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5f134c2931e35c7f92710b3afd8ba2e9499f001ea7d27a749961d2b6618147`

```dockerfile
```

-	Layers:
	-	`sha256:118c7d59c9cb4f7d198f6f1665fb59ebd526e350a86effd7f18d373487b0626d`  
		Last Modified: Thu, 13 Jun 2024 11:38:41 GMT  
		Size: 7.0 MB (6967053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d4e5d172181b0850dcfca5121846ddacad6c03659a2d6ba922ffc72115e3c0`  
		Last Modified: Thu, 13 Jun 2024 11:38:40 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
