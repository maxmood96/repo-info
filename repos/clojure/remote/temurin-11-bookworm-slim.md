## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:79f68f1e803c8ca6bcfc6d57e1ad8309960f8fe5cd05d0191868bcfbf448c1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:66c8ec19be337e7995b7e597fb471303d459ac05fa7c5c697a1b19fec98c4d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246538164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c259ee023eb6cf4a3429caab1d6e4da8d9c946ee4ac4d53e6342ae6973fe6a1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:05 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:02:50 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:02:50 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:03:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:03:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:03:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f381a6c442e4c567d840bbe8d23ac05753126b0641011e48b804c55c4b6c27`  
		Last Modified: Tue, 19 Dec 2023 07:18:32 GMT  
		Size: 145.3 MB (145266436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3a6a300a4a2db2b1400b8f615d981934c98b2137293b7635a9b1ab4f181f72`  
		Last Modified: Tue, 19 Dec 2023 07:20:33 GMT  
		Size: 72.1 MB (72145150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90061e53bf6d242f59a8fdb06e41c2de55151f1a5f11cf3df8660620b65217cb`  
		Last Modified: Tue, 19 Dec 2023 07:20:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc1e976cb4f6019f0b7dbaad934250ac31b519df1a02762cf6ef513f615c7b58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243044101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa3f3c9a15d77b52307b693475deafaa7760d2a302c951e264c156e51e8c68a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:31 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:02:38 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:02:38 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:02:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:02:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:02:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3caa98fe64b6e771f2487121c32bd24ed3c1efe0b70cd6eba73ff5a9db11b6`  
		Last Modified: Tue, 19 Dec 2023 07:16:03 GMT  
		Size: 142.0 MB (142001823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b62dc038e454dd62deaa89190e2c684e8428af57385300c27656f9f9e7bd098`  
		Last Modified: Tue, 19 Dec 2023 07:17:50 GMT  
		Size: 71.9 MB (71884393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbfaec5542c170ab2465f0a0de0004a76cb3dff7891791769508a799d94cd1b`  
		Last Modified: Tue, 19 Dec 2023 07:17:42 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
