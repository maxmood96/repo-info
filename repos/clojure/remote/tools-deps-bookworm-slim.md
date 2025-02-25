## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:297305d1cc8e81c4843c6a92b900ee6c080447c76729385227e54e7aacf3e46e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7033036953431abdc2286a2b208accc24805ae3e8daf7044409ad0e8130bc42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255336022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a17e3239b64a7ca336e886653184180378beca55475dcd128c06053d83e6ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1b893aeae12e7e0e13e0dce43f3f67c97cfbff10ffe22132678a5362df36c0`  
		Last Modified: Tue, 25 Feb 2025 02:34:13 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf57137c306279d421f5d134c05f6ae0054125eb87774443f40ffb35271fe3`  
		Last Modified: Tue, 25 Feb 2025 02:34:10 GMT  
		Size: 69.5 MB (69529792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7fcb26c0d5a74c652c691a0cebf4fc0fdab4e29417e8b8978e10b224fa380`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05117f64d837d11aed1434bb403be814d730a4618dddc63661e2b8e02297ff2`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64d61b86ad39a42420b88a797c3448e19186e52c08ef5ce2a12d8772e519a1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094171322685736558b7faa57611a653c22e35af246aa8d7f246537dd536d2e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a1ce544136d1c71702dac2233a17ba83860eeb526c9c6f1700bae22b1bf9261`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 4.9 MB (4916383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214a14ea97c3c0342bbd703c43a553896db481c9eed3d1bce9432fcc09b4efc0`  
		Last Modified: Tue, 25 Feb 2025 02:34:08 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d8b1a6a579614a0420e4ed4c4da63073e8b1af49a2b0f0e31ffaac4a867efc9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253288497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cddb7c92613db950b086e43bd6affb3ffd7b1e6d404ae24a10663ce64cb042`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2420f1607bca7565603bf512cf5e72b26b8879ff87c67a156cb4955275a1edd1`  
		Last Modified: Tue, 25 Feb 2025 11:09:35 GMT  
		Size: 155.9 MB (155859298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8f0e36b4b0978f62cfcda771a17d73ca0d1b31ad3d382203e21b4aedfa2193`  
		Last Modified: Tue, 25 Feb 2025 11:12:48 GMT  
		Size: 69.4 MB (69379733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbe92e00f4eeaa58d431b7136441cdda5de44a84d0d8bb159192281c998899`  
		Last Modified: Tue, 25 Feb 2025 11:12:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39a6ba574028b85efda64f307e6f32036eba33d4bf2f3e16566f2a5b69d1970`  
		Last Modified: Tue, 25 Feb 2025 11:12:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a352a345464c580193be6ade4827c9487f6015d5c801d05c1199f16da7cd504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac25b5e8f410fff7b0b840fdfa92994ed9fd876c77984bfcf8529dc4ec91e688`

```dockerfile
```

-	Layers:
	-	`sha256:871ab62937d4d8a4a7dead3e1d834b1d0b0c21f9bef3a584375768eebda22e77`  
		Last Modified: Tue, 25 Feb 2025 11:12:46 GMT  
		Size: 4.9 MB (4922168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab166463fafe57e978f2bd152675cd6bc4447745909a65a64cb02465ee7beba`  
		Last Modified: Tue, 25 Feb 2025 11:12:45 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
