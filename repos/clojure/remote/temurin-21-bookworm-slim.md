## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:c8314dfc94741375d1755e1de691c56d2e8923e0bc5478c59afacbb17646fc74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm-slim` - linux; amd64

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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:691bbeb1fe08d22fe9a24ee9bc02eb1c6d9dcbacca4e84eabcf05c24a7e84b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254467382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248aabf98bfe194631bb09490ad18d8477402821204cb91313edd15c703a9562`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c24c7a7b86f218dc61de558ffed50d5992f39df50505edf3204888486fe1b7`  
		Last Modified: Thu, 13 Jun 2024 11:53:39 GMT  
		Size: 156.7 MB (156665644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667d36716db6c32e5f608164829802c2dc048523eda4bc4f0af2899619d84594`  
		Last Modified: Thu, 13 Jun 2024 11:57:09 GMT  
		Size: 68.6 MB (68621026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60498181569edc615de2d1c4626403a3ec8ed0cab14a131cad534b5d7364fba6`  
		Last Modified: Thu, 13 Jun 2024 11:57:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a7e46124952c8db9a98ef9e91226fa9e944fa42a779de0809a939ba096f65`  
		Last Modified: Thu, 13 Jun 2024 11:57:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1445b83c40196ef621824131adecda830e1512e67c2e1c233dae9cd203640051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4728826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fb172c404377bb3684ddd14d39ff6c9e3027a5b2522b1a13182a6059d94e24`

```dockerfile
```

-	Layers:
	-	`sha256:ca029339e69991fc53edf5a195153cb6612f0ac7a66ac1e2c0244319e59d547f`  
		Last Modified: Thu, 13 Jun 2024 11:57:05 GMT  
		Size: 4.7 MB (4712053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f730c868e53d4290bd69157576f10970c072dca956df3a1dfa30fae07266cbb`  
		Last Modified: Thu, 13 Jun 2024 11:57:04 GMT  
		Size: 16.8 KB (16773 bytes)  
		MIME: application/vnd.in-toto+json
