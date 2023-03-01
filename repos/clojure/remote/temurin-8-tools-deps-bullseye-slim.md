## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:61686be44368945ac1b3e101e00f56b3e9700fd9ca73ad97e5bb6e45f3b8bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c0412b095c4ba85cf6b81d79f5e9e4f644ec11dc32552dfe4cd2ad9ef8887058
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147533097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5372481821c739837222278560ea2ca36fb46a125d513318bebd0a118e52b8b0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:41:23 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:41:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:43:14 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 07:43:14 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:43:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 07:43:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 07:43:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210fb3e5d8b959c70a42ac05437d84dbd0b87ade6872fb868c2e70d60c561eb7`  
		Last Modified: Wed, 01 Mar 2023 07:55:19 GMT  
		Size: 54.6 MB (54635554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247c94b3c29585ddef25eecc256ab33ca261b0e24dc21827365d9126610270e4`  
		Last Modified: Wed, 01 Mar 2023 07:56:17 GMT  
		Size: 61.5 MB (61485526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4202800e7b89281e9f5e08b86ac309db19c6b48424490573f9217fa7ead9df3f`  
		Last Modified: Wed, 01 Mar 2023 07:56:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8677e7ab5a1da471f9c091b0570bae74e07f84f08492bd54d4d7b029946f1c2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145391428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f2a07d91c5afe12b9ec8e3ecd9137d5518751a9c3b7214f975e7835144db59`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:02:03 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:03:38 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 03:03:38 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:03:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 03:03:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 03:03:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ed8d1b5c6c501960add7e45237e7cb7c527399c9fe073375eb66890797d9b9`  
		Last Modified: Wed, 01 Mar 2023 03:14:20 GMT  
		Size: 53.7 MB (53727906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87887f497307d09b7f45dcb424568f2042466bc4ea9b8584b513775f5a376eac`  
		Last Modified: Wed, 01 Mar 2023 03:15:16 GMT  
		Size: 61.6 MB (61600091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713ce2acb08eb0a7bb417c0568fb31388fd14154cf109aa4f7e97de753a867f7`  
		Last Modified: Wed, 01 Mar 2023 03:15:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
