## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:bed133712802a5bc7264036e3a079e7dd68775f6c586a5c484924b18941f3f5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:25e2009c41df98a8d09178df6cbc71413ccd1bcca533631841d732db719d2516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280784555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297d5aa7138427988a4ba9b7b97651889541f9e18dceefdce067044851eae8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbcf0121effd54c7f197f530e95e9367501fd9a9ff47ac82c28db4e50421392`  
		Last Modified: Tue, 03 Jun 2025 05:16:41 GMT  
		Size: 157.6 MB (157634492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8fdde9c15cdb20911c20df33dec0469b437f4b1f732d9c24734c198e7c4b6f`  
		Last Modified: Tue, 03 Jun 2025 05:16:40 GMT  
		Size: 69.4 MB (69398830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3d67cf92cc1926407781a36ce43f7223afd3708eac6c34ed3b740b73b99a98`  
		Last Modified: Tue, 03 Jun 2025 05:16:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461a0e5339e08b2d2ce9f102dab8ff312b4a190cbb7b62ccb7e264f8f116d719`  
		Last Modified: Tue, 03 Jun 2025 05:16:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2524ffad629077abe65204c463773150c881f376769a308d2a5f0b5dfa932ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7276461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808729494b111e1b027e670d86ab58fcb7cb100d299f10e0092cf7c031d41235`

```dockerfile
```

-	Layers:
	-	`sha256:1f3e4c55bfe6646805b2779cc087cd93e3b619589761267d8dc01e7220013e6b`  
		Last Modified: Tue, 03 Jun 2025 05:16:39 GMT  
		Size: 7.3 MB (7259964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a9dbae2fdb820afd06f2f9debd9a2746d344f7ca28daaa12e857bb7189a9a3`  
		Last Modified: Tue, 03 Jun 2025 05:16:38 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:585218be596f0b4af61f345f9f2c0c75347a07bfc58d50ba324c250043d3e976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277708448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1072e8d1b324ccdfca15284dde817dbf4d73ae17c9a05cb8718c2abdd0f94385`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e20865038b3b3ce624032e3975061a0946d41c6f1ee3d2697460ecc4305a60`  
		Last Modified: Thu, 22 May 2025 08:30:47 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005da2dec97fa7ff8f2a1305f1eea5573cd9141dd7617064381a9a43a13bca9`  
		Last Modified: Thu, 22 May 2025 08:35:40 GMT  
		Size: 69.5 MB (69530828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c455b1df422b08c9776526f62ca8a3b1c76e2628bf10aa5cc415347b346332`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cbd9c9c8fd0bfa345a1472a5b194b0ebd04bb8f89e319345c6ac2518728b84`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:46f4c808c92e5ebc22a4965400519d6c7ece4fa2603a77babfcd7eb39c5238ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7280130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ead25bd940e202c58f1ea8e62c375230b718bb9f5a843b6cf9f8e311f11bdb`

```dockerfile
```

-	Layers:
	-	`sha256:c708f13c603a7df8ee9200e4b92f683cb911c2366f959e23e146c947e1694cbd`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 7.3 MB (7263491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7d088ecf47e5478ffa11db80cb42fbcf75ea1ff81fd013a58b1d3a91a14a4e`  
		Last Modified: Thu, 22 May 2025 08:35:38 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
