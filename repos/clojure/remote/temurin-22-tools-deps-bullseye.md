## `clojure:temurin-22-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7c2e0327b516b8363051932fbb692ade6f7875ca29ca1c1f79ba9d61b9991883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9697dd1fad18b0e5d708e3b41197d0141407790bff0275d2b28cd72859eb93b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280838545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075637a621a26b08723d1b2a647cda3410d47852aee80dce399065d175c98695`
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
# Thu, 25 Apr 2024 19:40:56 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:40:56 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:41:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:41:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:41:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:41:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:41:14 GMT
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
	-	`sha256:3470bd5b2c9b23467aeb350e0d87615d67b23f9e22e048d958a4d46aee681a8f`  
		Last Modified: Thu, 25 Apr 2024 19:59:37 GMT  
		Size: 69.0 MB (69023710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f470e626caea417b38ba0a8b17ca871b5ce4c286496fc2ebbbf40b67f1fdfe80`  
		Last Modified: Thu, 25 Apr 2024 19:59:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1472c20178b68e4826cc7c3a277550e2401cf35a0b05acd9ecd1fd9efe5d38bb`  
		Last Modified: Thu, 25 Apr 2024 19:59:29 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f6c2044b57847e7665a9f19ba9b264f92105c1c5ae4d444ff0ed266e2cf35792
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277619941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c967ce1e76079faac5d0bf93499d4470c3c34319c320288cc1ffa9daa01b377`
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
# Thu, 25 Apr 2024 19:56:50 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:56:50 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:57:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:57:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:57:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:57:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:57:05 GMT
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
	-	`sha256:eb6a3e974a9c0ad28e93c1aa6ff7254e1c05d36e1b1f5528d543e056f1ec4c3c`  
		Last Modified: Thu, 25 Apr 2024 20:13:17 GMT  
		Size: 69.1 MB (69141216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a09264f6127c773eb2397c75bef419b561ee02142f873d134b5050b7d7fa2`  
		Last Modified: Thu, 25 Apr 2024 20:13:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bf400be302ebc639917ac49f6a816edab1af69aee81d430988f9ca29ea66d0`  
		Last Modified: Thu, 25 Apr 2024 20:13:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
