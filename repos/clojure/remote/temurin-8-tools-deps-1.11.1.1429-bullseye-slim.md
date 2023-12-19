## `clojure:temurin-8-tools-deps-1.11.1.1429-bullseye-slim`

```console
$ docker pull clojure@sha256:01875b7275adc8eaf26ee86125d41b7598732ab52ebb28fc62ae0e81d239f942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1429-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e10d971f408a43f0fd21017d55809c7b419b54e20b73d7e1f57a94011ef451c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196723514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dc32231a705944ae6a6d19d18688dfdf4f8f65e444c55b57360ee717529e12`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:54:34 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:54:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:58:03 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 06:58:03 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:58:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 06:58:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 06:58:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a81e534e5dbde731b8b44557c08ef958dbcfc1c7d5b67de1bc642afc5613f6`  
		Last Modified: Tue, 19 Dec 2023 07:15:47 GMT  
		Size: 103.6 MB (103598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314f5b577456e6c5221381195f5a47122e50427b4fba06d235000b7dea6867fe`  
		Last Modified: Tue, 19 Dec 2023 07:17:47 GMT  
		Size: 61.7 MB (61706763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ddb7f74dc828f7e3736d8ca95bb27982e21c0f531a16767ce04a04e70190f`  
		Last Modified: Tue, 19 Dec 2023 07:17:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1429-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:06989ee1a34ab96c998be4841680ea9c74670ba45aad29042d47d064392d5e05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194591824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30da67f34c05bd9b645f5590df07da2da78db2da8cc2d1609eba80ea9d96843`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:55:48 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:58:38 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 06:58:38 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:58:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 06:58:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 06:58:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8460c2429b384c138ca104a8d205038e1877169d7a2d55c0430c97fdacb19c12`  
		Last Modified: Tue, 19 Dec 2023 07:13:30 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcec9a7260663a93cbf01951b3be42e1066007d4a4a0cefe8a85b6a1f992399`  
		Last Modified: Tue, 19 Dec 2023 07:15:23 GMT  
		Size: 61.8 MB (61825615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db01b9bec66fe521e186aee48eaa67cd4e7764dd72d0c6846792ac8371e155d2`  
		Last Modified: Tue, 19 Dec 2023 07:15:16 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
