## `clojure:temurin-23-bullseye`

```console
$ docker pull clojure@sha256:1bd4fe654e360cec150bb4018d7812274738680753ddcf9b8c3bb59fbc8bd2db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:076397e60174b1b0be916125af8f816e3aa9b09cbd78ee8ff7da4ad850b6662a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288246053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca51d4a2ebe23afc970f08726b6a36d398cfd9b2ece235ba4d003d7f45347d99`
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e172a9cf2f0b060db83cbb3ee5424c16e0a6139d678c49f8e3fe5a9eed526b`  
		Last Modified: Tue, 25 Feb 2025 02:35:39 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706401864d511ad61534e2e88833c8b243f80a6a70500b9561bd2295deb702d2`  
		Last Modified: Tue, 25 Feb 2025 02:35:38 GMT  
		Size: 69.2 MB (69187382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82010919f1e9749e5a92747cef8561af959b67a372fcef925bb8a8e069d572d4`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56ee8049feee0dbb90319bf647fc1b8df86e2968376288551be7d7ff8d161b`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7c37ddbd631e8b65f133ae4abcac063764008b8c585aa1abfdda590db1747b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4852174b368876288728d212fb3e4385ada9361cea6f0de15bc1ba56e52e0a40`

```dockerfile
```

-	Layers:
	-	`sha256:564f2bbdc651bff9f17268414bc3a56f79566265679ebaa488ed2dc29e9e1406`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 7.2 MB (7209560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9c455e8d149d5606283e1d6300cfea64f3d3f12cc9c2614584849bd5ad4171`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 15.8 KB (15819 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ffd2f2530769d8abc2d5bb0e856f24b9a2519ecf7a12c5073e00b628bad8b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284900720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f180ff0d5976aae1bb0632467a7b0830a7877a2937d52a1410e3a8541bf00b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8eec5090566d9b173fbe17d851076eb6b1d8dd52aede26df92b2f75a42de64`  
		Last Modified: Tue, 25 Feb 2025 11:17:10 GMT  
		Size: 163.3 MB (163341441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47685a21f0a3a0fbe5a320de239b8530fa54a2a77fefc42828a7d8514d39df7f`  
		Last Modified: Tue, 25 Feb 2025 11:20:22 GMT  
		Size: 69.3 MB (69309594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0217d0a1733d0d983689f0e8959801c1b32b8bb627fadb9290940a08396dd357`  
		Last Modified: Tue, 25 Feb 2025 11:20:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434c60583d2c6ca1aca421425613efd0cd8333e1949279c08e06946b71fbdf1`  
		Last Modified: Tue, 25 Feb 2025 11:20:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a52340cfed13d163c945adb84b64d8214a8b5311d8b5a7258610e271056887bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e8a902686e523c29e08902e2c12678ffc61b35a3a3980c81f2759c9e8eb254`

```dockerfile
```

-	Layers:
	-	`sha256:11bd6ab53360e2752cb23beec03dcf6750f01152f016f409a97c0734ada149d0`  
		Last Modified: Tue, 25 Feb 2025 11:20:20 GMT  
		Size: 7.2 MB (7214038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a73c38ec8e203b7a0c509f914bfe3192afbfbf351afdb22adf94ec4ff6a266`  
		Last Modified: Tue, 25 Feb 2025 11:20:19 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
