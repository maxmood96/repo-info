## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:4ae155e88be7560195d5ff14d2f7ccf254aa5efd94b3e89ab40a7a9e035cbb24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8ded3800e937d3556cedc83f0c0f8993ef28e059a79ba07f33689260374600c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282757664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cdf6368a538b13b26015bdd0362f2151e85b164344e9c486ce43577481c38d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723fd207d76d9d11da2093fb7602ee0afb1686ecc9858b2e62c0b50f77d55e57`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 158.6 MB (158579294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a60b2887795d8dcdfa862bf0383a9aa784a9110434b6528948862ec53357c1`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 69.1 MB (69095998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6559f6fb6526301626f059f6f26ed6cffd309237e01a7d4c107dba61b0addb`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0881765befae62a49a5bee9a06103f4f9afff0cc2db9b56fdd46ee902103c5`  
		Last Modified: Wed, 04 Sep 2024 23:07:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d0da2523eb7c0dddb45a6d6279b8049ecc80bc219b57b2c2189b05a98b1433c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788c38b38ab73832a308de135fd3ea914529a819534169b167126be1a696ddbf`

```dockerfile
```

-	Layers:
	-	`sha256:daa934f4410362ecaf827bd685c938f81b5010a1a3128cfb5e01ec23b8046d56`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 7.0 MB (7041030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bda7af15826f7bfa79745d9ee092730b929a6cf7283a6de0a62611b83f09e30`  
		Last Modified: Wed, 04 Sep 2024 23:07:56 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0cc108fb2ef9a25cc87a6fbbeb9c5279078a94708b0bc52da450b4bc2c95ff30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279570130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18de1b69dac0710217aeced368973d89161e8a8752c5b25e74f5453f911fb5cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6abbac4e39392b14f19d30958c95b49a4311cd8c0068291c0df9b77f1896d4`  
		Last Modified: Sat, 17 Aug 2024 06:23:00 GMT  
		Size: 156.7 MB (156746151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dc2a944fad80339894fadec5d7cf36570215e34659a6ce662332c630ed1b20`  
		Last Modified: Sat, 17 Aug 2024 06:29:20 GMT  
		Size: 69.1 MB (69093015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ce23d7b2f690c10578d98242059323a9b9525ee59b319290cb240fd0d69114`  
		Last Modified: Sat, 17 Aug 2024 06:29:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398330a1cb5a5337910c8067ad434ce1f7cb139fd3a2630607e6613ce6d28ca7`  
		Last Modified: Sat, 17 Aug 2024 06:29:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dacdc25e75d8294436fbf602b9da857027df8f404c6ab7b694d8c958505695f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7063452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7038e4806d587e1a8639c7ed8ec02c66df8560425a615bf9bb057ca960ca5`

```dockerfile
```

-	Layers:
	-	`sha256:f61ce7d34e8acb571406d01dd257a8e953ff303ef221fa21200324f4a83e5e4b`  
		Last Modified: Sat, 24 Aug 2024 00:07:28 GMT  
		Size: 7.0 MB (7046776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e70177d249ecf30fe647a12286e1ca505e6fcb6945e4ffbdb32a80274a2b29`  
		Last Modified: Sat, 24 Aug 2024 00:07:27 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json
