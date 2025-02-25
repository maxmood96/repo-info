## `clojure:tools-deps-1.12.0.1517-bullseye-slim`

```console
$ docker pull clojure@sha256:b0fde931b7a717b61e70a68e746f8021f2970ccaf45164229936ae0cd4d66712
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1517-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:11094b5c34bf50354f2f81a0d24eb637c6e0c8658c19bb2d4f227ad0e8799cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246629262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec7c317f02735262e1af81ac660ec5109bb9fb66ed324041dab6687a13637c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310a2daa88b0594249a436f905b2ef292416cd95af8548d6fdb35b8cdc42a3ca`  
		Last Modified: Tue, 25 Feb 2025 03:22:23 GMT  
		Size: 157.6 MB (157585931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548f49cec502e2523e9d693caa40ffb8e2ed3091fa56738c1145cde20f8ca1b9`  
		Last Modified: Tue, 25 Feb 2025 03:22:22 GMT  
		Size: 58.8 MB (58788360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bbfad3a06c70f514481c14b1ffd6f3eb51ed4862d415171511a3ac7ffb66f6`  
		Last Modified: Tue, 25 Feb 2025 03:22:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f21c4ca13ac5cb4e0933e942cbef98be68136fc85804a1c9202be933a61a49`  
		Last Modified: Tue, 25 Feb 2025 03:22:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b06df197603f081169ebf7cb9adb90782cc3a0666bd029a1de97f4fc0e6f1c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54fd2bfb3ecd294166d26690882c0cc54bc5a405740c38a9251e7895a33309a0`

```dockerfile
```

-	Layers:
	-	`sha256:977f682d53a866b70bc79244feead9086598a5adf17fa2cc4d122c08feca410d`  
		Last Modified: Tue, 25 Feb 2025 03:22:21 GMT  
		Size: 5.1 MB (5120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd6a745479a7aa2c00d5113fb83ff85e5713adc56db9a87d43a9c786384866a`  
		Last Modified: Tue, 25 Feb 2025 03:22:21 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1517-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d130db3139739f8deafaa38c320b7104eeb2ba3f1a176b5ef2e622afce5a9e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243515490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7207822688a02071d8e5b153243f114068f224344495812b445a9e08f59edbac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1444b3218878a3b35e8951a2bc0e44515e7eeec8e85c72e00762e9498d1e33`  
		Last Modified: Tue, 04 Feb 2025 23:54:01 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f2ca8bd76b238d052a2de2801a16ff709a5a9dc5d2c07f0ff73802163c49ee`  
		Last Modified: Thu, 20 Feb 2025 03:58:26 GMT  
		Size: 58.9 MB (58910365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc47b6bca9b9fb9b78694081aef7fa088ca4435c56d6935510c4d934981983d`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4d53ef99e12c49789e6a376526873a5cdc5224ae18f4a243560080a3fc63f0`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f80de46f8e68f01673dcbde06f0b35f95eb23b9eed1d856b006fa34283b8f975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705b9d8c6998f097dc30ec64f81ba9b74c558504611edc7d2bf33aff28be0e28`

```dockerfile
```

-	Layers:
	-	`sha256:91c743471467981ac9492370907148329fdc310434588b6eb4e346baea891cc7`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 5.1 MB (5126621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65186017cb23ae996c59d1230209afcce01cbc78b172fb7d5dc5b93116d3dff`  
		Last Modified: Thu, 20 Feb 2025 03:58:24 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
