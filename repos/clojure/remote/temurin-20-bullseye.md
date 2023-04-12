## `clojure:temurin-20-bullseye`

```console
$ docker pull clojure@sha256:f8515c541ce256e086f36cfa2cd82d431df4e6de097c152542fde1898d63670e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0ad828e5cf45af7bb08c23be86ae07b5683e4aa411411129bb7f15f59375e4ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329727342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a49c1c43f1005bd640b46f544e26b73cbacab73bf74084bc5676d20f9f6fec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:16:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Apr 2023 00:01:46 GMT
COPY dir:0f9b663d61413099f20817ab55258941c09987290b8ce360d0fb2fab00ddddda in /opt/java/openjdk 
# Tue, 04 Apr 2023 00:01:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Apr 2023 00:03:13 GMT
ENV CLOJURE_VERSION=1.11.1.1267
# Tue, 04 Apr 2023 00:03:13 GMT
WORKDIR /tmp
# Tue, 04 Apr 2023 00:03:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c949c9ba24ee46a2c57c6e6aeff262ebb0ff8112ee2367b3dbabd2f2df75380a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 04 Apr 2023 00:03:29 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 04 Apr 2023 00:03:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 04 Apr 2023 00:03:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Apr 2023 00:03:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e56f75228f4da6333bbfc3af14f6331a1a7e7bf9070b876ad77d0e32e08e28`  
		Last Modified: Tue, 04 Apr 2023 00:11:00 GMT  
		Size: 202.8 MB (202800600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09a5df900d003e57500369b506fcbd4f94a59821ac6e14cb4b0f2713599c1a5`  
		Last Modified: Tue, 04 Apr 2023 00:12:06 GMT  
		Size: 71.9 MB (71880122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad519f8dbc38d2b652895224809ddc359c7cce4b1344729f1cb59d72af4babf4`  
		Last Modified: Tue, 04 Apr 2023 00:11:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba831cda201539a089be02727f56511af4243a5bbaa50086b848f939f0fe385`  
		Last Modified: Tue, 04 Apr 2023 00:11:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23f08b643d1c2b91f802561c885746b3d61f99084feae7f3ea5282a4af74de10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326863382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69aba6931bca4d9c10f20127014807f3b46b7fc31d65c5b692d5556ab43333c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:25:31 GMT
COPY dir:66b65f1974fed4b5bc3675e6b378c93a3ba9feeabfec7eeabd6d1d0b07fd5fa4 in /opt/java/openjdk 
# Wed, 12 Apr 2023 01:25:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 01:26:24 GMT
ENV CLOJURE_VERSION=1.11.1.1267
# Wed, 12 Apr 2023 01:26:25 GMT
WORKDIR /tmp
# Wed, 12 Apr 2023 01:26:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c949c9ba24ee46a2c57c6e6aeff262ebb0ff8112ee2367b3dbabd2f2df75380a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 12 Apr 2023 01:26:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 12 Apr 2023 01:26:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 12 Apr 2023 01:26:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 12 Apr 2023 01:26:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc51dd626337cedfa8259e3da03cef96eece3f3118695f388ae26fd81e82bd`  
		Last Modified: Wed, 12 Apr 2023 01:32:34 GMT  
		Size: 201.2 MB (201160086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148e8e31aea1aeeea95da7fe0d3eaeaafc6d434fc12111027fbbb92da1e8fe67`  
		Last Modified: Wed, 12 Apr 2023 01:33:10 GMT  
		Size: 72.0 MB (71996755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947de9fd2bb8b869ad812a0323142f5099e9f3cc90dcf37adccaf3b90a7d8c16`  
		Last Modified: Wed, 12 Apr 2023 01:33:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420f18bb454dcedac7c33f4ebb076283441960d3a4eda4cd6d230c87c178220a`  
		Last Modified: Wed, 12 Apr 2023 01:33:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
