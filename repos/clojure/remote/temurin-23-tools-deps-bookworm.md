## `clojure:temurin-23-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:b80fe7668106a0c616694532121b01c0bb3ce1578e6b89f7ee7c46bd741f55ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-23-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b152f86fe360ad05363a88571a5e852b1dc8a10841b1e47746e26676b09b5dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292494574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e07872f099d3acfd05584a4f1f89d314f421e6cd68cbb66c84fd28dfc0184`
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb1a0aa6b8da1a00cade98021d7314a3543e3f5baa14065fff895b71946068c`  
		Last Modified: Tue, 25 Feb 2025 11:15:14 GMT  
		Size: 163.3 MB (163341428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96676736872451e1c3410ef4a9b1825ac9e897443b2d81fa7244d1e7f2cef227`  
		Last Modified: Tue, 25 Feb 2025 11:18:55 GMT  
		Size: 80.8 MB (80844095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f41e1ce17acd8ef90b0d53d8845c7a2237736c83ae074a4db5670d8e7cc7e0`  
		Last Modified: Tue, 25 Feb 2025 11:18:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86be6969296dcbcaa3a86eab1bd21070a4b3cc584b8c448d34b7adba89d9808`  
		Last Modified: Tue, 25 Feb 2025 11:18:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:478260570e0baf6130e44dbf22319b2b189883b35c3301f4135ebfa3e305fe8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de990364d65c66d959b37de1ec18ff54dc7cccd7a304959d1619f59c56173f9c`

```dockerfile
```

-	Layers:
	-	`sha256:cd7286e89c5530eaea0b2a4953eeb46c234b41230c1fa100a663abf7555cef4f`  
		Last Modified: Tue, 25 Feb 2025 11:18:53 GMT  
		Size: 7.2 MB (7181951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07c825d1b381a3cbfb59effd33c06ce76a931a20b844fee566938ce086d45bf`  
		Last Modified: Tue, 25 Feb 2025 11:18:52 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
