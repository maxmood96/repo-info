## `clojure:temurin-17-tools-deps-1.12.0.1517-bullseye-slim`

```console
$ docker pull clojure@sha256:1d52fd55c47454f8820a6312ec8e8592400d4359e90a58ae75c8d78e182dbedd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1517-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b91f7cd13727595f2109427042d5fe4dfd340034d9e0a5a377318c0f116fafd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233609777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa2ffe746c46aa1f3a7ccb2960bd8b07b1a6b01860f550fbf25bfb85e0193cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d8f0d47dff0ce19b8d433830013cbb65165ac9cf7731cd27c9d558068358a`  
		Last Modified: Tue, 25 Feb 2025 02:33:16 GMT  
		Size: 144.6 MB (144566545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7df0a8272e272daf4dbc52a9f76ae6eb8a5796949c357975cefcaa9285f4e2`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 58.8 MB (58788258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9760ef131b03e1eedce2f10d00214b46c90ed0f5caf91b25a3d97665c2062847`  
		Last Modified: Tue, 25 Feb 2025 02:33:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c2ef81e8b71ae677a463bd828000f811e50ff9ec71e0813f2494face6a5b4`  
		Last Modified: Tue, 25 Feb 2025 02:33:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:427020e08e08b4306bf584e9bf08f6739b5cd46d3089f88d5e5a6c643f6da375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c601edbd3091dc8bf496c162359d6b2500c06fa1f1af3b83864475840c7c7b`

```dockerfile
```

-	Layers:
	-	`sha256:b912d51dd8fe300e613aa51fa2097353209839b3df2753d2da7d8ad0424dfcdd`  
		Last Modified: Tue, 25 Feb 2025 02:33:13 GMT  
		Size: 5.1 MB (5117067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09a1048f70f0f2f3464e3d6c5416e069cb474c9d80d8cda6a020a7ecf10a1b3`  
		Last Modified: Tue, 25 Feb 2025 02:33:12 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1517-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d81e754e85be0039bb4933aa3ddf8a5b6d23f35bcdb0b7a729c32aa03dd31689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231110966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51874da1f8867158e093df2c8be43dbdcc9757d5d38588f05451c0b156bf8f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348ff9ac1b37388eb3a2a2be1629fee6895100908a9151629f94915c2adee8bb`  
		Last Modified: Tue, 04 Feb 2025 21:13:28 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dd88e93bc60c1d9838f7661af81fd8ba93eafee675eba2a4599d52756a6af1`  
		Last Modified: Thu, 20 Feb 2025 03:53:48 GMT  
		Size: 58.9 MB (58910389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b69356db9120c901088281f3a092eb222e3a8616b230c368ce0f6a94219b44c`  
		Last Modified: Thu, 20 Feb 2025 03:53:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00efe1970cdf83144d1d941dcfb59b35c8798dfd34331eb1bbc459b37045d6c`  
		Last Modified: Thu, 20 Feb 2025 03:53:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1517-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02df1d0fe69f6d8ced2ea86187cb3a56a2cb565d17f42d46b3e785ef1898c8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36618914ec3948fa2c6ce9f05f65f1d96ef67062f7ea829c47f41ebac55d4a`

```dockerfile
```

-	Layers:
	-	`sha256:ee3de400079f3045b032d9276bca34c95c3761564e31555ef5c49b5ca9dfea89`  
		Last Modified: Thu, 20 Feb 2025 03:53:47 GMT  
		Size: 5.1 MB (5122799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fbed07f70f442948853303a810da0af30c911f3282c49f39238acfa59fb3c6e`  
		Last Modified: Thu, 20 Feb 2025 03:53:46 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
