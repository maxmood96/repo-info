## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:1aac71b82f15b06736a0ef3df341dfee59a5775a618c3aa9a1531696d4d9ce0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2fa8a87375199421ca13fd953af1bf3270b3840a4168f7048a5e69356257792b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb2d408c2bcab154b6a32a59552db65ec583cd0ed685f39225bf5c20f6aa882`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:37:03 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Thu, 02 May 2024 05:37:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:39:22 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:39:22 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:39:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:39:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:39:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:39:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:39:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e2ebb10873bf6b0fa0a37e950a94f94204d5baf185501b3c19be56f8d879f`  
		Last Modified: Thu, 02 May 2024 05:50:22 GMT  
		Size: 145.1 MB (145095178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b6693d1a5048d6c36f5b5352096a8d6b0c825347258d51113fdd309a9de5f`  
		Last Modified: Thu, 02 May 2024 05:52:03 GMT  
		Size: 69.1 MB (69066981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf526ccbc435dfd9fe833124c2c0e16ccb257c782e372f24fb6aadb94e1263e1`  
		Last Modified: Thu, 02 May 2024 05:51:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e08f8ef308ea63a75bf10e1f2390240c92fdc70cecea771a895351d92f565d5`  
		Last Modified: Thu, 02 May 2024 05:51:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b41ff0d75c888d1ec4e8a7c56aa63a0f1efda9b998aff21e20e6de85d78fb1fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c41a067837bae50e0482983b438d34045c580bb94b081ce5afd2ccdf9577c2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:34:25 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Thu, 02 May 2024 05:34:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:36:27 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:36:27 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:36:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:36:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:36:43 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:36:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:36:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff240f07bd7ec84db24ba936652a43f9d5b27137063d0553db4e078bc72c5a3`  
		Last Modified: Thu, 02 May 2024 05:45:43 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a625f7495070a8df25198aa96554cd9086e1e4c06da3731a89e0e49c51111b4`  
		Last Modified: Thu, 02 May 2024 05:47:17 GMT  
		Size: 68.8 MB (68817791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc6348435d390d8f5e811556101b59319929f4c6979f81a48932aa84284a0b7`  
		Last Modified: Thu, 02 May 2024 05:47:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ef6fd90cf947dc8d7b5a859cc33a0c11013e7f548e51c4060e17a3f06d7a36`  
		Last Modified: Thu, 02 May 2024 05:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
