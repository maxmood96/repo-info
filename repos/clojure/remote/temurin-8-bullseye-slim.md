## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:a8182eaa54e96cdcec3dd43cf32505ac68d4c98584052f0e9af0b2857ce9ce4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a13bd5e1674c859719ed79e2998c60ff78b996071959f48ca9a1db64b7b15d33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147516274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e961a5988919901ff69bf2708ee4ec0028de4e88e4324318b73eb4451628fec`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:06:08 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:07:59 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 14:07:59 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:08:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 14:08:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 14:08:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2e51264c882c87c91946d030677c2c91c91959e652ff8ca78e35a61148bb39`  
		Last Modified: Sat, 04 Feb 2023 14:20:17 GMT  
		Size: 54.6 MB (54635589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a6d3873823fe8316d0b0e2d14c3b5f0a7586afcc5e635e7e1051a33bd790a3`  
		Last Modified: Sat, 04 Feb 2023 14:21:16 GMT  
		Size: 61.5 MB (61483147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303cd3f7228b9bac0894a90645af1f3c765881631645087ae6a21cc8c31f95e1`  
		Last Modified: Sat, 04 Feb 2023 14:21:09 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5c7aec607063cb25496cd8929e5e47060ab3324a0e750ae4ac99692d5d858d4e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145370658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2fbd4f822e1c2c7532f18d1494cc994885928c2e425bfda242463af072ffc6`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:44:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:03:14 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:03:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:04:49 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 17:04:49 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:05:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 17:05:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 17:05:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728eccb26a7c7b50bd803fa4105ba630442ce5bc87412fd21de9d8e74052ed1e`  
		Last Modified: Sat, 04 Feb 2023 17:15:30 GMT  
		Size: 53.7 MB (53727893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2227955934f175dde12fed291b242614dbff0b4566ad1b827303d291e9f60ec`  
		Last Modified: Sat, 04 Feb 2023 17:16:25 GMT  
		Size: 61.6 MB (61597356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138b2b0f5d8bc6fe96d460097d63a4a15324e07724d873933f3fba95fbff4937`  
		Last Modified: Sat, 04 Feb 2023 17:16:19 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
