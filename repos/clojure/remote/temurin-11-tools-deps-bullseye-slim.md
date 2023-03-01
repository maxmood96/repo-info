## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:279eb4ae0aaa68456a86e3fdfda823e8293a3fda9c316c1fb377df2b957c9394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:33a1d8feba52995f15f0a3c8585ea64bd3d7421538b54ad3680963a5dfe2cf0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291372960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9a6f457e44010ad2a0ffaa1ee4cadacbf025571efeed34ab6edf2672836cb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:44:16 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:46:13 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 07:46:13 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:46:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 07:46:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 07:46:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56844ef93a6b4ee76d993441c680d901208ad2f1618368d240a20da46ff08911`  
		Last Modified: Wed, 01 Mar 2023 07:57:07 GMT  
		Size: 198.5 MB (198475514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fc029e127ca848226f7a83226586b3995105cb9bafa7b58900b96ce69c8070`  
		Last Modified: Wed, 01 Mar 2023 07:58:06 GMT  
		Size: 61.5 MB (61485426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380432334792909875045e6a54f1f0db49abff4ef893ffb377502c67afdf39b0`  
		Last Modified: Wed, 01 Mar 2023 07:57:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2340e13c19ad889a6c6605c3b5e325830a15dc90239bd0a8061aa0532850811b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286903651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74b918d2fa868318f50cd34a54ef527de14e4b716df04188a9464d4d8c94c9d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:04:34 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:04:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:06:14 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 03:06:14 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:06:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 03:06:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 03:06:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98c705f083b7d7e1bef89e4744939ae93866db4876e439d400bf551560d2010`  
		Last Modified: Wed, 01 Mar 2023 03:16:00 GMT  
		Size: 195.2 MB (195240377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb14ba3d13d34e81970416d9624f9a5930d5a1386cc083b00ea15866a1401b5`  
		Last Modified: Wed, 01 Mar 2023 03:16:54 GMT  
		Size: 61.6 MB (61599842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26eb74084963ffb4fc6c9d4e6c3bee3b7517790706d8e798fb4849438db84cf`  
		Last Modified: Wed, 01 Mar 2023 03:16:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
