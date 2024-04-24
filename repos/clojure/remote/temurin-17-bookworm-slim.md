## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:4d4590a4f25f61cc12842229a3665ffc0fbaa93977b567b3445841c6ac11b793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f67d498200ba34949d1727194234833769c3fd91e2bf209585e2faf598c965fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243109650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29e8b945daf3614e52f9396b5d65bad52ffaa8964e75e6899071fce88c23a63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 05:13:16 GMT
COPY dir:634e6dc1071a76d830a1c58e20efb6c42c0d02beb44d214374fc7817b69efa15 in /opt/java/openjdk 
# Wed, 24 Apr 2024 05:13:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 05:15:14 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 05:15:14 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 05:15:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 05:15:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 05:15:33 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 05:15:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 05:15:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d58f8f8cd59cb957be86a4b302d92b68a4d9510c7530aa568744439259f634`  
		Last Modified: Wed, 24 Apr 2024 05:30:39 GMT  
		Size: 144.9 MB (144893118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5d16022980113adcf1cb3d9a49baeffa501b9d3298f768fe90e1752178ea4b`  
		Last Modified: Wed, 24 Apr 2024 05:32:03 GMT  
		Size: 69.1 MB (69065033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8f7f6948554e364576f4417eef8bd1e3878750d9561a812f16c0fa67535358`  
		Last Modified: Wed, 24 Apr 2024 05:31:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fae81852b7cf9a175e1ba3761df013bccfd1b66cc2ebb0d3ef011595ddb11b`  
		Last Modified: Wed, 24 Apr 2024 05:31:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7296873701957c71e6c0975e052ab1816820cd4673f8923d5a2c5b9c0476e29b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241721597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc31de0d3b2a3996336491cf36a0ec604a46c84eb2fa474b041b5946428985`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 10:49:42 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Wed, 24 Apr 2024 10:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 10:51:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 10:51:15 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 10:51:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 10:51:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 10:51:31 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 10:51:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 10:51:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b85e35b435cc4987fd76ab50a9f1645a606b112a771e65ad34fdb55df26d8`  
		Last Modified: Wed, 24 Apr 2024 11:04:26 GMT  
		Size: 143.7 MB (143720948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a56b09eb6f88e0cedbb563268031dc00c1ea6273161b287b37a61adb0a97777`  
		Last Modified: Wed, 24 Apr 2024 11:05:37 GMT  
		Size: 68.8 MB (68819698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29edcb3d9c84f775a00d080da08f880ea022364c1dcb0ec1bbb5fcd77cc69cb1`  
		Last Modified: Wed, 24 Apr 2024 11:05:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e6ce2f6084ffa2ba10acb8aee1fcdcecb8d109dc79e7f4766b44287c7e96c5`  
		Last Modified: Wed, 24 Apr 2024 11:05:29 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
