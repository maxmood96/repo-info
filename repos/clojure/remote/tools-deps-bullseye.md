## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:cac33d4e71bba5feea5494183aa62ca0fd0db678edcc2ab128e062372ea7bfab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9dcf3e29e263b1118cb298942a348d8bae96c83f90c83a20faea8b806ec2c42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282994706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373a6f20e4ca5da11bc1b3a75b523727cde47397c52ba5e5dc3148726f114c69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba65de38025fcdc65bb50a396caf55cba7c87535bf8d81b0cf4cf5091ab45889`  
		Last Modified: Sat, 19 Oct 2024 02:59:51 GMT  
		Size: 158.6 MB (158579322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b120fbdb960a5bba35bdcafe668fe3f99b03884d099067e212d15b727e09f61a`  
		Last Modified: Sat, 19 Oct 2024 02:59:49 GMT  
		Size: 69.3 MB (69333732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e699a56e29fffc498134a818af1aabb1105a142ec6e5cb0448ca025a7f00a0`  
		Last Modified: Sat, 19 Oct 2024 02:59:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd8f55b0bbf7c1a139f2f47f00dedbae3ac2c96dc4d41feb20c735d54f26b3d`  
		Last Modified: Sat, 19 Oct 2024 02:59:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:12269b04655020631074c0b72639897c20f96f9cb2b7477259373852073442b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0206cafd85335ac5a7aabef47d1f3ecbb500a14a0b381b05b04836f77cf373f0`

```dockerfile
```

-	Layers:
	-	`sha256:0d0dcd31a7dfa20cb7484fc0879e57d70eb432dd1171b551457d1cda464ec84f`  
		Last Modified: Sat, 19 Oct 2024 02:59:47 GMT  
		Size: 7.2 MB (7219615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ba828a13d2cc79008e2ec47f28f25e6e5857f0ab18d69c2d65bc6182bafb5b`  
		Last Modified: Sat, 19 Oct 2024 02:59:47 GMT  
		Size: 16.3 KB (16322 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dcc98db4e1bc066188e139319ba7ef3a05429d0e178ea3751cb3c450170432c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279949018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc95d820294a4581a1c836c46f7530daf110500d1ea473e5dd08d1687441e91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6c724a7bc6cad4a23ca6399b659781378a31f3d057e3a52e35e8a27699eb41`  
		Last Modified: Thu, 17 Oct 2024 08:21:06 GMT  
		Size: 156.7 MB (156746197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2104b5d73fde5f1676859ed83f39dfcf41d2a5e444888a2e353b80038b206ce3`  
		Last Modified: Thu, 17 Oct 2024 08:24:49 GMT  
		Size: 69.5 MB (69466888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a15bc81ffb492dd77d700da83122a171e009ffcde72294b9d913051498373`  
		Last Modified: Thu, 17 Oct 2024 08:24:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5b868f65e25b6d32bdb0856ac334ab99c118039c51526bf22053332e5d5bcb`  
		Last Modified: Thu, 17 Oct 2024 08:24:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9a2432ae88fc8c33d1863fe7d6d33dff2e471821c67e1c124c2490472844e87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6559e1e004fc1e53c36f95d0a5926859d9e46c86e7dd756ae485efe44631f97`

```dockerfile
```

-	Layers:
	-	`sha256:95354d37b0d6081be253b1ff9b6018c0b030926fc9545320f8482e7937f84ca0`  
		Last Modified: Thu, 17 Oct 2024 08:24:47 GMT  
		Size: 7.2 MB (7198997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b13107907f1f029d2fdbdcb3547abc06ef927666d0f63cc1089883a37b28a36`  
		Last Modified: Thu, 17 Oct 2024 08:24:47 GMT  
		Size: 16.3 KB (16284 bytes)  
		MIME: application/vnd.in-toto+json
