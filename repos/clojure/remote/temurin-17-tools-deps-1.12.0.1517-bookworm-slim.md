## `clojure:temurin-17-tools-deps-1.12.0.1517-bookworm-slim`

```console
$ docker pull clojure@sha256:799f0642205d7ac50ab57e137ee22aacdb8747fd1cee0fe05262fd7da3ee4eaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1517-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4774f77db2030a8166fd7bcfbf674e842ca19b757ecf99785f439547bbdf654a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242310275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cde30c16fa68d664e2457eee535f34fdaa33568e70cc4676a01004bde44f127`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cebf0cc08fe484ceefb09f1bcda13737b9dfff5a3cc95a55457fb8c4b18c722`  
		Last Modified: Thu, 20 Feb 2025 02:30:53 GMT  
		Size: 144.6 MB (144566523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3ff67bfabb68b9141890e41db06aa05ac2b9f51c32c4eed4ba85532159a544`  
		Last Modified: Thu, 20 Feb 2025 02:30:51 GMT  
		Size: 69.5 MB (69530408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c49dbf3e15feec02b8f9405ab65a50ceec4cc2cd24e2458b2033ba5099bf3d7`  
		Last Modified: Thu, 20 Feb 2025 02:30:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7852d6fe1cf48ad7315cf7edfa59f1c5c721606efcec64097b7c172fd5486d0`  
		Last Modified: Thu, 20 Feb 2025 02:30:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce0d5c1ea9639fb82627968a0ebb2695e1dff19fc5aea60a4213c8411572f4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611425c32b217d859b9abe1ad22345c6b773e32119e143c72acf1cb3aaee815a`

```dockerfile
```

-	Layers:
	-	`sha256:9653f84862e8f1f1b07554726ae8b648f6303df2b13d9d857700db4d3bafe7b1`  
		Last Modified: Thu, 20 Feb 2025 02:30:49 GMT  
		Size: 4.9 MB (4912567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076d7303e3b746d77994ce2c9c33990eb142d8d7ec0bfaf771ccb45dd7d71806`  
		Last Modified: Thu, 20 Feb 2025 02:30:49 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1517-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:357200bf4d5f1bee71542e0a717ea097438fb33544d36f6cecd45b528c8cd1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240875823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f98419e8bf7d683de1af94334011644aa883f345f5a6d4102230d287fea2a2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae012ff89092306c93163c5501638b4e1ea553e25181d4997dd7d40d4e9812`  
		Last Modified: Tue, 04 Feb 2025 23:43:37 GMT  
		Size: 143.5 MB (143454713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b1c679d5832c6d1e337091f8afa07a4bf9c8c671ef00239c9b57df443d4c0`  
		Last Modified: Thu, 20 Feb 2025 03:52:20 GMT  
		Size: 69.4 MB (69379190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8432733fee2264253931c5fb978fc791428416c34bc6876d8ccacc5a21aba38`  
		Last Modified: Thu, 20 Feb 2025 03:52:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2e45b26206972a3fb49a62187b9b595ba3fa46498a18a595ef5731651e30b6`  
		Last Modified: Thu, 20 Feb 2025 03:52:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8eecbdd1cd4cb2d9da3b503d7756abe07cee9762467f6c8ad203a4df6aef7592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d304cdb797c339b215f32b78be591a044b7baad2f6fb88a87a79f07dc1daaea`

```dockerfile
```

-	Layers:
	-	`sha256:c13f78f6ac90e898bc4f6209776aee2b1830727e1bc4d4b01dee8ccc6600c886`  
		Last Modified: Thu, 20 Feb 2025 03:52:18 GMT  
		Size: 4.9 MB (4918328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0a944938ee701ec25f412a5a6e1a085e66ef587575cb124850ccbf11f7b558`  
		Last Modified: Thu, 20 Feb 2025 03:52:17 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
