## `clojure:tools-deps-1.12.0.1501-bookworm-slim`

```console
$ docker pull clojure@sha256:f85a0ef785bc6fc51a2934646f1af71e1ae74de451b2402617688745be1c3ebf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1501-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ecce53901c9f2914687c5b60e774c4bf9d53b578423b0c24d56e89a734eb0efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255313724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eec06d33406fab90686131293754b888da8cc9f912a8cac5edfa732a40ab2fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80feb786482482bbf040b17e112654238ceb1df2771b3db09e8ff72611529c2`  
		Last Modified: Wed, 29 Jan 2025 20:27:44 GMT  
		Size: 157.6 MB (157568679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0b19c68fea460ee505b3bb64e8ca34197c2642945d5d564971ec1622c163b7`  
		Last Modified: Wed, 29 Jan 2025 20:27:45 GMT  
		Size: 69.5 MB (69531589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90d1112d33ee29082912b251d8b6ed5499a815a56277ce634ae29bafd1bad3c`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de67fb5d4d333ea8437ecdf3816c6c2c999d0d42a039d57808d96f55f0ba90`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38c8d708d2a08a99b20f629a44242f15a41b74e20d485e3f0c0466cf21857ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48389ebc091c07c1690dbf22daa9d1fc49ef46681836b1649be6c933c011ccc`

```dockerfile
```

-	Layers:
	-	`sha256:71410ffdfb48ccd65fa67b32477fa648dc3ca954f7d066a7932fbecff852129b`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 4.9 MB (4916367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e7b0620fd44ed099cd4e74d4e6370127fff5a2f3115976402f063e3a5af71f`  
		Last Modified: Wed, 29 Jan 2025 20:27:42 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1501-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2242bd340f4e63bf8c0930131d91b444f6d4e8e00a6f3736d27a5ca88a8009f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253216673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f2a7c8a1a3bf634efb544e1b64d8d7e9c26c5e7dc47cb2e50dc32c74894ff2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2b2cbcec988c950b61c68558a29d15b455bb56c17644373d901a2c20f07fa0`  
		Last Modified: Thu, 23 Jan 2025 02:54:30 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ead2e75b8fb57fe26c9c1a2e0d7e2e26e45a4bf298571e4b3316ba737aa934d`  
		Last Modified: Wed, 29 Jan 2025 20:53:35 GMT  
		Size: 69.4 MB (69381536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b913a6f12470d6fcf11eea0cab146f22d630f412ba7887e6fc1b63b7e5f62ca`  
		Last Modified: Wed, 29 Jan 2025 20:53:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbbfc26219354234495c05235e04be8cba9b6879038aa200832dff2c0384b85`  
		Last Modified: Wed, 29 Jan 2025 20:53:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8eebab34064c9fa7d03163774ff9770a56e7ac3fc9a03695bee981fa1a648ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e384b506f2a72266f492a7588c810a30d44a8dc84addb0096ea125bd1b4d7dd8`

```dockerfile
```

-	Layers:
	-	`sha256:dd592eed124f95a3768cfffc67252df279d739afd9c360d9807041a572cb6086`  
		Last Modified: Wed, 29 Jan 2025 20:53:33 GMT  
		Size: 4.9 MB (4922152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a35d116656585ad4717cdb9b4695ae4f55da768ad43c1125c7cde442648afd`  
		Last Modified: Wed, 29 Jan 2025 20:53:33 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
