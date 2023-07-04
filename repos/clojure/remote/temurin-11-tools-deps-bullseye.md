## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:1af968b5c723fdd4e2e155bbd7e927e48b674bc7363c6199d090a975600eb10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ac3d44193327e003d2ec4deea9d2e626cf04d7f3b8f7c843f4e4b59e0062bc81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325488224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f1c881eec801f159ee1f873c923e1b8e6d88ba03ef41774a72e090ee5501a6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:03:00 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:03:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:04:59 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 04 Jul 2023 04:04:59 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:05:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 04 Jul 2023 04:05:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 04 Jul 2023 04:05:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b5fb32c7c13fc3044e1370f05931aae1497f5be699a0ec5bf4c0e665c4881`  
		Last Modified: Tue, 04 Jul 2023 04:13:22 GMT  
		Size: 198.5 MB (198549439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680770949965e09b34e4668372e73f0f8018a0a233b4245ded1279daf072555`  
		Last Modified: Tue, 04 Jul 2023 04:14:24 GMT  
		Size: 71.9 MB (71882871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df284f1d8c71ee1daa2d32bfa11d182afe0d6db1fd8380829276e4bae6e2ac0a`  
		Last Modified: Tue, 04 Jul 2023 04:14:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d0ddb40e2c53acee0e8f6ff6e0f03b92d6d4c16e87343f193111f04ed5374d59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321026158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fef85dd39f9713b4750f7976cbe6a58523bc0748f9583390cfdeb001a8975e2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:41:42 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:41:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:45:04 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Fri, 16 Jun 2023 04:45:04 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:45:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 16 Jun 2023 04:45:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 16 Jun 2023 04:45:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b429dc913a313200e2709dc18ae8c848cf538439e00d089ddee5b4541385cd44`  
		Last Modified: Fri, 16 Jun 2023 04:54:03 GMT  
		Size: 195.3 MB (195324188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce07dc32467f92e5ba41096fc7016f698229c4ff9bc5bb53d5dd70e179ab14`  
		Last Modified: Fri, 16 Jun 2023 04:55:46 GMT  
		Size: 72.0 MB (71997218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320b190fa002db47310252255ee4c0785b4997fa31abdfc8cab0dd401f66d898`  
		Last Modified: Fri, 16 Jun 2023 04:55:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
