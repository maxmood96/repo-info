## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:9a53263fa38c09fc5a2b78700460348bcc41ba0417fb997b90ea44ba52327827
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:277dcb5ed57666715bf5245a82a1f4bd0360789a5ae600b3c59ab59204cd6a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267436677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6adb657a6049c56a4943de8b99385b22fd6ea0eb31c56ee23240661990c9ee0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cde9188f35989d4b59cd78defad7e0b91e90e8e6f8932ca8792ae53ea63191`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 144.5 MB (144536666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fa4cc9ea238fda6fca5e1c0ec4b630245aa3c06e13f0cc3a00275df9ad766`  
		Last Modified: Tue, 24 Dec 2024 22:38:28 GMT  
		Size: 69.2 MB (69160015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b172720149e92d5f3cd3063a8da39d1a68647a468e3d1b78340ad7626e2223dd`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25a11a8be72a9fa8d0a3d017d1063015aa8acc1b026345a7cd9d32f61fe31c5`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:58304f9ddb155376ff3c954647ce818ff01b1a7774f58f5b57154bd3a671adca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7465076b46570ecd7ab04159d308768193c4f2ed1a2342fd9a2e12b4dc5037`

```dockerfile
```

-	Layers:
	-	`sha256:8c58bdf3200e50c58bcad72b3562c4492debdff848f59d91f7a22bb0d7212f09`  
		Last Modified: Tue, 24 Dec 2024 22:38:26 GMT  
		Size: 7.2 MB (7204495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd704be2275ec43bd1dde9161398a0a8f813ff5a0d5e34bacb2ef719cb50d04`  
		Last Modified: Tue, 24 Dec 2024 22:38:25 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9e1c963453a3a50d940dddc6e5998eca7479dca97b9c8762486c4464629a8e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264893741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543817e86f5f133cc9aca473e12dce6b44e03513e46d4938ec11e3570290714d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d1ea0cb763505ca8df8fc32c78297612e6917521b4419e34a15aea4a92e6b`  
		Last Modified: Tue, 03 Dec 2024 15:18:30 GMT  
		Size: 143.4 MB (143360959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648a44f8907f695f2a7a55ccd78e78ee557ec55e8c4503ccd00e0e80d5572fc`  
		Last Modified: Tue, 03 Dec 2024 15:22:24 GMT  
		Size: 69.3 MB (69285751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62eeca9d605a65cc8db007b2249917c7dd74a95cb782d2f3417bbbfedf905b`  
		Last Modified: Tue, 03 Dec 2024 15:22:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda6856938f2e8a29e8c0d4420b208eca4619da7d0d0e8abd35e1035e1fc7c8a`  
		Last Modified: Tue, 03 Dec 2024 15:22:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f9b0e8296595fcd42dc0babe149dc87a3ecf08d576fe8cfb7f7dec3c7afb69b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51263b99ce99c9bbc28299511d54cccd36013e82afcd76403e5488a4b1ecdb76`

```dockerfile
```

-	Layers:
	-	`sha256:3a9d3593af45f02a13e63fdc0dab26abcb4df396c351af4c0308b4ed012d9dff`  
		Last Modified: Tue, 03 Dec 2024 15:22:22 GMT  
		Size: 7.2 MB (7219170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ecc8ed8c5b7456baa549f51f5da22a86677a2d86afa03f49f1374de2d45c2bd`  
		Last Modified: Tue, 03 Dec 2024 15:22:21 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
