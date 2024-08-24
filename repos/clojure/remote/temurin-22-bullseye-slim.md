## `clojure:temurin-22-bullseye-slim`

```console
$ docker pull clojure@sha256:b2a4b1e8f54e6006ef182b598ccedeca46fe5728d051a65e055b824fd61fc032
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c8818fd54d6a34b7de958710ca037fa29c570e6c8bb1cbebb1917bae5df7db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246483014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4c9bdd5b2a0c96b2f9c049808b4f2a06fe9e9b8d06e4c51036dd5f446d7df8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2622cda60e815645d4a0e8b58ed2b29ff684fdd0b6bba06b31a7f17dd07b90a0`  
		Last Modified: Fri, 23 Aug 2024 20:05:33 GMT  
		Size: 156.5 MB (156481631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac48fe999611bf2c5325c7125a9cef9a12a87f883def4d1873e203ac2fbd726`  
		Last Modified: Fri, 23 Aug 2024 20:05:32 GMT  
		Size: 58.6 MB (58572053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0202704ae48e7fdff7912f8fdc9a587a0f623dc85e31b867e7b028b53163a9c5`  
		Last Modified: Fri, 23 Aug 2024 20:05:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5f7dad7b5433db35bd2e49baef8650c76f555a71bbf25748408ab916aeda36`  
		Last Modified: Fri, 23 Aug 2024 20:05:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e986421fddb91d7017ed1f423595f2ca10caa4b3d1cb534164d72993b51a1152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0359038afd067e5184bb1e0e111f1bb59e4d8ab3a871c82146411973d900eabb`

```dockerfile
```

-	Layers:
	-	`sha256:cab16077ebd1c7030a99db93d1a602d7cd0382cb0d7f2511d2c2e470fee26a74`  
		Last Modified: Fri, 23 Aug 2024 20:05:31 GMT  
		Size: 4.9 MB (4949820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792875dcc856d63a444d813c72d1d7128852d4e1033fb7b005f997d0fcb1e945`  
		Last Modified: Fri, 23 Aug 2024 20:05:31 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81a6b856a61faed4950b922c62d013eb2fe04c22f8dcabfafa1897a88adc657a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982fc8993371b2f891da8c60c7c0254e74d74927cd5a03e4b53dcaaec072a573`

```dockerfile
```

-	Layers:
	-	`sha256:7dd76a1ab5bb57608d67b72adc8938f09bc5c4b6689809bd3bbee62bd8186534`  
		Last Modified: Sat, 17 Aug 2024 06:41:18 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7e338204567ae38016f3fe4039a06239d54bc4469c75c47b031769c8a036f8`  
		Last Modified: Sat, 17 Aug 2024 06:41:17 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
