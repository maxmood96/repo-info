## `clojure:temurin-11-tools-deps-1.11.1.1347-bullseye`

```console
$ docker pull clojure@sha256:056f235e16c7a0273be0afff35a3c82eba63438d0428e8823ca570b69103d08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1347-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:66bbe2de502f7317d889f1ea17b18a6f1e2184c774f1f48f024d74fac7cbecdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271768346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0acd483bba1aef4bccfd95968a6e77e1ef74f159705d35291eb6d7a48593646`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jul 2023 02:40:54 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Wed, 26 Jul 2023 02:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 02:44:54 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 26 Jul 2023 02:44:54 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 02:45:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Jul 2023 02:45:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Jul 2023 02:45:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973fced5ae624f57d1b1d94457bbc1b8a2cbd2e473cd90b80736c518cf648d50`  
		Last Modified: Wed, 26 Jul 2023 02:49:01 GMT  
		Size: 144.8 MB (144829489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e08cb4f787d4496e88741698f73552863f5018bb4a62ee885256336bcf7f23`  
		Last Modified: Wed, 26 Jul 2023 02:51:13 GMT  
		Size: 71.9 MB (71882940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bce16ea9019cb3017cfb893467c3b0273e48673c19af328cfe57eb57af908c4`  
		Last Modified: Wed, 26 Jul 2023 02:51:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1347-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5f4d2162ff1813e3b8e62bcb5ddd8341c067da5142d122ef6841e89f1426c13f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267271097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50dc13e44a59d1a8e4041871977d3d4f983f6638dc06ed78c150903a47c67d0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jul 2023 01:07:04 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Wed, 26 Jul 2023 01:07:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:10:22 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 26 Jul 2023 01:10:22 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 01:10:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Jul 2023 01:10:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Jul 2023 01:10:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a099a46124988665742eae84cd51e5a2ec69ba12a5a0324bfdecb15c9fcca0ec`  
		Last Modified: Wed, 26 Jul 2023 01:13:29 GMT  
		Size: 141.6 MB (141565305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58edb4e407ccd51ad080d713bda95b42946822fc3c33b86606e7eb074291ae41`  
		Last Modified: Wed, 26 Jul 2023 01:15:08 GMT  
		Size: 72.0 MB (72001196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5dfe25f46e3bf9c1582e348731f7ab1aa6587d265699b3d9da4354dfdd82076`  
		Last Modified: Wed, 26 Jul 2023 01:15:01 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
