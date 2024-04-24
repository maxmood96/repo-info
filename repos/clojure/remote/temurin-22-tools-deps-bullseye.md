## `clojure:temurin-22-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:ff3c8d39859d5e95c51808707e5e3326f02e0cfbbac93c845d274ded3d72eace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7856195474e2247886b03ca432c28d14ccfb97cfcfbaa632d2cb6b76daf3ed6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280831971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac51e47fe5cdc382088e2c6dd057c9d314051dd55a01a5ce25f2bfa82e720dd8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:34:22 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:34:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:36:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:36:36 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:36:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:36:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:36:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:36:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:36:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb42358e05fa354176ec5ba06791568e9c3dedc13064bdb068d9b22ca31665a`  
		Last Modified: Wed, 24 Apr 2024 21:56:37 GMT  
		Size: 156.7 MB (156714948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019e9bbb2adbeedbf1ea1888c5ac24866b67ed8e090a3aaa5ea0e4be11dcb94c`  
		Last Modified: Wed, 24 Apr 2024 21:58:16 GMT  
		Size: 69.0 MB (69017134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3b595124e572ea973944a9e3b40947c12b491f5a1c2d2e53ef6065826e6ca6`  
		Last Modified: Wed, 24 Apr 2024 21:58:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd5d5ab2f6d8e73be18f49bfc726131b7238ac11c42c01abd3bdf86ed7e8ed7`  
		Last Modified: Wed, 24 Apr 2024 21:58:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6637b7c2b6564eadf8af0ac4dabe671427713831b6eea367886d6c608d46b97e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277621047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bfb4aa9561ec5c91b11ae0e6145ee9e22df69dd01dd8b9fdbf121fd3d02918`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:16:53 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:16:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:18:38 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:18:38 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:18:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:18:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:18:53 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:18:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:18:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cf6201046f2875d6045e672651b1f855d08758eea63c0fc68cca7cf15406df`  
		Last Modified: Wed, 24 Apr 2024 19:35:48 GMT  
		Size: 154.7 MB (154737747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c6b0fd426d887b437bfe5ce44a889bcade968264b4b5b3e832cd65c67698e`  
		Last Modified: Wed, 24 Apr 2024 19:37:14 GMT  
		Size: 69.1 MB (69142323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afe6b31a4a34b61867119b85fbe397721cc4fbf80b06193e00d70ae947e4c1d`  
		Last Modified: Wed, 24 Apr 2024 19:37:06 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d6a677b5e91e4550a45b98e7a770d8e7cf26295458d2f5b3997d6048088911`  
		Last Modified: Wed, 24 Apr 2024 19:37:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
