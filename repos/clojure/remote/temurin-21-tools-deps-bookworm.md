## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:41c1f52fe247ad4f3abc1ded1fb9c02b6c089ad371b0dd31691aefce39107a81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5ba6cf9f25a41ee2a285fec3408c13cfdafec8ecfe4f3c7a788ce7b1510d48ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289063462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed578eea41812a9af31c7ce7a90ef7e625a3fc4bc8d1ed00ce05be73e04b7811`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddfeef2eabf1d6558d7c280c1f5c2d7145b884edd8cd60d0d6ac6c97dda6a68`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 158.6 MB (158579218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900da715ed16d38919fb4883192dd7a768eff2af1ca85c80f89eaebdba29927f`  
		Last Modified: Sat, 12 Oct 2024 00:54:00 GMT  
		Size: 80.9 MB (80928152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975d384479e144552fdf23e3e8410130ac32480269a2dfe4a9fb2178647955ec`  
		Last Modified: Sat, 12 Oct 2024 00:53:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a8009fc11f30c82b732673040d47a5bacfb67cc198b1d280dd429454fd8ae6`  
		Last Modified: Sat, 12 Oct 2024 00:53:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cbfbaef631419f43612640c5f191f24e5ec951a1107dfff47be52fcf7f819e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7179223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163a6c45bbb07a8dddeca9597f4c50a05f9e28ee92af7b4a2ef3ada63f9732bf`

```dockerfile
```

-	Layers:
	-	`sha256:f1df784628866c778e8c7159ca03753a1a4bee3fa148bae2ba9cc64b6e16ecd6`  
		Last Modified: Sat, 12 Oct 2024 00:53:59 GMT  
		Size: 7.2 MB (7161747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c773f4b211b373e73b723223409f554470e656f73d59950312a1373ff20911`  
		Last Modified: Sat, 12 Oct 2024 00:53:59 GMT  
		Size: 17.5 KB (17476 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e1af9314632e327df2f6e79e17ff4a5f1e3285d0e1756700795e33620a46c70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def86ce18a0ffd76b253d01b3dc2d78bcf334ad4b567be648c892dd252849cf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a21e2b47f54cf68dc71a6ca9ed705169a4d785cad9444569b57095902aa78ad`  
		Last Modified: Wed, 02 Oct 2024 05:23:18 GMT  
		Size: 156.7 MB (156746184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d042b9901153cb73ebf7334cff11ad7233bc0e1e811534fe001d8e1c5ec56759`  
		Last Modified: Sat, 12 Oct 2024 01:27:26 GMT  
		Size: 80.8 MB (80790214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ac408f14471b02639633642b15bc209c84796948047a187c0d12b743010813`  
		Last Modified: Sat, 12 Oct 2024 01:27:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381e751879bff1b697085b4233c0091dda889b3489a93a4629891e277713ffe6`  
		Last Modified: Sat, 12 Oct 2024 01:27:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:96c6e305c9fb75aa79c6fc676b2b7aa1f1d21e1c025ae0a39bd903eba0bfcd16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5239b54bd3444a029b59b8b784140819aa51485b1f14fb31a8cbeabbcc2a1a4b`

```dockerfile
```

-	Layers:
	-	`sha256:b035aaae6aaf137752a6f9fefe4267eaa7759f3c76ac48e4f10e4964fa3b60fb`  
		Last Modified: Sat, 12 Oct 2024 01:27:24 GMT  
		Size: 7.2 MB (7167587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a37993ab0c6c32d0e46f2da1caeb020b44c004c723a8411e9198498cf4556fe0`  
		Last Modified: Sat, 12 Oct 2024 01:27:24 GMT  
		Size: 17.7 KB (17656 bytes)  
		MIME: application/vnd.in-toto+json
