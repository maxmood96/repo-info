## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:928a0067170b3649be28281348f6f379e63625d57f1e0b5f40250d8ab526421f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:383a7d8d2fadcd329c20dcca28823f91996af5ce05e491d2a3bb8db6c24508c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267494117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab03725e80fda93dda3ef225b00e0a2e79b638aa620bf5c84ce065d54345608`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db946bc34ffbfb504cc1c964b87b7be0aac9e17ae6c1ff8ed206ce5ce142bfb`  
		Last Modified: Thu, 20 Feb 2025 02:30:51 GMT  
		Size: 144.6 MB (144566545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337af382aaf3c8c028657e97891373b86f7c28e5a2bb5251671d56961cbc49d0`  
		Last Modified: Thu, 20 Feb 2025 02:30:53 GMT  
		Size: 69.2 MB (69187658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fad70b07bc638d8176eb53f15c92924d0b317c187dc67cb72ebb24aafcb817`  
		Last Modified: Thu, 20 Feb 2025 02:30:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8495360f0f73109468d27614e757a3f676560591630853b814f4dace0bb834be`  
		Last Modified: Thu, 20 Feb 2025 02:30:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3ade4f1bd51d483eb5cbd40b41d3ec7d67034b8bc869872f21baec5d9a596be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdbd28751e2d04f5a7d17f2aa6db15e516e60d00de5f128048da41e5c5fc718`

```dockerfile
```

-	Layers:
	-	`sha256:17aea650188f79c2cdf2e34102b6c0feebd48001b9daf83f7c46a4d995008cd1`  
		Last Modified: Thu, 20 Feb 2025 02:30:52 GMT  
		Size: 7.2 MB (7204555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:592f7f9d720655f1b745b444853562ea5a4413018ebe8448d123e526054bde81`  
		Last Modified: Thu, 20 Feb 2025 02:30:52 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7cdfa540ad4ddafc96ef8b20ff89632e5d248cb54fbd1f3998fa94eb2701d081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265011010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ec1ce33a52ba92a90ad7145b195e856ddcffd0e16683e29c9f2f556aa6fdb9`
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1708d5129285b28e8d76370a0f7735985e646f6353ff58995c4404eb7c7ac`  
		Last Modified: Tue, 04 Feb 2025 23:44:31 GMT  
		Size: 143.5 MB (143454660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfd7c503850166975589aa4660a701de35d79d09526abef090a02799acd078c`  
		Last Modified: Thu, 20 Feb 2025 03:53:04 GMT  
		Size: 69.3 MB (69309614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defbbea8bd670eb1b5239acf79a4a7f919850e2b3f9cee11fc6d47ca164a8f36`  
		Last Modified: Thu, 20 Feb 2025 03:53:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17739e1b0736012053a219be289d9ca2993b25fb6f3fe9c6e6c3381846c0f7`  
		Last Modified: Thu, 20 Feb 2025 03:53:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5134b26f3a5553d1f2cd7e8d708fc52951bc7a848ff839d0019c4eea72c26b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43235ad19942280030eef912a4933a420a511a249cb6245a236cc3a9841e584b`

```dockerfile
```

-	Layers:
	-	`sha256:94e5b49077474dea5f111ba572f65e4538b5f3f650695b12aeb31ff8ecfc5594`  
		Last Modified: Thu, 20 Feb 2025 03:53:02 GMT  
		Size: 7.2 MB (7209654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06625093d211bf2bdb0b5212b01f6c87989a6a52fc6950c6189fe5655d0caf8b`  
		Last Modified: Thu, 20 Feb 2025 03:53:02 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
