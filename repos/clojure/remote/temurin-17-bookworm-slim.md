## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:99724c96614f584dbf7b3cc74c5893a864677f6540d60928724798413634a22d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4b08f08ec44e821c144915f97c3997743582bf568906242c70d075c88e2185a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243315624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adf0580b4e6ba7b6026eef2c20cd98ad932b056d2efcc50d01b2bbffd1bf4dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196aa1d5898a3068e020641ae927b0e33ba03ada362715c2d8f68ae0377ce3a1`  
		Last Modified: Sat, 17 Aug 2024 01:59:44 GMT  
		Size: 145.2 MB (145164850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be3cec1a591d428562fa7f6602e2bd7aad03ff8eef0b909bb3562211566d1b6`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 69.0 MB (69023500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7957d280a12a26496b3e3b0997b85af6762f7add64b296b3d4b5f33143ac11d`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22085267e869c26e42b4bf16b2d9ab00802829cdcd5966ddaf4708c39863e634`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c3626b71421f93a68d48211bef26a5b38b3ab1f59f6fafd6b9bfc90ff3fc784e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9b56cfe36b77a154864149ca19ce9c4b84dbf077842aa0818bdb1e5fdecac5`

```dockerfile
```

-	Layers:
	-	`sha256:6b4526024622155fce2515ac3bf4a24a8a408b5e9a71dbc38901e63e657cb99e`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f594e0ab2af89f9a5153b4cd398391c93cf57c486c15e560770f88a7468d98f`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e936d3a29b6cfd4b74a8a57d79199aecbe8095c80e8a316bfcc792d79d9b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f501b40ecffeeb4eaa8cb535aa477ee556a0e494b75bfad090479860125b8a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9c0339aabced184ab039c5680e7ed2855ab3a3801ba3e4f5b74614d7da3ed`  
		Last Modified: Tue, 13 Aug 2024 06:31:29 GMT  
		Size: 144.0 MB (143959451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6149fbf015a51e0ccd0f2f48cc98a497fe931eb78004681bb28cc580e3405bce`  
		Last Modified: Tue, 13 Aug 2024 06:35:30 GMT  
		Size: 68.8 MB (68773427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1955f5179c89854e41452b65ac9e34c0415cf14c8699cde19180ba808ba064`  
		Last Modified: Tue, 13 Aug 2024 06:35:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf78f568eedef318a8a8dd122c425ca8c70b5585d91c01682c12a5cb376a4af`  
		Last Modified: Tue, 13 Aug 2024 06:35:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:557600231376ca9fc9e3965fa8f987f34249c995faf9b89136427f364609f519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eceb3d26be041a0daba8267d916c4afe8484d538bda702a002d9d1f7164bced`

```dockerfile
```

-	Layers:
	-	`sha256:92c450abcd504a082c9c1ba8e9f2480e98951b3b714d5ec1e29ad8edea0a076f`  
		Last Modified: Tue, 13 Aug 2024 06:35:28 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57924c80d56c3b9736df506ef76a322eb5c5bbbd7fabae15d4c146303249f835`  
		Last Modified: Tue, 13 Aug 2024 06:35:28 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
