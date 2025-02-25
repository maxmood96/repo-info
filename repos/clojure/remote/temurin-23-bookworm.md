## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:20b6d9a2c7f9ad88f079fa08c5889ad741fd7ca395802c6ff1cb15786dd7d275
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:403dbc47b5cc6a8042369e76aa63601dfa3e7a0ca7ee4491707b0409e777031c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294787964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8b4bef92f3bb1296a634267b6b8fe34bda0aad5499c15d341bd62c324b9cfa`
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cefa413a2be5389c07916b405f2b20c7094c64878cf52f2888e8c66977d7b77`  
		Last Modified: Tue, 25 Feb 2025 02:35:41 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3b722f23b99f4542ded4b142d9b5dc58cc87266d1e68b99b9c538b3738e321`  
		Last Modified: Tue, 25 Feb 2025 02:35:40 GMT  
		Size: 81.0 MB (80994594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d082d444a2d8507ec97a363851045cb7c6dab98abdc31be5944f1f327f273c`  
		Last Modified: Tue, 25 Feb 2025 02:35:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34770cfd853db3c8159845b5e60909d2f5fee3300196d7a204f95eaf698c02fb`  
		Last Modified: Tue, 25 Feb 2025 02:35:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ff588083b914152562f6cb1ac8270cdaa8bae84adb10ecb53c6fcf02a10c1b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a99e1ce5de3de8709452dc982128aaa9d8f55a0fc5d00a6aa3159e5ee5a176c`

```dockerfile
```

-	Layers:
	-	`sha256:34dcbfebf03a3baa466d8e9f2216b2c4dc0d704ba1e2dff46657d6d4e743681b`  
		Last Modified: Tue, 25 Feb 2025 02:35:39 GMT  
		Size: 7.2 MB (7176785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4234a4cc461a23db1030cc98636174b071da07e519f652112ebdf7af6d3e4f`  
		Last Modified: Tue, 25 Feb 2025 02:35:38 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5865a198d0f6badf56a9a55836ac6e54f0a1a41c03dbe76754f18c232f3c605b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292493317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1492bd3a9990dd2b458bd0a8441494392901d887cf1bee6547ea110345e28821`
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca50648c20ef7fd0a5ed1545a1006f88f616c5a3affb90331185a9a998f1dce`  
		Last Modified: Wed, 05 Feb 2025 00:04:35 GMT  
		Size: 163.3 MB (163341440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cffe8cde004092a2753d36dd9d001cf3c1c6aec8449147a42684ed195d3b8b`  
		Last Modified: Thu, 20 Feb 2025 04:00:46 GMT  
		Size: 80.8 MB (80844285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e9de1220290c529ba404cd6797fc3af10ae262e23b49a5ee7de0147f9ff9fc`  
		Last Modified: Thu, 20 Feb 2025 04:00:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf72135009559319df3db97e4eedbaba11338eae33218cfba824cf01ad5bcda5`  
		Last Modified: Thu, 20 Feb 2025 04:00:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:20e24d5a0b08d2351e6d8830fc4fbf41f12c522755122109c40f58b60d8eeb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12332d93392e9fed6851fee57c679d3c5ccfbf0d15498d2c6a1aade472aad5a`

```dockerfile
```

-	Layers:
	-	`sha256:4409c998b40bacc3d64a76b9586204beb6cdf370e9afd86420d26372702753ac`  
		Last Modified: Thu, 20 Feb 2025 04:00:44 GMT  
		Size: 7.2 MB (7181933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c50f7ee75c2229a41931abc02a7378d3f1b1d6315f84c2b81a721e7fdba7ca`  
		Last Modified: Thu, 20 Feb 2025 04:00:43 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
