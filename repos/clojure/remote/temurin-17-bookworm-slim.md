## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:b602cf735d1466bf82e033900df8b245bfa8107372af96e70cedcfa4cf733bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e70451fdb0b2f14de122f8e68000a1eea09f0569b96bf323bd5b6f1532176413
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed954eb51aece4359e381b50e686ec8680c9bb098002c95e6e851e037f163f85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:21:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:33:11 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Tue, 28 May 2024 21:33:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:35:57 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:35:57 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:36:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:36:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:36:16 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 21:36:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 21:36:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba54cf2f577f53c4305645867c9e929e115421852f9a8bc5351356d905978b5`  
		Last Modified: Tue, 28 May 2024 21:57:07 GMT  
		Size: 145.1 MB (145095207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1314d7010a3dd51006d6741fbfebe50e358a8a5e5ad825ded5d42df824b7f51`  
		Last Modified: Tue, 28 May 2024 21:58:58 GMT  
		Size: 69.1 MB (69066661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba787d7e85a9daad8c8c0d220f07a8c6cd35ec8e2445e5fe271ffbcb991e1f7e`  
		Last Modified: Tue, 28 May 2024 21:58:49 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1588e2e046a099e72b6c2dc0bfcfede4c1885786e28a9fecc132b8e83275f690`  
		Last Modified: Tue, 28 May 2024 21:58:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b01098be2ae462e801902b59ad32724f21d8b4681aea5649229052ba4628af44
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143c1a9630904da6d7ae933dacc82e9873c0773ec2036b0a2ed01fe80e267d9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:54:57 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:55:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:57:08 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:57:08 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:57:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:57:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:57:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72920bb393b41da798570e0a544fba4a0fc4aee2db82d333d8a4949661635df`  
		Last Modified: Tue, 28 May 2024 20:14:53 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b329ed1bf6490b2ec99df0756cffbfe08add1994636346fb4dd7f664d528815d`  
		Last Modified: Tue, 28 May 2024 20:16:35 GMT  
		Size: 68.8 MB (68818317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a18a35366468e0d3ad2c2ff5a887fcd16c09f5b25079e953734fe783795a4ae`  
		Last Modified: Tue, 28 May 2024 20:16:28 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f7de2aed3cb3683a10c33362cbf02afa3c87bfd146610a10e6d8f73ac52221`  
		Last Modified: Tue, 28 May 2024 20:16:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
