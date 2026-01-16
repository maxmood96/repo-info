## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:d98e4a8650a837a81a3641c0862d4b375a01851f473df75d55337ebc2bd10621
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f7ef30a34be34897222f57e64799c7727c8a928eb90e49669b1cdf6c6f13f7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215359436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20bd58bf3eb91c003ad127ace4e9b0e4a2a48980bffd01b3ffbcc89e3582c73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:40:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:40:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:40:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:40:10 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:40:10 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:40:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:40:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:40:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:40:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:40:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06b1dcc712c947fb6adee70ad409bf96c70e802ce14aa44cd00056a24319f6d`  
		Last Modified: Tue, 13 Jan 2026 03:41:03 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8dde4f1fcee2aea4a9d8ab2354ee12f6e4ee53de896cd4cd71592f4ec2970d`  
		Last Modified: Tue, 13 Jan 2026 03:41:04 GMT  
		Size: 69.6 MB (69556660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf819c57cc3208cb56f41185dfa826aac3e40fc5bb733b98019fac20dc630273`  
		Last Modified: Tue, 13 Jan 2026 03:40:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a488cf10bc5cbf4689a1cd7d9dbdb1924c7f719d8e4d66b3403617e577702c2`  
		Last Modified: Tue, 13 Jan 2026 03:40:56 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c8a592a8fa8a153c0dead9a876a6ebcbed5e9e458dc0eb5a4de35265f2082018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f676e0c0e5b8c9101cba60d1d02928a01003f6e0a5d84bb5f8513d02f4944cf9`

```dockerfile
```

-	Layers:
	-	`sha256:8ac65b14650aa672cd88946f242f0f3ac74aa3630c61b022185277c6a8b5a0ed`  
		Last Modified: Tue, 13 Jan 2026 07:45:37 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9cf3fa5458cc423e8d618ed09083146f4c05af1caf747d0ac2686ccd9245287`  
		Last Modified: Tue, 13 Jan 2026 07:45:39 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c4e36c6e6e6c9a6b51c7d72521f3bc5c91c396b87884f23c5a20749cf1ca77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212998207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec135084340f5e7e4b6870927a4e7c83a24fddc743d52c32a4739409dabe415`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:43:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:43:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:43:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:43:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:43:22 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:43:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:43:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:43:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:43:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:43:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019ac788c4a1578cc5994264646e248dac8ccafff8ac344809812a3a2c393d72`  
		Last Modified: Tue, 13 Jan 2026 03:44:15 GMT  
		Size: 91.1 MB (91052481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563c37accfc66e28ceea74757ca826965b4511a6477f15b4264f6b1818c8c1e4`  
		Last Modified: Tue, 13 Jan 2026 03:44:06 GMT  
		Size: 69.7 MB (69686920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ad255411d7a63ca0ae283d7c694a0f4197ba9ce8bb5d04c247432676927349`  
		Last Modified: Tue, 13 Jan 2026 03:44:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15702557bbadd4c66b482bdeb79870c79084039beaf023394d5cf188bd7526e5`  
		Last Modified: Tue, 13 Jan 2026 03:44:01 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4426d375aa16df58a51120d551902ddbd23068b0eb37dddb6d43ea5c0f4cfce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f778d49d170e93803034ee668bc1a64dccef92ae44e5e4e68dd5c96ab2cf518`

```dockerfile
```

-	Layers:
	-	`sha256:53822d874ea8843d0c2c963b2a22cc3427defdca5a7794fb03d40625a640e937`  
		Last Modified: Tue, 13 Jan 2026 07:45:46 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a4e52a4fc29eb59ad731f006f0df98fbbdd19b706455a61d8885b05e3b26e27`  
		Last Modified: Tue, 13 Jan 2026 07:45:55 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
