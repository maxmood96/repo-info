## `clojure:temurin-20-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:205462c1e3cda88bb3879ccdf9852d86eff451f8028f35c12c6e47bf44f144de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:62b79e4ac027e0cd314c4f30b675e5931da4463783c60d80ff1fc7ce9a2ee592
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329753526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d69b2a4f7344d43e4470be5720cbf4b73caf01e714bd5483bfe71227f79874`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:08:34 GMT
COPY dir:02736280d197ac4d1b6ebf68d948efb46e7eeffd579505356f8c94946dbcce6f in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:08:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:09:27 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 04 Jul 2023 04:09:27 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:09:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 04 Jul 2023 04:09:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 04 Jul 2023 04:09:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 04 Jul 2023 04:09:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Jul 2023 04:09:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40631d120d49437ca2da3c7f742e7b64c0b6a8d64e2bad614f128909eff12140`  
		Last Modified: Tue, 04 Jul 2023 04:17:05 GMT  
		Size: 202.8 MB (202814014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a62ff0ef2a69a26deb6990dba442383902079dd88835e4d3d987006a7c5abc`  
		Last Modified: Tue, 04 Jul 2023 04:17:46 GMT  
		Size: 71.9 MB (71883199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9ce8b530889b1e7af0e9ad5939e80ae1b6ac9432344b80cf1ae2735e2c5df3`  
		Last Modified: Tue, 04 Jul 2023 04:17:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eff8273119e44870cf49be3794f70f173ae1a835a261218a936406d9707086`  
		Last Modified: Tue, 04 Jul 2023 04:17:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1591bcd964018c0f61d7bb20acdad5917d06b90ee170529eb5181854274afde6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326860213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0b77461398118e973232ac390c99414004e27e21a85443e5b4bbfa11a73c7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jun 2023 04:57:52 GMT
COPY dir:f555428af67a610819205eec573e23f479077e0999818ee9dc0f3375599d21db in /opt/java/openjdk 
# Tue, 13 Jun 2023 04:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:58:42 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 13 Jun 2023 04:58:42 GMT
WORKDIR /tmp
# Tue, 13 Jun 2023 04:58:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Jun 2023 04:58:57 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Jun 2023 04:58:57 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Jun 2023 04:58:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jun 2023 04:58:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7fbc4a56457275b512e08117bbea540a06635c8ef73e73b83254270abe2921`  
		Last Modified: Tue, 13 Jun 2023 05:04:44 GMT  
		Size: 201.2 MB (201158012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40544225a78e0dca4534d195a78b5be0a2312b35b126f85f07da844ef762f49`  
		Last Modified: Tue, 13 Jun 2023 05:05:20 GMT  
		Size: 72.0 MB (71997055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d146f5901339d7ecff55f91a5009b65a0647612eaa9ff702aa8fcfa33cc419`  
		Last Modified: Tue, 13 Jun 2023 05:05:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8fe1e2d1d24d35be647ffa622119b5f884868b6020bf65cca4984cf422581`  
		Last Modified: Tue, 13 Jun 2023 05:05:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
