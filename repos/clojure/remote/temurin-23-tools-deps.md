## `clojure:temurin-23-tools-deps`

```console
$ docker pull clojure@sha256:bb5a3cbe422aaca9c860d09a651a66fce434320b10f6db26e67468e9e795c333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:427202371bbbe8592ac981a07b2b370561ac6ad472fc52068ee844b2c0e2cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294786420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ed19d39b13e34fe2d7775e7312b3c60c29b6084dbe8a6f4f4a0855c597799d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b5ac0155384a97f60455cbf44b86f5e5d239ad69e4d543c98077ca21cad7b`  
		Last Modified: Mon, 10 Mar 2025 17:40:17 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b1eed4d7be1d0d9956cd24e9cebd64493cba7882e5ade59558f4adf85711f7`  
		Last Modified: Mon, 10 Mar 2025 17:40:17 GMT  
		Size: 81.0 MB (80993048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aca9ac7e25174a6be8ffd762547ecef99fad0968505eb5313b3ad83a63dd28e`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c6cb6a3f8b043c0879ba5987ae5e2ae0e9ff68b55a018740ca99f2cd67b066`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:8babaf2f63f8d0d0c714d86385b02b80650136d98d15b0efd5a6863105cc13f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920941d19cc8be3703a3b97882b782023f171fae2683e664610029b001b210ab`

```dockerfile
```

-	Layers:
	-	`sha256:b7399b7833bc979a7282cd37db59441e413af7b2fa51b8a8c68afae457d6ce02`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 7.2 MB (7176785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a53fe06abc827e416750cabfd2c723427192fed02402b3f1560b6574710f2ad`  
		Last Modified: Mon, 10 Mar 2025 17:40:16 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:842aa8f667602b1d1437213a691e26b2cacd2640bfd6b630a128f617c6ea71d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292493051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45590ad55998248088e2db61ac1c291c5aae3a3113ba0d7f75de3d141ce2904d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459a651417ff47b1d2b782ab86b9ac6c1ac93e7c552a5c0f83350383fd90a52b`  
		Last Modified: Mon, 10 Mar 2025 18:02:05 GMT  
		Size: 163.3 MB (163341424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcb93031150f52a34971c06d8355dc9d65f9dd1c5e878682cdf71f304a47371`  
		Last Modified: Mon, 10 Mar 2025 18:02:04 GMT  
		Size: 80.8 MB (80842575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463af1a67a6656a6c0217a05696b0f385043d05baedecab4e26107fab214e65e`  
		Last Modified: Mon, 10 Mar 2025 18:02:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f566700f32f3c3130563a4c2998edb2dc4239f0f348b8f3e9b2c8f9563113a`  
		Last Modified: Mon, 10 Mar 2025 18:02:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:279b09573ecc8e0861e1d0050bb5b6c8dafd47e4484156a412fd75a34b419ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd8eacf8b81a7bc06f1b088e26122fac9c9eb186af218d9cbeef6f3726ac9d8`

```dockerfile
```

-	Layers:
	-	`sha256:fd59e69dca1900f19a3d9f6d64a0ac12c97120c9619fe316246502e7e70efef5`  
		Last Modified: Mon, 10 Mar 2025 18:02:02 GMT  
		Size: 7.2 MB (7181951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73f36f865a6a3a3c009d0b7cc1c55e8d4575903d7f8d6fe9a814b1d47976338`  
		Last Modified: Mon, 10 Mar 2025 18:02:01 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
