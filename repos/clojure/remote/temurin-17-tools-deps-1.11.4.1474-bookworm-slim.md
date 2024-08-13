## `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim`

```console
$ docker pull clojure@sha256:a4f044202dc910c0e7c21fa2519cea73b3322d4c7b2aa32c6ff7c7e5fcffb661
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f5abf25b581e7002669fe1e7734ab78cd162be6091a5affe0c07a8909ffba0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243318178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3818ead549801a749828c4542c5e98d51d5aa9d06f14f2738d84a15245e17c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f9dc5cc2859e1d0dfdd3a795ddd545cf38308f4f64476e4d943433db4c9089`  
		Last Modified: Tue, 13 Aug 2024 01:11:34 GMT  
		Size: 145.2 MB (145166561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af0b21a7d2ebb1e2d4798636e8d4b90352e43d3ba4855ba2d6f411fd9364db3`  
		Last Modified: Tue, 13 Aug 2024 01:11:32 GMT  
		Size: 69.0 MB (69024345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4656058ad6aa1c654c0eec86d4f574e50506d289279bc89e30048d2ffbc689e`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febd7d8e309e929a4b35a425228c1b418bee1d97fd4b0f3a161826e719df4c63`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7894e7f1360e774275317506bfd3e8e57fb6b4ea9ae4dec6b7aea24b9bbf8508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceba9504ccecdd417d229aa1a1c7cc76953046d2b3e8979588ec66db49c00416`

```dockerfile
```

-	Layers:
	-	`sha256:a78d3faab23aa8e3c37ababac6e31ab3321492c268ef89562633147d1a18f94b`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d717ee069a9d930ca0f9d479527fe10316a867de10372f0b39ba20370ace65b6`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5779b2f5013437b823fee6e634783ce5eccf752d0a59f010697b9e28b63c8334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241889683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b74c295403d0bc1187a63947d8c8e1f348d75649bae015c27801c6db968d9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228d17b6c8b13f68265397f277085d6d433219f01c8551f3a5272bb6cd9389fe`  
		Last Modified: Thu, 25 Jul 2024 19:30:31 GMT  
		Size: 144.0 MB (143959439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e13d87685e11c9c8aa30ae5786520d3a1709f4b25a8f1d680d722e7ebc0974`  
		Last Modified: Wed, 07 Aug 2024 20:08:01 GMT  
		Size: 68.8 MB (68772629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2884894cc69f1d814e22a179860a979ba2f6c144f3f4947b4f97eec1c72abae7`  
		Last Modified: Wed, 07 Aug 2024 20:07:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0021ec02e275c40d1113b4c010705f6f157a60deeb65dbef42c0fb139cfc8920`  
		Last Modified: Wed, 07 Aug 2024 20:07:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bcf93ef38c93af4be46027e5dad0c4508220eaea925b7d6a9cbff43c6af40e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac98e1572a4e40f8751bfb93803835ac1c2c247081b6528a4181ad67f1f3176`

```dockerfile
```

-	Layers:
	-	`sha256:7fb0f0e1fc11e9013acee4f2372b69a36806b8d31d956483af86b77531bd56f1`  
		Last Modified: Wed, 07 Aug 2024 20:07:59 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31999acb6eaeb222ae7dc5b73d9f1f0a60073cdc77eecd2abbcccc23e6d8f7dd`  
		Last Modified: Wed, 07 Aug 2024 20:07:59 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
