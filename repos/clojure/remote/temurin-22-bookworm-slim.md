## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:a9c5e70680435af2e476a4201307bc57e876ea2c38d87c351fef0c7d8c3bcd91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6d291c546eb68c5ee0a50e2bbad2977ad73cd1899019431b49446e1513e00bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254734623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f704e0737f4558eb180599d9fe40017df1db84d6f35c1cc6e9daa717c5c88c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d4fcb7cdbe7866a0295c9a8757b5c7002ccf88a8e34edf15f4b703e36029c6`  
		Last Modified: Wed, 29 May 2024 19:59:28 GMT  
		Size: 156.7 MB (156715495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c46edcadb8869266f5baec86e5e66b623e0b8898ab08abdec640f1dd33cdb9`  
		Last Modified: Wed, 29 May 2024 19:59:26 GMT  
		Size: 68.9 MB (68867669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7598f6312138a7790b84128586c6bef68781b6b209c27674afb116c5175e0459`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a51fa6f5b9df47eb62c129ca4c8b33ad8c50bdc9871b43de8925fcce1085be`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9bafd5cbca4d9090d117e97a453ce32338cc6fa94c932771ba310b568a30de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f63dcaadf1867589b54d3315fd1f182e46fd1d34ca6654fd2750e23853cedc7`

```dockerfile
```

-	Layers:
	-	`sha256:c44a582ec21710e7028ceb3c3b87de2dd862cfd8e8edb66c83db883653c2c596`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 4.7 MB (4704933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497950cd243e5b44432af755d5d2582f276b364d86d8534ac057c44bc611bd57`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9ab38f71e0700526de17ada914d6732f40796ff17b3201586f0e0738da40cce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252736563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d153c90fb102db4f15a8f1658ea60681510390ebfcec5bdbc2f3e99bb918298`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:02:15 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:02:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:04:24 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:04:24 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:04:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:04:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:04:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:04:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:04:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0d69f3d78e64bd747e1c78e304dba8ab3618928d50e632af98143081a1774b`  
		Last Modified: Tue, 28 May 2024 20:21:56 GMT  
		Size: 154.7 MB (154737693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8935c09c56ed1f5efe44f0ca7fb12a4e2e4be79a69d7a3ebf2afe22a617bb9`  
		Last Modified: Tue, 28 May 2024 20:23:21 GMT  
		Size: 68.8 MB (68818352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bde09ab23f12a6c627b44611a692efe0ac2b6d14dbe5bbdcb723d306d148ac`  
		Last Modified: Tue, 28 May 2024 20:23:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e051a1be10d6861b8fc7bf690a2425cc754562a17a25ac573ea5ca3eeffa5868`  
		Last Modified: Tue, 28 May 2024 20:23:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
