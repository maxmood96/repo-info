## `clojure:temurin-8-tools-deps-1.12.5.1645-bookworm`

```console
$ docker pull clojure@sha256:bc998a1eed84ebdf879d46af0a63bde9120e6f7bd6ce7e38fc79a04abfc4de86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1645-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f1ba2b9a72f1c3f164008277766b7ee7cbd12a42703b746a04beae9f90d186ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184901631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6cd795c7224a477b10002baba23204088f175fb2fd7cb8bd479840914b23c9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:12:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:12:46 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:12:46 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c75e70251507438984821ad2e02089608b415f999d5b601e9c9afe75d60ce4`  
		Last Modified: Fri, 15 May 2026 20:13:23 GMT  
		Size: 55.2 MB (55198706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b230c0e628f28842c8b2997e56df6ea3e586420651cbb3b37d1b4ac891c5711`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 81.2 MB (81213603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccbe227e9b4d341e1709f1c6e8d78179c2706bf32150508d2f25eea82109968`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d28af5ce9029d3b4dd267fa6095759740da9d00b8868863af1dd5401b62fbac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1fa05ad714116526b5748eabf968b5baef2a941262211eaed98c774634408e`

```dockerfile
```

-	Layers:
	-	`sha256:4e6865c66d8ce65c773ad9ab65922227d19c9fda432590d00796855ceb360d3e`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 7.5 MB (7499287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c598813a820f21f428358f62be6bf24e15e8d87e65dc47fdb61398901b1415b3`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1645-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a18eb55d997839cf00ad6e569787b6ae516a7cd795c7433cf043fdd3489119ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183841207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca63549566af636161bb31601453b3772d7561a1ef79ad76cdb093df3441c902`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:13:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:13:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:13:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:13:23 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:23 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c803b8f13c09682129ceabfceaa2bd60762fb518753800335ebe2d59a61c0ce3`  
		Last Modified: Fri, 15 May 2026 20:13:57 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a0c9aab21fd12c5febc035549da4da9d7d12ee034fb0f3fec677a2157f529e`  
		Last Modified: Fri, 15 May 2026 20:13:58 GMT  
		Size: 81.2 MB (81194489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abde898c3531c37bc8e3b68741f0871480d24b7392048de8339a643e5f83060`  
		Last Modified: Fri, 15 May 2026 20:13:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:00f082b525d188c8b8a8a80290c16caeb4d299ae8a6c5b06db9d387ae2b97601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40886b4ec63e54b1c66f7d664777a0123c85755ddad5fef14e0ccb17985836d`

```dockerfile
```

-	Layers:
	-	`sha256:b010cf801d2d000516f954bb3398606c248ea2f3c1b1ca48e53583a5c0254899`  
		Last Modified: Fri, 15 May 2026 20:13:55 GMT  
		Size: 7.5 MB (7505750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23ef9b41c664af1c1a946816799e3d67cdb5c211eb0ae704cc29b4d18b44365`  
		Last Modified: Fri, 15 May 2026 20:13:54 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1645-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:bdacb4c5fba5e2ff5e4b59dd66d490be0e9abcfe5ce88f7874939947ba84473d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192039697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36acf12b26eb1e3026148e26362d20e883d7502c67f408db27a41311d9d40da`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:12:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:12:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:12:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baed57d78c0446cb6763b5e86eccec32e2195c45066e437fe1338a88b4c1db74`  
		Last Modified: Fri, 15 May 2026 20:13:29 GMT  
		Size: 87.0 MB (87033110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f1e5960e297ca8394b5eb305d47f52eedc24d3686cf5effaf96035fdc827bf`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fdefc041fddc1f592182cd589d0fb3b2c67cab513d83b2cdd7c099ca4e703e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264ab488ddf05da960faf03a40f818c003ea29b1f028b5e91f65b390c3993c9a`

```dockerfile
```

-	Layers:
	-	`sha256:4c435e25688f669d8999f19b825ca1e826800791fae618b44dc3722e1ad32f35`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 7.5 MB (7505098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8360c75719773f16118615041bc081aad6f2d7b7f2e2dc97509393d0a2ca8ae`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
