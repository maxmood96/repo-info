## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:6bd099f3684862c6f5eea38df5b2231014db566653d2ccca9d236998ffd0dc75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e1005930e380b6ec3fe1a51a78bafad37acf4e47aa3ea2c0f282ff650be4be89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274029388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859b633f4cdfc451b349ee84fb8e3f1b7f9e6f40d71d7c7b86252bb358049372`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e5d2993a8d7a5e5bc0ea260d1baab53b29f5f416bdfd62408cd041b29435`  
		Last Modified: Mon, 17 Mar 2025 23:17:48 GMT  
		Size: 144.6 MB (144566524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7a1af1130a59134aa775073045b3f37c3525005237e6278d4047db8bb786c`  
		Last Modified: Mon, 17 Mar 2025 23:17:47 GMT  
		Size: 81.0 MB (80993986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f30934fa1cdba539703970cb28a31ad81a3d0b5a20c665080452402e19e1bdd`  
		Last Modified: Mon, 17 Mar 2025 23:17:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a54ee93b19a683d919fa1462c37627dabd6cd443db47fa293adc4aa35f8b49c`  
		Last Modified: Mon, 17 Mar 2025 23:17:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4ef60913b6812d8cbe8a785e753b0d2c984851b8fdbd78f3973b947185a16e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab786eccd34358cec093886b87afd494bf94429272f9d591459933b8a88b39b8`

```dockerfile
```

-	Layers:
	-	`sha256:3a02355517cc2a0170f01786f4520285e772508b285f864fbcc5b41d08676f94`  
		Last Modified: Mon, 17 Mar 2025 23:17:46 GMT  
		Size: 7.2 MB (7171108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2542bc37a3d6f58bc1df2e52cebdceb3ac357b9e102b4c7f01278c8b9f039ae3`  
		Last Modified: Mon, 17 Mar 2025 23:17:46 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80f7c0e4ca0914a04c2af75ab5637ced541d7b671175e2d70056e1533be205e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272603411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc12dbc15a02e135e3d43e197c213e07d3feaa01816ac8b8018232e42302f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998164cfae4d7f81bfc93eddab66e4a630e0ebbdc2a82ffda297a99017b6aa1e`  
		Last Modified: Mon, 17 Mar 2025 23:40:16 GMT  
		Size: 143.5 MB (143454716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719ec5c6f685922819e6ad078067d97c7503551d877000bd6b826069be0543d3`  
		Last Modified: Tue, 18 Mar 2025 00:02:37 GMT  
		Size: 80.8 MB (80842796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3af4718ea050154c3a88839bb48844f7c8655f9cfecfcacef4d0029e0d680e`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd44b4c7c94085fdfad20f7cd7391304a446f7035a2732d14443613fa61233`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ad45d5b0912c732c7648c36bf23a68d2c3224fc4d391c4a4da1f8f5172228208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb84681039560de16f5c698947b6694556ca668250bf04062cfe3e0f781d171`

```dockerfile
```

-	Layers:
	-	`sha256:8859e5ff191047d1ed53892d7bddb0ff375555fff786d43f4ffe5cd03a685506`  
		Last Modified: Tue, 18 Mar 2025 00:02:35 GMT  
		Size: 7.2 MB (7176871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:150b8c1d4a8e21d6b42ac754a87e30b9cadb673679228472dcd7e3640bb95bc0`  
		Last Modified: Tue, 18 Mar 2025 00:02:34 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
