## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ddc2406d7fe7363ad229becdaa03ed89db5e510debbba442e03059c459392710
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ee86c40df43917d094faebd74f92994c9e62029d1ef95771597ed5a343242af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233608671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40acc6172f763c855737da8129f523fe5e5a739358b2487fc88511a91569ef7c`
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
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db946bc34ffbfb504cc1c964b87b7be0aac9e17ae6c1ff8ed206ce5ce142bfb`  
		Last Modified: Thu, 20 Feb 2025 09:57:33 GMT  
		Size: 144.6 MB (144566545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698106d77aa007b9d97634d1616724b35c43874d75c984d6dac07f52cf488f78`  
		Last Modified: Thu, 20 Feb 2025 02:31:29 GMT  
		Size: 58.8 MB (58788495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1da532878bd4e5de32513c05b024794d2c83580988e0970bf686a303e929c0d`  
		Last Modified: Thu, 20 Feb 2025 02:31:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c0f206839d40f15078bf27b997298e6282b6fba33720c138b9a0475351afd4`  
		Last Modified: Thu, 20 Feb 2025 02:31:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb7cc302174619c41f82a91c2f86e4c2f4417c1d3c4d1a7d23280e296474949d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6914ac47ade0027fa30a28fb6c8c8af71de5c79d37870da3c2df83973a939b6`

```dockerfile
```

-	Layers:
	-	`sha256:21e144ad43321371ef4cf2ac4d31c7da721dec68d7dbc95361a9249c1873c90e`  
		Last Modified: Thu, 20 Feb 2025 04:35:57 GMT  
		Size: 5.1 MB (5117067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6480f1597e8ce6f7bb223681eb8ecb2e4f7cc3763892ae730351e6a33afc11fe`  
		Last Modified: Thu, 20 Feb 2025 04:35:57 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

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
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348ff9ac1b37388eb3a2a2be1629fee6895100908a9151629f94915c2adee8bb`  
		Last Modified: Tue, 04 Feb 2025 22:21:43 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dd88e93bc60c1d9838f7661af81fd8ba93eafee675eba2a4599d52756a6af1`  
		Last Modified: Thu, 20 Feb 2025 03:54:13 GMT  
		Size: 58.9 MB (58910389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b69356db9120c901088281f3a092eb222e3a8616b230c368ce0f6a94219b44c`  
		Last Modified: Thu, 20 Feb 2025 03:53:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00efe1970cdf83144d1d941dcfb59b35c8798dfd34331eb1bbc459b37045d6c`  
		Last Modified: Thu, 20 Feb 2025 03:53:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

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
		Last Modified: Thu, 20 Feb 2025 04:36:00 GMT  
		Size: 5.1 MB (5122799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fbed07f70f442948853303a810da0af30c911f3282c49f39238acfa59fb3c6e`  
		Last Modified: Thu, 20 Feb 2025 04:36:00 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
