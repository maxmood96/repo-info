## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d45206c61f594a81226f318f00eb1782296e7340d6d2d4dd6b27a236cb76bef2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8cf133625a56507b98b642366eb35333d356b86b8b4e5bd65704b9f5b7f42958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256517790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3710a434dccc7790f66f77be8db4cb44b08b64ceb588a3c5a59bec4ec162e27d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f813acd019188d826cfa0eb82e35b5e72840acd9944bdccf1102f36de2ce0a`  
		Last Modified: Wed, 05 Jun 2024 06:10:44 GMT  
		Size: 158.5 MB (158497970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f814f66f4c00fafe6f0508abec50956864fa519620718673a44eaf729f95b06`  
		Last Modified: Wed, 05 Jun 2024 06:10:42 GMT  
		Size: 68.9 MB (68868360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca2f7e335e919e4dc94eec3f1fe1c701dedd8fdd88a6933c9c3f940184361b0`  
		Last Modified: Wed, 05 Jun 2024 06:10:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8773e62b1addb13326534627f715eadb46e6a49f2c8d43418c85131f47e155d9`  
		Last Modified: Wed, 05 Jun 2024 06:10:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b848b487ae2bd08cfaaa78045dcc86da4b90097b3b682c7cf8428fd3de877c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b835e4061b7e6abd6369f3c36443576c5069023c0fb12e09bf499efd5ce6af0c`

```dockerfile
```

-	Layers:
	-	`sha256:6cbdc1a6245febebbcda480df2e8b3f9971e9cbb617c5b54a77d27f4edf28751`  
		Last Modified: Wed, 05 Jun 2024 06:10:40 GMT  
		Size: 4.7 MB (4705644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16c356440a9299a02281824aa48dd1994610babb56cb9065f09686b0f23f43f`  
		Last Modified: Wed, 05 Jun 2024 06:10:39 GMT  
		Size: 16.2 KB (16158 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cbe5d6d2f09fb1c0e632b92b82554e7e8e5f46980a08f74d89a328986587671e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254466554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8b413996f743519e3f219161c4769fe666f3aa59647e5bee0695ce4ccabf50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf8b9f24d5c5ebeda01a43eb33bba3c652043c50f7de508353d27b1c4162fd6`  
		Last Modified: Wed, 05 Jun 2024 14:12:34 GMT  
		Size: 156.7 MB (156665623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9382ea3dfdc4f18c1899e815ebbb10c70bd17e3d612be0fb2b31567acae398e4`  
		Last Modified: Wed, 05 Jun 2024 14:16:32 GMT  
		Size: 68.6 MB (68620379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee01ad8ef2bf517576ee0462a9047f4ece2b9a6ee9f205c83d44f7fe330a059`  
		Last Modified: Wed, 05 Jun 2024 14:16:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e30e39770475a20f06d91d863394595ac2b9097b22a609ad12fd1678b6912f3`  
		Last Modified: Wed, 05 Jun 2024 14:16:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c54510c6fbc0b01d067a8e25f3ea7311f5cc390113c19671e94f636a5cf7e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4728777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c31d370c832f50ab9baeb59523dcbed231ebb690ef79359507769a2870d318`

```dockerfile
```

-	Layers:
	-	`sha256:24bae956e5f2899c8d1adef3aad9a9d24144703584e1a266831fc67f3ce8fa38`  
		Last Modified: Wed, 05 Jun 2024 14:16:29 GMT  
		Size: 4.7 MB (4712053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6bfed87ad3f349a7b93dedf4c8bfb39e9c864d7f7d35177eb788d305d517e7`  
		Last Modified: Wed, 05 Jun 2024 14:16:29 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json
