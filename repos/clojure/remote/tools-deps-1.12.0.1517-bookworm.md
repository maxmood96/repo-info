## `clojure:tools-deps-1.12.0.1517-bookworm`

```console
$ docker pull clojure@sha256:5e94ad3615f45c2916e00c7fda65d74be695736c1fe7b6df7feb1efe9f50d803
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1517-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3e49004f776ed4579a1da3e7bb13d00cc54a50fd62b055558242c39887add422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287061342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5067adfffe8154d00a5b799946880d1b9308d259231010498e01f4e1cb8026`
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
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286c02107b02166964256b95773c67206861d7811f210ebd2a3c341bbbdfcc88`  
		Last Modified: Thu, 20 Feb 2025 05:15:22 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6a81ae099e61d1e00f0c1c55539f7efc973c48999d6e3b9fe28599ea5e6960`  
		Last Modified: Thu, 20 Feb 2025 02:31:30 GMT  
		Size: 81.0 MB (80994734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c41130a6884fce5d6351e831b8e786c24d06a09920b3712f6157064c981ddf`  
		Last Modified: Thu, 20 Feb 2025 02:31:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16d26d349829ae425cd52b54e9a3b9ec5a26f9eed32cde389e9b443428f1845`  
		Last Modified: Thu, 20 Feb 2025 02:31:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1517-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:702b9d626290f51feec62f271b12f19ef90e6ee273b02215cae1e10726fa7c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16155a656d55ba466e7ee121c44342326e3f4ca3e5ab475404a2749c6d4ed2f1`

```dockerfile
```

-	Layers:
	-	`sha256:4c2779b7156e340a1ec65e0512be842909168a8c4c09baecf1e2d575447a69ec`  
		Last Modified: Thu, 20 Feb 2025 04:36:42 GMT  
		Size: 7.2 MB (7176180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7abebe725c738e74ee3081f7981cd8d295267722598fd0bd9af775a05a312f4a`  
		Last Modified: Thu, 20 Feb 2025 04:36:42 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1517-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93043ab4f0653e407070a0125d317b1c7c295ca5203da7ffeacb68a7c237719a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285010895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c12551df43e3555538150d90d390358f54c14e7176be2db54e12db09db99277`
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
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5fa34edacd0f0acb63e2f1d258d50a9bfe6e1592d31c38031a099fd6fb4fd`  
		Last Modified: Wed, 05 Feb 2025 02:01:25 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db9801a2417e18573a328fe46f57d13c86b5a3d88838561ef7a5ed58554b1eb`  
		Last Modified: Thu, 20 Feb 2025 03:56:41 GMT  
		Size: 80.8 MB (80844030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a20562664a5a1b798729ec223c8944fb356c7ee0ad877b5c3e21e90737bf03`  
		Last Modified: Thu, 20 Feb 2025 03:56:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2b9cf256910cd2b82c41676a17e3135001d4f35d123f33b08d15cc12cc459`  
		Last Modified: Thu, 20 Feb 2025 03:56:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1517-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3399f03fad884025742e7ed696326ebc4344bffaf577cd6dbde09c29a6bcad44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47cc8580c70b600ecfa79d359d70b63860ee211d2207cb720e7c03e06bf1930`

```dockerfile
```

-	Layers:
	-	`sha256:a5719a50243f5138341e65f709445cccca1b53884feb08e98bea50ffe82e6879`  
		Last Modified: Thu, 20 Feb 2025 04:36:45 GMT  
		Size: 7.2 MB (7182015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc9fce4d3f0a60bac9c8406423a9ecd34950e8d3936f4015d2c071433737f2a`  
		Last Modified: Thu, 20 Feb 2025 04:36:46 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
