## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:305962a33a252a375a209a352697ce7508a7875da5459e2681c5b07abf226812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e3542f5fe3ed6e5f0cc6dfbb34f7a9b8bbadac8fef59529ccc7747ae998024a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234941231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1154b90895fafaf2c365d984c16c81dad58f9a78c2da824760cba2ccaa9ac1f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:07:49 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:07:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:12:57 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:12:57 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:13:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 03:13:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:13:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:13:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:13:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dee0771562f1b4ec86637223b99c85058c85add467447be5a3635c7d84bfb9`  
		Last Modified: Thu, 28 Mar 2024 03:25:18 GMT  
		Size: 144.9 MB (144893095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d98e8d641dbadaa57dc2e2385d0f0c56067b167687aad607f40abfcddebb06a`  
		Last Modified: Thu, 28 Mar 2024 03:28:18 GMT  
		Size: 58.6 MB (58624629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3654a83050fa8a79c6569de3a8db54360ae4770124b48c143245d72934d123`  
		Last Modified: Thu, 28 Mar 2024 03:28:11 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab0b13eacd71b4bf9a191570f9383cbd3cbc2e18d4aa06a4655e84840f86a1d`  
		Last Modified: Thu, 28 Mar 2024 03:28:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3cd5dc9364e9dd77873ba1406ea8eae093aaee64c8bc1b94c06998f52cd23460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232543850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf9eea35f57d63f8329033a8c9165dfec564b49f97e33bb22da97000bba9234`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:40:27 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:40:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:44:34 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:44:34 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:44:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:44:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:44:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:44:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:44:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357c1070edd1560e2fca055cc1853bc6786248dbfbf2c71f7238747ddd407d1c`  
		Last Modified: Thu, 28 Mar 2024 02:54:36 GMT  
		Size: 143.7 MB (143720921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f05df7dfc4573947c962870d1042d76580b9cbc2adb8dd02b0f08020c076c6`  
		Last Modified: Thu, 28 Mar 2024 02:57:03 GMT  
		Size: 58.8 MB (58750795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd7e7d1f9b6dc0fab97d5331f027220c55ccb84d587b7f406f5dcffe151c567`  
		Last Modified: Thu, 28 Mar 2024 02:56:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bcbe48d651522d8f5811d42744d093d38db9bf2a6a5e3f75b03f8ecdf64a8a`  
		Last Modified: Thu, 28 Mar 2024 02:56:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
