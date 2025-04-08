## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:66b7b262e5ca5eb4b8d865f4875b6552c55dad51f16332676d4ec5acf508eb54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5be8ca0e44f0209aaa9ce53462dade38636de82a386a1da803421b0e03723339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267710984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbd7a8c59a62b63ce1041d1171c977996cd3f44bbb1f78e353f10215e4c5f2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384928da5074ebbb01e61be8084d664629974b9f4e2c65abbf0cbad3448967e1`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 144.6 MB (144566556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a7b9df872f183423f2c4b5d6ce0e9134e9cf585d55f20e3d004184cf16505`  
		Last Modified: Tue, 08 Apr 2025 01:36:26 GMT  
		Size: 69.4 MB (69394861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dc9a660bf5d24c6933fe2c1ab81ab3865c29b3dc71d8b38a365fb5e8c234`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dace952059d21a364d77d6f9caeb22fd94809b7bcdf8fb098883ee51b17143df`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ac2cfcc388ac2e3a533cf27b960380b839b7a0d1bfb93f4c8f6b9b48f19dc810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1df5e31158cdd29ebdb5129ff5e6d6819d430b131062fa65a2c18ae7d9575a`

```dockerfile
```

-	Layers:
	-	`sha256:e9c0edcd820a05641f5c509f0c0c6b7ad488b956ca1bfcb2a0427ddc2ae6dad6`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 7.2 MB (7206501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54040f0735796fbc8cb3fee9f7a3c6fe8e42465842a4f811b016b12967a9eb8`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e730f54edb093ac35aeafe972e1b4c7bb5db88a96cf72b3035891aa9c5c19d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265009712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b16a71b6c18bcd6598f65952614743aae08ff6dfdfe1018c7c7a9c121b47e6e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac5f7c6c7c6220bb5761ec89c55fd2dae4d63edf89128d22e1e53d7cf650eab`  
		Last Modified: Tue, 18 Mar 2025 00:00:21 GMT  
		Size: 143.5 MB (143454700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba669108d3225511d85e8a7b4114bd355617e38fd3d3faf2d0c6c6f2155fc95`  
		Last Modified: Tue, 18 Mar 2025 00:00:20 GMT  
		Size: 69.3 MB (69305579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7739b9b08896b5308920fc4baeb878f62bc396c89a0a9efc988ec46587f4b9`  
		Last Modified: Tue, 18 Mar 2025 00:00:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddea6b727b379b1dd392fbb22b54f9cdbaf3445cbda0b5c3ed371f1809cee2a`  
		Last Modified: Tue, 18 Mar 2025 00:00:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f162610a6368b7112e5f42b881fc445792f2f777b6c6a7baac9f557e3a5f4c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b48f1b8533a4b9a8b9f372fc3c94265e7580c48f366aa55f2e15fcfbeb2016`

```dockerfile
```

-	Layers:
	-	`sha256:4b40147a6607903040fa0f652ecbb2f5dadae845a6cbfbf0fc20d4403fea1615`  
		Last Modified: Tue, 18 Mar 2025 00:00:18 GMT  
		Size: 7.2 MB (7209654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7968c306ee3c6fe07b9fcac9a3000e3b11707906cf633b79e1f22086aad0123`  
		Last Modified: Tue, 18 Mar 2025 00:00:17 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
