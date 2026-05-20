## `clojure:temurin-26-tools-deps-1.12.5.1645-trixie`

```console
$ docker pull clojure@sha256:7a2b043a1ad8c3fbbdda1ad8aeabd783ff107d9f928cd0c4cf894dc36c16c86c
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

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:7926a632193c6bf0a10c7a1cf83026057adc7fb99b5177903dcae1a80ce18142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229443320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07f95204c8cb4a712cf1f9d4de5f5dd886fd01bdbc81b52b8c4f5c3a97252b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:02:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:48 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:49 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:03:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:03:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:03:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:03:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd8850b8c2d0ea49ed92c1c44ae13246bf21f6a37cfda8e0924a2ed70b200b6`  
		Last Modified: Wed, 20 May 2026 00:03:31 GMT  
		Size: 94.5 MB (94524345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720651f201f6b307b3e51f3ad9fd7c529409c82eb5f8ab5155de0070f212470e`  
		Last Modified: Wed, 20 May 2026 00:03:31 GMT  
		Size: 85.6 MB (85607309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced398f3aec40ff9ae64a9f6cd1dfd71a462d799cf191194131efb7ce1afa67d`  
		Last Modified: Wed, 20 May 2026 00:03:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81cde9de30f3a5de9e303212a69dd468ab708ab9b5d6be92a093351b2d88593`  
		Last Modified: Wed, 20 May 2026 00:03:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c98a604b81249f41f68fa9340f3e994122ccf6632dd38c5920cc313b5eaaeb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7452288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f732f6587ec0a3e38d38b9e9764dc79e5e3b5a3e2a2d8d19751970c35a530a73`

```dockerfile
```

-	Layers:
	-	`sha256:cb0528454a4e76f6d0522b4dc36fdce9d6d34b4d50bd1690cdba65447e894d54`  
		Last Modified: Wed, 20 May 2026 00:03:28 GMT  
		Size: 7.4 MB (7436387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aff581704dce5b8811331f41acf1845176962b14a36a675637b4d4b163adbbf`  
		Last Modified: Wed, 20 May 2026 00:03:27 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4bab110d62f1e57ac3a620dc348a06c8dd39e4bc9c55e9da9bd1fa7a7c991c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228609489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712655f4a61b227b114a5e1e2b917da7d8175a6f529412c8a5c4b4de992c73b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:09:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:32 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb37c445a55409ec2164c86dd30864a9fa0991e78d22dd614141581c2235aa`  
		Last Modified: Wed, 20 May 2026 00:10:12 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17da4c48df036f7f6c62dafebe480adbb70b47f1235d56539ebc551c39908fa`  
		Last Modified: Wed, 20 May 2026 00:10:12 GMT  
		Size: 85.4 MB (85431896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4216112ad961ece9d6560e4716c67a3f370fa5a8f1dc3c9d1f515add2fd33164`  
		Last Modified: Wed, 20 May 2026 00:10:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d5675672cc8d7dca6fed40262b5c25641463ae8c2ef06b560f9ffc6ac4cb1`  
		Last Modified: Wed, 20 May 2026 00:10:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9013134849c215719a1c47e49c30c213834ad8b3f24a8df288b47a63505782b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7458794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a08dbb463f78281d2fbf6056bcdf7798fe0576abd102cf73637bdc2d3b9bf4`

```dockerfile
```

-	Layers:
	-	`sha256:8739a560128b1a78c76c3353a862ae40113b8259828f64eaee9124cfe8f400f9`  
		Last Modified: Wed, 20 May 2026 00:10:09 GMT  
		Size: 7.4 MB (7442777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b2480e665dcb220eb243a4ed30d0069fc757315c96cf97d592453df707af0d`  
		Last Modified: Wed, 20 May 2026 00:10:08 GMT  
		Size: 16.0 KB (16017 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d209aa38b5f2644d6a51a69f7fc25780671e4562d8834ac3ee37bc311c7d504a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (238033808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f619c925c1a20cfbf75015e8843d8d0157b88c3c70bf6a14bffa57afe32dce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:47:27 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:47:27 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:53:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:53:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:53:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:53:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:53:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ae203a513e0c8b74c981e5684b8f31f4776f60d5e19fb39186eaa7bfba6fe`  
		Last Modified: Fri, 15 May 2026 21:48:46 GMT  
		Size: 93.9 MB (93902122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1a967785e58d08bb2b03c72746aabd821faafa6db72d0848990b73d8fb7a19`  
		Last Modified: Fri, 15 May 2026 21:53:44 GMT  
		Size: 91.0 MB (91007476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818555b814dab8032c5def66098ccb54f92303ceac6b23b2c5b06585ccce915a`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85d00a28a911795ce2c48657d1fb50e3a901dc881607feda6c27cd093950dd`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b4887732a51a3b34d167ec96238d374d8440a2392f073260beb2968925d870d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f452357de00624e8c83f2a0529cbe0dfb5a4781ddd246d4fd85dd5ec22dd06`

```dockerfile
```

-	Layers:
	-	`sha256:de38fcbb5aa4569bd1abf1a20bf0b578263e78c26f6d869b3518827b5848cecb`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 7.4 MB (7424630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f6ce14800f2121cbd98f088ba402782f18de8be3633f79a1fe2b1d89d7f663`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 15.9 KB (15948 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a23f9e63f0b48db5fe5bce0620532a251a8102c194b089811d2c0971c5bca7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226476529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7a6de794f8de9a83729ddc069c54ca279897fa8f480784e03c972dcf2a8363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:29:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:29:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:29:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:29:24 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:29:24 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:31:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:31:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:31:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:31:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:31:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b45323254ce3bd87b7d048e00f69b36859e12f3173f4f96cdebb3ea0b71fbc`  
		Last Modified: Fri, 15 May 2026 21:31:00 GMT  
		Size: 90.5 MB (90536948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa073431e5895dd3ea1a546bb6e46d3f1749909c8a6c6989ade91e280ca073`  
		Last Modified: Fri, 15 May 2026 21:32:32 GMT  
		Size: 86.6 MB (86566231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52013599350517609da6dfb50baf2617faec67b1977ee0a8a7ad9397b1e13b5c`  
		Last Modified: Fri, 15 May 2026 21:32:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c60f353f08b98c932a1ac09f5ecd02f1a43baecc5e7c2ea06339c1ade2628b1`  
		Last Modified: Fri, 15 May 2026 21:32:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:abcb36b6b54fc7e89cf1f073167ba1cb9bbc338c593aef3040aa2b50facf7236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805e35710e908b3d4304b00ee19e7796f68cfb9b067a27fc79fc1fc855312f36`

```dockerfile
```

-	Layers:
	-	`sha256:54a42308ec6dfc6a325043281158e28cc986e8824003808f12af7269332f8013`  
		Last Modified: Fri, 15 May 2026 21:32:31 GMT  
		Size: 7.4 MB (7417381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e24a3621e40a06eefa44950264c7968a9f78c778ef787d7b064b40d3ca88c6`  
		Last Modified: Fri, 15 May 2026 21:32:29 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
