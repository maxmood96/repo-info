## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:50fea326231fe7136bb9f8f4053f912ead56ae40d6e72d8d685e6cced2da31ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7abd64d54b446f757e96eea412a2fdbbec32ae8334ca2405c556bb5f5ffed919
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271834201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5a3413ef9a7175f5d486a88019fb260305af0831d8c44143b8e5cef528f2cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 10:02:53 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 10:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:07:51 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 10:07:51 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 10:08:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 10:08:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 10:08:09 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 10:08:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 10:08:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35d66848e01a74b7790ea370bb493db47c5518cd5c088ad8d2bf98e4e7b617`  
		Last Modified: Sat, 02 Dec 2023 10:18:57 GMT  
		Size: 144.9 MB (144873962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa092af82042965bbc8a3be7a0f1a37cad276adf35b35f527fee6565db4fe1e`  
		Last Modified: Sat, 02 Dec 2023 10:21:36 GMT  
		Size: 71.9 MB (71901318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31cdcb13039e000b3199a117be7ef3d9c4a94ada6483a0a6a7496c7baf57dd0`  
		Last Modified: Sat, 02 Dec 2023 10:21:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817dba453c4f78fdc933dcfced8f690904a07eb717b334daa3ae484888109966`  
		Last Modified: Sat, 02 Dec 2023 10:21:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a2a366f349625f782e70ecb1b627b3172b9e44deb879450a07ad25539678316
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269407425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d001a41e2ce240dfd60f2c103ee581c6753fc33567d0db3f799276db4ee105`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:53:59 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:58:32 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 08:58:32 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:58:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 08:58:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 08:58:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 08:58:47 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 08:58:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188efff16de26f2786cfb1a16453748b1bec33191f4cc6735aa049a5a316877e`  
		Last Modified: Sat, 02 Dec 2023 09:08:30 GMT  
		Size: 143.7 MB (143681758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf49daf850ead8e53e8e9fd80661c362149dfd61cfacb64ceb38cfeee6b1ff1`  
		Last Modified: Sat, 02 Dec 2023 09:11:03 GMT  
		Size: 72.0 MB (72016774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa73861c7eb0f9c0442ad29877f90820c6e3109196144bac92679c9fa8bd6cdd`  
		Last Modified: Sat, 02 Dec 2023 09:10:57 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9381eed815a11292b5b3598458631c85234de449c82cdd2775b7815b88e492`  
		Last Modified: Sat, 02 Dec 2023 09:10:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
