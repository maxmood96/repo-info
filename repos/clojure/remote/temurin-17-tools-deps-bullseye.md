## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:abaa4689d61ff32e4774e524b381fa04d6d9609566b97b3e0a9773af08092398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:529899c22a1842cd763030eaefc24db149c583cc4fdb4702d5459403aab99617
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271711324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182e2665a16c1f40accf51f21776a269c9cfe7e9897e511de423917ed7830181`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:27:45 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:27:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:29:46 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 20 Sep 2023 07:29:46 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:30:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 20 Sep 2023 07:30:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 20 Sep 2023 07:30:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:30:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:30:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf4a672ed9955378a963316cbf18411e8a03dfdf04af1c6124a50daf2a46955`  
		Last Modified: Wed, 20 Sep 2023 07:37:17 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909e245bed9ab7bd09e063ac9b4408f44c2851292257060257f009777ab3b707`  
		Last Modified: Wed, 20 Sep 2023 07:38:22 GMT  
		Size: 71.9 MB (71877856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2034c9083f1e54cbab1a4d9436c4fd776aef931f762b24452ac5d86d7e4027`  
		Last Modified: Wed, 20 Sep 2023 07:38:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354377d01b80e4fdb79c1bbde7bc5d288dd843e2dedc6d897d41f1864a2dfd61`  
		Last Modified: Wed, 20 Sep 2023 07:38:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:82c33c4a5301d23a4963a7ea8bdab1f3c440ec13b9b3b7d4745ac9d9a6c59432
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269246952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d30541d543f8aef6a7d4100f43bd567da84b1c06bf4c59310f1227290f93a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:09:15 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:10:59 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 09:10:59 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:11:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 09:11:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 09:11:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:11:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:11:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abafe6bd868d46b7ee281876a4f1449b1024ece764bcbdf2e54191d6f14bf0`  
		Last Modified: Thu, 07 Sep 2023 09:17:33 GMT  
		Size: 143.5 MB (143543491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a29ce0ff71ef3a1ba862248f77ff66b1754cc5d563e3a1016567e8b1a9b9949`  
		Last Modified: Thu, 07 Sep 2023 09:18:27 GMT  
		Size: 72.0 MB (71997729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6b33ec5fae9443e460dac69ba151eab124074782e01f1d08212a182928e140`  
		Last Modified: Thu, 07 Sep 2023 09:18:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fd7a6ba259c4bf64f69ac87dc670639b1b2a016c87d9c624e877feb19d1892`  
		Last Modified: Thu, 07 Sep 2023 09:18:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
