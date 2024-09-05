## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:6cba7814ca0724e3b975fba640f6bbf633fac2a98fd8f7efe62a57d5a078bac4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:208af244ca5d2cfe283bae7c0d24b6091e062a87766b126c5353267f9c1bf892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246614242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bb84b9c7c3b4d7f7669dfccb21544d781928414cbc5f95a5365f34d8291b04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
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
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef2cae9910068d992445827c0440c500f4d77bc4de3a6272adde60a73aa0f3e`  
		Last Modified: Wed, 04 Sep 2024 23:08:13 GMT  
		Size: 156.5 MB (156481614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ccb885decd613f16f5469b218745a86283f013033626ee65572e06b5996d93`  
		Last Modified: Wed, 04 Sep 2024 23:08:11 GMT  
		Size: 58.7 MB (58702910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c755e6d3a966050d7545e09a62dd1fec67b89b8d7fcd3d0ebe55d1d9d29a01c`  
		Last Modified: Wed, 04 Sep 2024 23:08:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a420c83bc2fb684f57738d7fa4b4294c890f9e6184c50e6a4eaf9dc1cbc185`  
		Last Modified: Wed, 04 Sep 2024 23:08:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1bbeeb98615d193d8b0af424ef518a25b254003bb2474e7b5cc389fab4512997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc407d154b8850ea97d8ca8a38e4262fa5575aebef0e51963edd9e66ed5de8a`

```dockerfile
```

-	Layers:
	-	`sha256:554932017ff2ff2130ebef439ff2f8958dbba4a3679a4f226c7feeb2a64c40b3`  
		Last Modified: Wed, 04 Sep 2024 23:08:10 GMT  
		Size: 4.9 MB (4949820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cc7c9d87f1740d67962a5b3575952f1cc296c37e7835b707bb946bf906bf333`  
		Last Modified: Wed, 04 Sep 2024 23:08:09 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c70ba5933e726ae46a6b0ef57dcf450f0fdcd6d78039154f3b681bf4174f771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243280223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fe7774270c66984761b80fa6a3a1d0bf39ec656acfacdebd568a1d4ec6c5e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ba7e76195cda3ca8bbaa6bc3f2cf7d8202bc05ae093c85d2a27712dda42f9`  
		Last Modified: Sat, 17 Aug 2024 06:36:09 GMT  
		Size: 154.5 MB (154503757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe34f77d416d9fbcef2d982b500291ae3f0c303e61db9a73cd23bc006373479`  
		Last Modified: Sat, 17 Aug 2024 06:41:19 GMT  
		Size: 58.7 MB (58699337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9490fe9eaa61e98bdc0af33fd3ef6e466d9d4900477910ba69a7a6a1b293f592`  
		Last Modified: Sat, 17 Aug 2024 06:41:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93617668e19a30b1c834fbe8bf06585e08a8fefcc7b24f54aa345dacd8aa0cd2`  
		Last Modified: Sat, 17 Aug 2024 06:41:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d35b0fc6def0483edf21089473983da5dfe394031861c86b2716810c1a7564d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d77ca5e0c0c01c37b71076c6a65d009e85168894a7dc357a52ca4092cbddb31`

```dockerfile
```

-	Layers:
	-	`sha256:700dbe260686a8f609dae31750cc148d4f0f009f028a0bb41028b15cd11fd343`  
		Last Modified: Sat, 24 Aug 2024 00:12:08 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b9eee928b4955b3eb9055fd8fc6c3b3bf5803e67d001342334140f256fef85`  
		Last Modified: Sat, 24 Aug 2024 00:12:07 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
