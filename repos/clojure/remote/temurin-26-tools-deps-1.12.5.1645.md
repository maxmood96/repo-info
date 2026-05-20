## `clojure:temurin-26-tools-deps-1.12.5.1645`

```console
$ docker pull clojure@sha256:eda042c0f904a1133d4b55ff91990c8d9639b9e7265f2c2ad964b8ea18700a16
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

### `clojure:temurin-26-tools-deps-1.12.5.1645` - linux; amd64

```console
$ docker pull clojure@sha256:2a8912d82bd5527cd68193ddcb3e3d83c68f8a3f2c5e45ebec8957dba6459ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224233515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dd71c77241b28d6dd9bcb668a799d9cc91962fdef92f9614e987852459df63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:17 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:02:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:02:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a49998aec6b2dfbf350d5124f25cfa4b7f7cdcd1fd78a2c358a9c0f1ea27fe9`  
		Last Modified: Wed, 20 May 2026 00:02:56 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301f8419e84be164242ecb71bc5abf9c4ac51c17340184a9983488e305d955e8`  
		Last Modified: Wed, 20 May 2026 00:02:56 GMT  
		Size: 81.2 MB (81212701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c801a9a45a630925dfe8a78f59629ab0f856e958aad54327b3d5fa70d8aec313`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9825abfd115287f7b1615aa6c55912abcb96e7de43e5f6130e6f0b6a7e8cad4c`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645` - unknown; unknown

```console
$ docker pull clojure@sha256:c17ea380dacb75a884bf6c5de058cfe575f1315cc685bfde7ca09734ea322028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7361133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b5e313dea80ec0b3c01b96e1c2b8890592985add812a99784d9233203eefe7`

```dockerfile
```

-	Layers:
	-	`sha256:e477cfca1308f1a113040b6d63a78bdc174fd7584a5e89da30c74310e76abfd6`  
		Last Modified: Wed, 20 May 2026 00:02:53 GMT  
		Size: 7.3 MB (7344524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b389bd71f1e26c5ba76f775ab96120915f1a5fdb8666f60df3af9c6ecf36a97`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3dfbff2624e5ab99474c2d0ca8d99c154d95652a9cc040924dbc3ac0ddeaa0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223098446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4041a1eabc788474b1b4412b9a04bcadf0724c8c980f08de4cc4fc140e39be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:09:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:01 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0336c35f973a9813043cc07ecc68d7b9451d2785d0126e459a1289829b406`  
		Last Modified: Wed, 20 May 2026 00:09:39 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d957823114ed7d51944d808bb829919b37e4c517bc34014e814ae7e23c2c1d3`  
		Last Modified: Wed, 20 May 2026 00:09:38 GMT  
		Size: 81.2 MB (81213624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ed67fc38028691506356d8846a50415d82dba076e4e278d458d2ad8ec1f99e`  
		Last Modified: Wed, 20 May 2026 00:09:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8c9eb5ff49008593d68012c8e0b32aeded44c876e0ba8739fbbde899525609`  
		Last Modified: Wed, 20 May 2026 00:09:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645` - unknown; unknown

```console
$ docker pull clojure@sha256:4910f1dbf19aa596124f3065168ef5fb5d9c51500500b5e42231ec8a9ad9e24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2209e12bc1c2208061831c5b14e86754045c9c00fcb1e1b12ba6b8b161dc8f3`

```dockerfile
```

-	Layers:
	-	`sha256:b23b5c4f2486649bf8b14f6686cf23b24f08824f4f73554986dd267458a72769`  
		Last Modified: Wed, 20 May 2026 00:09:35 GMT  
		Size: 7.4 MB (7350308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd0c7e7feec5ddaef3983c1c5fb1f303243e3c1dca9f59a8dd0904a64c9ea4d`  
		Last Modified: Wed, 20 May 2026 00:09:34 GMT  
		Size: 16.8 KB (16751 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645` - linux; ppc64le

```console
$ docker pull clojure@sha256:ddd5ea300dec64fdd77d1742cbb1af7a11410e99c1f9283c2d7d59059550babf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233290287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a9aa336ff421e8e8a5f44a5c1199f116c935a018d010c509a2f8f90784d7c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:10:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:10:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:10:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:10:17 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 06:10:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:13:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:13:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:13:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:13:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:13:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a250708f248a2296e18311b56818c5d5e6477c5552cb0d7df7a8d16b02343c`  
		Last Modified: Wed, 20 May 2026 06:11:23 GMT  
		Size: 93.9 MB (93902016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb75803b5376ffed5a5f8f683c7bda29bd8b3d49146443c9d11096f820bcd94`  
		Last Modified: Wed, 20 May 2026 06:14:12 GMT  
		Size: 87.0 MB (87047030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94afdbc305c7d164680e3b96a1fd55723f157ffed9029ad078faf06cf44caebe`  
		Last Modified: Wed, 20 May 2026 06:14:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20cb7496e58fda0de57ecfcc6b4af2ca57f516f0e4dd1edd4940a204d5d58f`  
		Last Modified: Wed, 20 May 2026 06:14:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645` - unknown; unknown

```console
$ docker pull clojure@sha256:0611f80475c2fd81c515859c41d7bb2ea49211f47aef8e73458243a005fb709c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e32df75eccc7542db7330d196c891a4dbb832b7b80fc5036b9eb5b78efccba1`

```dockerfile
```

-	Layers:
	-	`sha256:1c6c7d28db2d6077ff4db34207ccdec65383d7d6c329e854c77435a6a29038ba`  
		Last Modified: Wed, 20 May 2026 06:14:09 GMT  
		Size: 7.3 MB (7333688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5628a179ed63661d07f8b030b6db8ec7bc6e58c776c74877a68655fed6b13c`  
		Last Modified: Wed, 20 May 2026 06:14:09 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645` - linux; s390x

```console
$ docker pull clojure@sha256:eb224cef27a4463caeb546f28d0e9f7efee789d06d52197f9287224f32a6ea3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217719687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd9dfe5e345285352790895484a18de386a2a38eec73f43b0f4091f0a7a3bbe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:48:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:48:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:48:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:48:54 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:48:54 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:50:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:50:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:50:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:50:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:50:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9ae4ae0ae9e5f83ec5cdac2d66779f72a32acf5bd578b66847f1d4b88f484d`  
		Last Modified: Wed, 20 May 2026 01:49:33 GMT  
		Size: 90.5 MB (90536967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1cc62c0af89cd95129e3043c893fc3fb2b3817cee81a00d4745a3d3b3f34d8`  
		Last Modified: Wed, 20 May 2026 01:50:29 GMT  
		Size: 80.0 MB (80026091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8896f9ba639486ea937b26794c9218479b6b26d2915421b6f7d7719c7ddded33`  
		Last Modified: Wed, 20 May 2026 01:50:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8014d4901963d868a34bd62e0c819dd161c50f20c9e1760b307a5eec1360b5`  
		Last Modified: Wed, 20 May 2026 01:50:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645` - unknown; unknown

```console
$ docker pull clojure@sha256:4a0b0cd794884c3ea832e453f423a4cb5c8fe5e50481067658cd4c65a76ad9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7337638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a532a0cabb5e03439f8a0f323175c4d2b6f3eb8e4cf0b651f535554087d81eb6`

```dockerfile
```

-	Layers:
	-	`sha256:6f1674428f256a9a4504a29de4d41a2ade9135338323d4f83d62f44bb1c2f9fc`  
		Last Modified: Wed, 20 May 2026 01:50:27 GMT  
		Size: 7.3 MB (7321029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b550fef61c733047f57815c68e3ae1617144a08d797c7d300d53a266d12143`  
		Last Modified: Wed, 20 May 2026 01:50:27 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
