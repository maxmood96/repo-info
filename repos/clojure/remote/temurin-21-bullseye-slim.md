## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:27857467544a3703be66507c35c5ce435c680c503ecd494214b7898027a2dc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:84a30e2e6894a3e3537ed026dd798f18db2e4f76c294683eba568d14b839b68e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251755766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8626dd65328526898b9461759fbbcde49933debd5b1e3b731afa86fe3c88169`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:10:43 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:10:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:12:23 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:12:23 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:12:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:12:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:12:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:12:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:12:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3418aa3768f8a1666146d9291b33a8c05371db25e1b2236c0425f14b731d43b0`  
		Last Modified: Tue, 19 Dec 2023 07:26:18 GMT  
		Size: 158.6 MB (158630595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9a1ded4d9e1b5081e0c36ef5b9ccb827eff68f9698c1402d17a3bb937605ca`  
		Last Modified: Tue, 19 Dec 2023 07:27:57 GMT  
		Size: 61.7 MB (61706284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba77587912c77d4773f6e7c55494a9f21bc8e99057c69a005e6f0192d2414d33`  
		Last Modified: Tue, 19 Dec 2023 07:27:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cb27878d54ab2ad7fb635198a3169999849132c4daf78e407c0b878a76ee47`  
		Last Modified: Tue, 19 Dec 2023 07:27:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:576a050e2453f601d54a4ab2d86c276f19857678f4752da20cac5c940a8cf6cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248762037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416be7e1f17aa7b8cc83156029a3bb5230f922791f8b534bf2124baae87814c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:09:07 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:09:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:10:30 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:10:30 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:10:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:10:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:10:45 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:10:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:10:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c125c1ca87fdf704a7b920d25350427184a9cfec1b320aa3f11cdac7f0540885`  
		Last Modified: Tue, 19 Dec 2023 07:22:59 GMT  
		Size: 156.9 MB (156872108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75107dca1f1eb4939b0d4a511bd937a635b97342f69a9906b4d21a4d46fe2ce`  
		Last Modified: Tue, 19 Dec 2023 07:24:31 GMT  
		Size: 61.8 MB (61824860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55545e1cad95f7f8345997d296440b571015a472ee991bbc0c959b74a7dd32d`  
		Last Modified: Tue, 19 Dec 2023 07:24:24 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f04d82ad144833e7bbe985d3de8a9b403cb53f9ebc060d294a7161805da6b6b`  
		Last Modified: Tue, 19 Dec 2023 07:24:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
