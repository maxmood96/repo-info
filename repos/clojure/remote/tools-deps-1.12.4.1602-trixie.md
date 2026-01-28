## `clojure:tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:082da86f82384eb1e5394020d41ecd1dde100a1a8aa259a8868e8ac5e091615a
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

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f3e0f4dcf93dff99a48a91d2b424147e50d102aa23a1d7cff10901c32f1a5911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229845738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab0b8161a48826237b883784b37e0f167f3b0876f845e715b997fdb26ff4ea8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:06:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:54 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:07:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:07:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:07:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:07:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:07:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6ae30583177540274b33c5a22fcac9def1582fa370782550b8e44801ebdef3`  
		Last Modified: Wed, 28 Jan 2026 18:07:36 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ddc72f5e61e21a0b37a4bb24595506885e563e9d45c4f6b01c59c9c213f868`  
		Last Modified: Wed, 28 Jan 2026 18:07:36 GMT  
		Size: 88.5 MB (88513762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45666c56f8a4a32bc3754fc460ddc280cb4ef34e7ab7610f6ddfa983a0c7dcb3`  
		Last Modified: Wed, 28 Jan 2026 18:07:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986a97f36ed69b0430f75cf0cb515fc37869838ea9b458563c73b563c5e83816`  
		Last Modified: Wed, 28 Jan 2026 18:07:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d75b6cc44c34b7f8bd1cb45bd3c85757632bd1a596e7a2680eb7ca137b897fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569dc57ca946d8e4b7500c95a2200ff07435b407addb3b79c45280996184f648`

```dockerfile
```

-	Layers:
	-	`sha256:953f37f790760c818fc044f19aa96b1781d84e2edeb147603dfb8b799a89d8c6`  
		Last Modified: Wed, 28 Jan 2026 18:07:32 GMT  
		Size: 7.4 MB (7419158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf9acb31135d17dd027d39f072596cc2e76ca82fc7307460fb7685abbf34869`  
		Last Modified: Wed, 28 Jan 2026 18:07:32 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a100dd720c812de2d0cdfb4aa51176a6cd04ce54d58a3b45eb259f0d29c4ed02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229394126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863049a082f0f9e265a24b782f72af77ad592934041a3dfae1f65d9a366711eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:06:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:51 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:07:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:07:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:07:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:07:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:07:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db7196f98befad24d66ed880f42f91d4e72d702c989c9ec0acb6a6963379ba2`  
		Last Modified: Wed, 28 Jan 2026 18:07:35 GMT  
		Size: 91.1 MB (91052475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a8432c46d287604b94989129dc91935b2a19bcb185c590832549f62c9d895d`  
		Last Modified: Wed, 28 Jan 2026 18:07:35 GMT  
		Size: 88.7 MB (88692527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a80b31590ce77c81ca33f8636680cf9dfe9f6d65da7c7a165774ecc91be53f`  
		Last Modified: Wed, 28 Jan 2026 18:07:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a819a0c9f7754e95bdbfaa2a34b44a20a07bb2a161baccb9fe24504593a425`  
		Last Modified: Wed, 28 Jan 2026 18:07:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ab72363482f0ed6aad046ec00cadfe9aac01c144808e5fb6b6aa5d29619cbaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c503578b3745bd38fa6cb55a8be819dba5fb502f3d13446f1e184f88f31de08c`

```dockerfile
```

-	Layers:
	-	`sha256:02058a76e04580d3274958526a55bbfed4c41ae72ecb9003af8d97981a0bd7b8`  
		Last Modified: Wed, 28 Jan 2026 18:07:29 GMT  
		Size: 7.4 MB (7426209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654ff68d1059dc9549753e9a85ae14371eeab5f67eb94fc47604b29a42948bbc`  
		Last Modified: Wed, 28 Jan 2026 18:07:28 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:542e6971a294ab96da65310f9617230bd47d3b82fe0005b1964fc30ae23cb525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238871482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972004051a8ccd91e0ea9863b7584f26e7d38b3e5626137839d7f865c3d2132f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:34:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:34:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:34:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:34:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:34:47 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:35:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:35:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:35:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:35:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:35:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d07c497bd75fc89d2238aa81fe87c347efb3342db98ae486cea553fd599cf8b`  
		Last Modified: Wed, 28 Jan 2026 18:36:21 GMT  
		Size: 91.6 MB (91610775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97040e523354f65c91e7851c630ab30fc7f96c45902880237895f4be74251e8`  
		Last Modified: Wed, 28 Jan 2026 18:36:22 GMT  
		Size: 94.2 MB (94152703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9b57a763cbb47569d5995ec37764e7c8f24e15bb21559ad6d883d2b51879f2`  
		Last Modified: Wed, 28 Jan 2026 18:36:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f5245d1932f792b90cb002e21bd90e55cee609e3c5cc61c695beb39564805f`  
		Last Modified: Wed, 28 Jan 2026 18:36:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:478049231d8589b3c7bccc8fabfb371dc97f21ea30bc6647b48b872136ae732d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87753e952178ac8e8b1cef7062f5fb779945e1a8d88df7fb8692837d77c9e92`

```dockerfile
```

-	Layers:
	-	`sha256:61addbe810066550148af6073cd159602d451f06ee22b1f11e4008f51680228d`  
		Last Modified: Wed, 28 Jan 2026 18:36:18 GMT  
		Size: 7.4 MB (7424889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6197267b8c83db073080e560c392ae13331af25d4cec645db86936c5279533f`  
		Last Modified: Wed, 28 Jan 2026 18:36:17 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:7b66122adda839e662c78f9c3614aa3a518ed0b2cc72415a8a66607a08fe8ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226692409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767162daf50a85b3d9e20316e6b76f980089976e1014fbabab5d85af4578fc42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:22:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:22:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:22:58 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:15:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:15:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:15:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:15:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:15:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9da15375349ed468c4d395178dea5e2fe711fa01064413f4605f3f47af67086`  
		Last Modified: Thu, 15 Jan 2026 23:23:38 GMT  
		Size: 88.2 MB (88210648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283739385404e1e9d3f947009d347cabc4ab66a0d8f775c46beb03049ded5672`  
		Last Modified: Wed, 28 Jan 2026 18:16:05 GMT  
		Size: 89.1 MB (89132016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee869e3e711176514b9b3da9b87971f01377026ce72ccc73701e19f5d4dc3fe2`  
		Last Modified: Wed, 28 Jan 2026 18:16:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e009ef584d1eb076071d60b9de23ea12ecf96662e3de45c5433eb7ff042b364`  
		Last Modified: Wed, 28 Jan 2026 18:16:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:52caa6453b16bc53e40063bc50b31166b25e7e463eff4d09b941c85d72506026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282333136215b5f38a043a010947b08980e0add6f9b2b003ea52d6b96a27dbfa`

```dockerfile
```

-	Layers:
	-	`sha256:178f4ffa1ff22be9e68b1aa3dee7c7eb6f959574f3c59e2d66d0f509f96bd6d1`  
		Last Modified: Wed, 28 Jan 2026 18:16:04 GMT  
		Size: 7.4 MB (7417628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa52e7243ccb6ae4ec6da252eb902f973fd9603c4338a51ac6c28a144b54657`  
		Last Modified: Wed, 28 Jan 2026 18:16:04 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
