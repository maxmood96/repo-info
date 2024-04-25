## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:b61293385968d963e32316ad8768696befa3d52abd8b0194f36780e6941e5223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:63866c041de440194d5a1512182ea0a21536da92327ebd2d49947f76859245f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254933412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef53bf397587f59eb0569b480f9f192f96550822643a253fbf4669a3ba5140aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:33:53 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:33:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Apr 2024 19:40:32 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:40:32 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:40:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:40:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:40:50 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:40:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:40:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3e6c4954995a12286c7c607c87255b378abd6de9a4684e27b7148dce8802c`  
		Last Modified: Wed, 24 Apr 2024 21:56:15 GMT  
		Size: 156.7 MB (156714969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b077efdc049e8c41aca324b1b91347aa0b304763744ac168a6908003e73dd9ba`  
		Last Modified: Thu, 25 Apr 2024 19:59:19 GMT  
		Size: 69.1 MB (69066948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059071b6c70ccece4b6d0a0a914dd88fd2e2a6312939af787af0ddcb8d4eec2d`  
		Last Modified: Thu, 25 Apr 2024 19:59:11 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48e05f97cf3b5ffb9a39a4c8557b1729881e5e9a92cd9b3c7564af3bf5b4726`  
		Last Modified: Thu, 25 Apr 2024 19:59:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da9fd730270ae023da1fa6c8de1846c0cced92e07e24933c97ac63e2d94d66f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252736262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17576fb6e5e9fab518b3aa7fe8dccfef3eefa0c23026670e926c8e37854fd588`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:16:25 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Apr 2024 19:56:30 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:56:30 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:56:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:56:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:56:46 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:56:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:56:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcdc808de12c5b13586bf6281d40898af45806fdf28474ab372d97f3940be38`  
		Last Modified: Wed, 24 Apr 2024 19:35:30 GMT  
		Size: 154.7 MB (154737743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30311c4aed587800402441ef3545ceb8a36bb227dd4e1fe39df212a52e5f12ca`  
		Last Modified: Thu, 25 Apr 2024 20:12:59 GMT  
		Size: 68.8 MB (68817568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f73a05f38bf39f66f920889b320a26e81b12ece8dd669590bf822e8405d4d9`  
		Last Modified: Thu, 25 Apr 2024 20:12:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebcd69cf388254b08b64040a2593a9bec1427229bb393e7f5a02217b65c9b258`  
		Last Modified: Thu, 25 Apr 2024 20:12:52 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
