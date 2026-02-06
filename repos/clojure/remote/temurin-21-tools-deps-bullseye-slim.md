## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:4e583695912c350e3a836306697eba4f69e1be7eb8fa7b8554e3efe0303b6227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b902b0e867070d4fdb54da86479279c0cfbdbffa3a2f5db039078cacf02d8a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247252899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d9cff796ca1cc7407c26fb5c993860435d7b136a687557b20bac6d7a958a9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:09 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:06:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:06:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f5e50bc4c22ca4fba6be7d18906e6ba2716ee2d5eec39dbac3cdd2a0fdd3ef`  
		Last Modified: Thu, 05 Feb 2026 23:06:48 GMT  
		Size: 157.9 MB (157857074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb11bd69f97c09ebac20f494c56061d35779aba8787f5c87ca0bb6d59485333`  
		Last Modified: Thu, 05 Feb 2026 23:06:46 GMT  
		Size: 59.1 MB (59136502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26b2bedab65eb75ae789d0d4791080474baefd4fae117b2632cfe84e75c8e52`  
		Last Modified: Thu, 05 Feb 2026 23:06:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cf48814ba4817302fab902ef88fff118b6618fe9e4e8231e287f030b0c7704`  
		Last Modified: Thu, 05 Feb 2026 23:06:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f082286567be2b478a0798556bd7cb64855752220e613c83f5de6289789d5234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca1ccfe4d13568134ce71965cc72f744ac57203b9b12442dc5617e798be6f78`

```dockerfile
```

-	Layers:
	-	`sha256:6764c9ff77f379ffba76350a5b5a5dc90b333da1afa3d85a231ecb79fada3f03`  
		Last Modified: Thu, 05 Feb 2026 23:06:43 GMT  
		Size: 5.3 MB (5311972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18512afe042ee2c197244de87dd1e45aea6f0faca92da6a02292895a97b98dfe`  
		Last Modified: Thu, 05 Feb 2026 23:06:43 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:95d7f453f548a79db5cda0dfaefd008edeff56cee6f5582eec28c3baec4b4a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244166548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c43a7620aef601f20546503ba3f5250d70a27cc73eed10289cb0098a8c0fc8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:07:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:20 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:20 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8452df53d7901067f97949b7483b0a379769b3ed94166d65e44c263cc32cb7`  
		Last Modified: Thu, 05 Feb 2026 23:07:59 GMT  
		Size: 156.1 MB (156133062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d802a22b60d02d2dc034d824cdf6ec1a45bc2c84e403fbdec38933f31931f37d`  
		Last Modified: Thu, 05 Feb 2026 23:07:58 GMT  
		Size: 59.3 MB (59288005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab69fc73b44bde3cf21bdc16f8d93464e1c27e48279566e9f49f22225bfab7d`  
		Last Modified: Thu, 05 Feb 2026 23:07:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5961b52b6a81cb64eeab77771de08205e358b793e969f8075b156304a0e0e954`  
		Last Modified: Thu, 05 Feb 2026 23:07:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3c874c7bbb8b3b860389d4f63e9732174d8bb7570bce2efc91dd089967c1047c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5333658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24d45183b0cdb55e595ba93153916c4820be9a193348144a88ca399df6f1720`

```dockerfile
```

-	Layers:
	-	`sha256:65180b717454ca964a5098e9e5181760f356b89deeb062835097e8b28fe9035f`  
		Last Modified: Thu, 05 Feb 2026 23:07:56 GMT  
		Size: 5.3 MB (5317704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f3ae1e02c079dbb4a4d9d40b501b5d543187a71576e57b39be2de4b712404e`  
		Last Modified: Thu, 05 Feb 2026 23:07:55 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
