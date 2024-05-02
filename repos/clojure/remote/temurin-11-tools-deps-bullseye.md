## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f76608c62dbabbbdb1f50e59caa9f0c34d117361e314d00ca2917c2e34a2774a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1350a1387c28015eb0a046952c463d0e8d0afd3f08975112b71f165134d897bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269627785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b86bf4d03a86f85528e4ef497f8519c71cd56fee00b7605673a1235c1351fca`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:32:27 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Thu, 02 May 2024 05:32:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:35:04 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:35:04 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:35:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:35:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:35:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c005fad9ea3cfeba5a28e13da195a46a98e42660f37f551fe04643fcdaa5032`  
		Last Modified: Thu, 02 May 2024 05:47:07 GMT  
		Size: 145.5 MB (145504611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86cb881cd5eb78fe7abb0c6e179539091debcff2833c3dbe02990ebf4d81b1b2`  
		Last Modified: Thu, 02 May 2024 05:48:44 GMT  
		Size: 69.0 MB (69023688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112a751135f552ce97c71cdb9ee51a4a683569beb40d96c95b7f8bddb48e74ac`  
		Last Modified: Thu, 02 May 2024 05:48:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:655d0fb2e3334af271e34af78f4e1026297dc82d32fefd90a140da32d3f3e5e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265186253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f27111d5869181857e5d108a6d2b740b07bc0e751d208e1491f5ab1c59a39d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:30:41 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Thu, 02 May 2024 05:30:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:32:48 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:32:48 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:33:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:33:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:33:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb63a17e73f2c260e7ed8f88ab031803b18ea4b4a6053b3c047bb98977116194`  
		Last Modified: Thu, 02 May 2024 05:42:45 GMT  
		Size: 142.3 MB (142304344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922cca5a78d176120e3e86f53be29cc5b7735e71e1db4c98a94077a6ce110050`  
		Last Modified: Thu, 02 May 2024 05:44:13 GMT  
		Size: 69.1 MB (69141333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777c9f5b1779c24cb957be6f34db2e98e3bb493d431e686653903be2a636a500`  
		Last Modified: Thu, 02 May 2024 05:44:07 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
