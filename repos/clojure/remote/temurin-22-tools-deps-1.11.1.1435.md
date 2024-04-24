## `clojure:temurin-22-tools-deps-1.11.1.1435`

```console
$ docker pull clojure@sha256:2b2cfe7e151ba8d7a4f2ed2399c12028a8979073928611953f037899fadd939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-1.11.1.1435` - linux; amd64

```console
$ docker pull clojure@sha256:6d11209cc7b369a36f78ed0f512c4db3b1fe8485ed88dd1494c8f06bb33c7161
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286785016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f17b2d7e00301ae107af2cb13dad83db5a7910be8eefdb20b83ec4f2b331d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:33:25 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:33:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:35:47 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:35:47 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:36:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:36:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:36:06 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:36:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:36:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522be7a11b3bc6b464f347d214d53851eff99fc537af85604fa527600fc33d48`  
		Last Modified: Wed, 24 Apr 2024 21:55:51 GMT  
		Size: 156.7 MB (156714950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615905e7cfc40c973437d0b0a0731eda8ae184d69632268cec3c129e872c1a4f`  
		Last Modified: Wed, 24 Apr 2024 21:57:37 GMT  
		Size: 80.5 MB (80492763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6facaaaa1b6b7b100cbe02c43ce8f4cde6b32a1808295d1336ab617e4ae1eebe`  
		Last Modified: Wed, 24 Apr 2024 21:57:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76165b98dd97612b4cf7b582550399e82e9f75986c0a8738cde80b8cc6b93f`  
		Last Modified: Wed, 24 Apr 2024 21:57:28 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-1.11.1.1435` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74ef4b63e03d56244c2e7d3b108a6ab9ff73f775ba4b1b3d5312716f3cc7ed45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284610699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303e730ca88a5bab1491660c916162715ce415902238f940f92a261c0998e2df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:15:58 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:17:59 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:17:59 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:18:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:18:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:18:16 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:18:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:18:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76692e349ab3fc28939969feb219a1adc5237e5df9daf81b4b08faa0c3cc5ea`  
		Last Modified: Wed, 24 Apr 2024 19:35:07 GMT  
		Size: 154.7 MB (154737723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8aeea9483b25bbc5030784652f604d708b03b2d88731e10c0e0dbdc4f2b2c87`  
		Last Modified: Wed, 24 Apr 2024 19:36:35 GMT  
		Size: 80.3 MB (80258619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa135ec2c3c0b73c67a475d92d8b6fb35d26101c9fd72b92c461d2e7d0a3f292`  
		Last Modified: Wed, 24 Apr 2024 19:36:26 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8c37a88b47c42bb582b60d8b6d9c864aaf57e5cef445e49504047ed456d324`  
		Last Modified: Wed, 24 Apr 2024 19:36:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
