## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0e2d3f1d348603ace3ecf1a947eaa48c17cfc2421b9d5518bedcbd84d4f4baf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b152585da40c7b77218e1b798f6677c02f8aa6e68ad656a0442fbfe5155b921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242323387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e993565fb947463cfb62caa4dffce38b9241a56eaee91417be4b2d49792193`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f573a9bf8dcd578bb718ee9e1d55b4608898dede75278a32f99e70b5d0a60590`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 144.6 MB (144566523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6b4b946414ad4f07839628be646b388b1c13cca2e431baaad5185678ec53e8`  
		Last Modified: Wed, 09 Apr 2025 02:19:07 GMT  
		Size: 69.5 MB (69528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e0731c6613824399ab41d05e3cec34ec9d6fe17c87fb9e2cd9b163bbf0d391`  
		Last Modified: Wed, 09 Apr 2025 02:19:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4369be9406cc89796fceec7c86f120d3db6290caae6d3d208a751a9f92db1b6f`  
		Last Modified: Wed, 09 Apr 2025 02:19:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0297e2bf10d38790f0ff63bcddcda90cbde09cff222a7e18d4bed792debc869e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203b987a8171985e99bef4ff238027d7765539e5b49c84f6f4a17ebb6ae67e73`

```dockerfile
```

-	Layers:
	-	`sha256:4a1d13c349be63ce9b835fe38fba68d21a9eb3e72649bca2eb07b82a187e8233`  
		Last Modified: Wed, 09 Apr 2025 02:19:05 GMT  
		Size: 4.9 MB (4913965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a221c006e63a03c59dca22ae69fd53b0f5aa65d9a2f8030f2f882257adb0e48`  
		Last Modified: Wed, 09 Apr 2025 02:19:05 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5a038fd1623bcb325779c9ab5085e320eb66eb054c52119ef416431dd3e1416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240899734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dac9156179292592c7a2908f909d6b8200488bb2a1311f133c1588a8f9ca16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e330b25eff171b18e5a99f840bc62624233db83e3b75bc7cf704398fb8b1a059`  
		Last Modified: Wed, 09 Apr 2025 17:30:24 GMT  
		Size: 143.5 MB (143454651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170fbb0b441b1eb9fbac206f9c6bfaa91f956b083f313e802b09ef4e28b5f135`  
		Last Modified: Wed, 09 Apr 2025 17:35:17 GMT  
		Size: 69.4 MB (69377722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac6d0c8afdfa503c708c23111d4fe061c50c2f05cf80f59146a999bf9e19d01`  
		Last Modified: Wed, 09 Apr 2025 17:35:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6d87f77bf13046961d888c04dcb124c2680d81ac8e2985ce0b6cad74d36901`  
		Last Modified: Wed, 09 Apr 2025 17:35:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a64798ea486ffee59d5670b088b42a8062770acc08ee794b95277543a2ac76bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174aee276120846f453ae1f38a8626d7ed02a5f9de3cf699fa438d5fcda56857`

```dockerfile
```

-	Layers:
	-	`sha256:8e0a0d1a867af4a6d898e34addaff02ac7c04c6941d9de4918a1c1f9565b9cba`  
		Last Modified: Wed, 09 Apr 2025 17:35:15 GMT  
		Size: 4.9 MB (4919726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba83130f524ed7e9724b32c379015245025640a558be3580750eec0ee0dca8e5`  
		Last Modified: Wed, 09 Apr 2025 17:35:14 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
