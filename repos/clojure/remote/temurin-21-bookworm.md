## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:fc0ad6fb2bd2156d3b7fa2e30b3b23e818ec7dedfe808e784df74f1d1fe4f92d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9aaee686b9d4b79a2c0004909ca8662a3f0267a9cbee75dfcae64e93f5a2544f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287057409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bad43d4502f0ea789fb63d9346ab1326abf379247fefa9db3de47a93d1bc362`
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
	-	`sha256:4ac55335407a6d8c8ffe607691aaca73b4317e1e3c5fccedea7670cbc6d07c78`  
		Last Modified: Tue, 25 Feb 2025 02:34:29 GMT  
		Size: 157.6 MB (157585882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecadf41747f723a90cab99bd63fe50e3b60b8013af0697728bff714749dab7`  
		Last Modified: Tue, 25 Feb 2025 02:34:27 GMT  
		Size: 81.0 MB (80994388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473d24c23dcd27e9d9c1e1d219b205e9025ba51ff7afeb75a319dd7d44304486`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb02c65f51adfe5984be435a3e5c7aa14c13357249c35d7f180c28e18ffad10a`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:506146fc17cf27bf9f04b7e49df8047be1016b85f2c96433ce222663bbf83d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a5d907c67ac0eea2a23068ec3d969826be2783ea57c9685c37c9627d37945a`

```dockerfile
```

-	Layers:
	-	`sha256:8479cc40f2990db2282e53702b424af24bec7916bd47069efb994b192d31fdea`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 7.2 MB (7176198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ff687e66fbb5ea0533a86e1acf4c51029e34fabf32ef5a73a8563daff216b6`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

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
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5fa34edacd0f0acb63e2f1d258d50a9bfe6e1592d31c38031a099fd6fb4fd`  
		Last Modified: Tue, 04 Feb 2025 23:23:27 GMT  
		Size: 155.9 MB (155859274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db9801a2417e18573a328fe46f57d13c86b5a3d88838561ef7a5ed58554b1eb`  
		Last Modified: Thu, 20 Feb 2025 03:56:08 GMT  
		Size: 80.8 MB (80844030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a20562664a5a1b798729ec223c8944fb356c7ee0ad877b5c3e21e90737bf03`  
		Last Modified: Thu, 20 Feb 2025 03:56:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf2b9cf256910cd2b82c41676a17e3135001d4f35d123f33b08d15cc12cc459`  
		Last Modified: Thu, 20 Feb 2025 03:56:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

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
		Last Modified: Thu, 20 Feb 2025 03:56:06 GMT  
		Size: 7.2 MB (7182015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc9fce4d3f0a60bac9c8406423a9ecd34950e8d3936f4015d2c071433737f2a`  
		Last Modified: Thu, 20 Feb 2025 03:56:06 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
