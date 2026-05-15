## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:732cb1c5efa7cdb22f87e40b3b0bb0a49406c6fad69e93a8fe4d7bd0062c71c2
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:05ec71a9b825cf1bb462fcabe23d29c36dc6e68b54bbb75643e6ba28cbf5843d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259994833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75272dadfeebb07909236427138a68c92523d22020c2738aad5c637884ced7dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:57 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:57 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d54befd331fd0937d266b32b504271eff2564525849a61a064b9aa604587a4`  
		Last Modified: Thu, 14 May 2026 23:36:36 GMT  
		Size: 158.2 MB (158166937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a40c7c8be43e5fde607b6ee95d5d639768351782a4c2d6c3cb20509476234e`  
		Last Modified: Thu, 14 May 2026 23:36:35 GMT  
		Size: 72.0 MB (72046629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b527bcb9d2e30902ffc264bb8f78489d1ed95e4b49ece1c8a48fc308fa181c`  
		Last Modified: Thu, 14 May 2026 23:36:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725dd417842d1294bc18af3c7cec6b8275bcc607215601040278a31219ac91f4`  
		Last Modified: Thu, 14 May 2026 23:36:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e16cca108cf87f6c2d011864a3f1a34731c9a90ebcb3e5eb9ef412c11e4111b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523f095be35722e0ce82a30aeda6a8c5bb56c1680bff38adb7ebf2613351eca0`

```dockerfile
```

-	Layers:
	-	`sha256:d2e8691527180a82fd0542c36908a4146c1c3eb18b8e1ecb988be850e6d6f97c`  
		Last Modified: Thu, 14 May 2026 23:36:31 GMT  
		Size: 5.3 MB (5261705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6922e56d9f0e815c82b04059f70e83b8da884f34cae1a7fb8462eb7f524438`  
		Last Modified: Thu, 14 May 2026 23:36:31 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7955f572fba483604d74d78117e44aed16d8304f0f2017e4d96e0fd35150cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258460603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2877e5e2a2493a5726d5f8a355906063210d6d4952e353d9464fe710cbb01f7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:36:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:03 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:03 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f90d6e1909737e82ab88c5421572d4ce69b62c08acf31f3494a2ea71360e234`  
		Last Modified: Thu, 14 May 2026 23:36:44 GMT  
		Size: 156.5 MB (156461285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2809e59b5c7c1792a47153d437a291c548127719c8a82f871c03a048a61547eb`  
		Last Modified: Thu, 14 May 2026 23:36:42 GMT  
		Size: 71.9 MB (71854630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34290669f583119c9b6ce6873bcba90fa8ac8c5493e42e6ec9cbcaa59484333`  
		Last Modified: Thu, 14 May 2026 23:36:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69eda3c56e0e2916c8c5c729abd629b192288918603ff993b155c47baa93095`  
		Last Modified: Thu, 14 May 2026 23:36:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7da4252a9ab89f083ea0b2f2371ce2dda29a810f8277fa1179b4ae0c0f3ec8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa6e1f6da6f1a5b58851085bbafa37430188e5e436fd453bffe1c62fa33a51f`

```dockerfile
```

-	Layers:
	-	`sha256:8d12541c69759084b7cd3ccc01aeede3b023dff0738618bed179352049e453e6`  
		Last Modified: Thu, 14 May 2026 23:36:39 GMT  
		Size: 5.3 MB (5267474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dda4c7eb6c691d8e50e7c2f2fbe74620bbafeae6e588a8e8eb2b2599b6682bc`  
		Last Modified: Thu, 14 May 2026 23:36:39 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8644e11a0e83e3c8913d590f61bfc6390b32ca9b189284ed6b9b94e117908432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269399262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3266a6f11f804702b80b76827fae53a8e650b0b28b495c8eabecca8dfb542381`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:50:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:50:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:50:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:50:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:50:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a2e44170efa239ff5477b73b12dee474d93e51231983d36720618d44729646`  
		Last Modified: Thu, 14 May 2026 23:51:31 GMT  
		Size: 77.5 MB (77456846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c673a8788416f0b78e56fc54c59a5f31d1bac103db3425cd7a8ae717843c28`  
		Last Modified: Thu, 14 May 2026 23:51:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ff2b345bf8d6b516c9ce199f0323ca94f28386a12835a18cca7de19c480cb4`  
		Last Modified: Thu, 14 May 2026 23:51:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5180a4874b35bbe1bf4bcce863cfe1ba9235046ca1386e5999747fc6b669d42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c289124731d46e2243643f447f05da6d61c0dc96be4b32a043e4885601f251`

```dockerfile
```

-	Layers:
	-	`sha256:678d89e2da40faf94f09e2a1dcebfeb85a98c5f0b97411cb4a6b773a7780dc58`  
		Last Modified: Thu, 14 May 2026 23:51:29 GMT  
		Size: 5.3 MB (5266076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d9beb092f577e683e91747e7b84d83a1ffdffe5b9dcd166b12f8c2e5d21a31`  
		Last Modified: Thu, 14 May 2026 23:51:28 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:710db91c816ca8fbcac262352d58b3b7558aa9a62ef3f62dc3fbb657ea1a70ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250244390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277dfc6bdc97c9177787067588dcc524054be6afeb0821c5338f389d169dd8a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:36:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:44 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:44 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60fdad65c5bfeaf0c27790ab98e49237e7c213a49fdd76e96531aa878f36899`  
		Last Modified: Thu, 14 May 2026 23:37:28 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365adb91feb965e94e81b1e5ceabdd7f442e2613d491c35f27d2959af978c867`  
		Last Modified: Thu, 14 May 2026 23:37:27 GMT  
		Size: 73.0 MB (73014652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e72f69751d92afa6e12707cc5f361debb19d07fbc6d4e7cfa299dbd3bded51`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4fc3b3c0d51eb320f07f9a5f9146f5fedd47ad10c594ff24ac0cbd4f1d23bc`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:449ce605f0025e4363f063c3409ed112d4db12e75d1067c721d32dce228b3c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af74dbcbf9acc7fcf4676d6c4f381d3d344258054693a6e47baa556aaad005a`

```dockerfile
```

-	Layers:
	-	`sha256:3902e4c4a31e73f126b17de3f5e8c65ec1c29f383f0316151f07070075c60236`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 5.3 MB (5257629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ded244af582944f826ec36b5cf50d2c2fdc792b45ac3de3182ecfc2c151a4a1`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 16.0 KB (15965 bytes)  
		MIME: application/vnd.in-toto+json
