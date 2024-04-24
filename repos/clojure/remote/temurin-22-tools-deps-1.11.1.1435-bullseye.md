## `clojure:temurin-22-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:e5bb17ed3fd7ee3155e3d882ddd268c1bf7e026e9ea95aa4039c1a00e4657018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6fc491768205fd271c0948b4bf92b3a6a264f61752a729feb4a9e509ff775a72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.0 MB (281996722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19668fa4f4e05f3ff546926cf4b4cadb8d7ca3f963d25a0945babd3802bd0c22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 05:20:34 GMT
COPY dir:657bb663bfeaa42d669fabe632e75f73eae3c4aa2d4e78ab7b29311c6e01254d in /opt/java/openjdk 
# Wed, 24 Apr 2024 05:20:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 05:22:24 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 05:22:24 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 05:22:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 05:22:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 05:22:42 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 05:22:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 05:22:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46c160c7ce247b049c1cb67457b314ce47229734601b5607607683aecfadc90`  
		Last Modified: Wed, 24 Apr 2024 05:37:02 GMT  
		Size: 157.9 MB (157879823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2b2e0f019d852bc828fca5f10784f586b258b056c6cc1487f71b941f1d51b5`  
		Last Modified: Wed, 24 Apr 2024 05:38:23 GMT  
		Size: 69.0 MB (69017014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c959dfb66124d56da8eef9932cb073152105f168621c3d2579892204a731de4`  
		Last Modified: Wed, 24 Apr 2024 05:38:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80e8578f936a25174cda6ef1c5fd9b41c34509c07128e27c2a2a51c917919c8`  
		Last Modified: Wed, 24 Apr 2024 05:38:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc6047948444350ab3b1b2a8161048f340452da6a110e25daae4bc2770c84e27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278744650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4294127ccd66498ca89672885763af00c4fecfad782fda178b164f3601c2234b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 10:55:47 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 24 Apr 2024 10:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 10:57:14 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 10:57:14 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 10:57:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 10:57:29 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 10:57:29 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 10:57:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 10:57:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4ebe21f26c045833b1e4df016792b0ceb9f7f12a44488ce95af30cf9554e10`  
		Last Modified: Wed, 24 Apr 2024 11:10:09 GMT  
		Size: 155.9 MB (155861704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d98b1ebd0f567b70f117798589c9104179851e7d7442484c532fa770682b800`  
		Last Modified: Wed, 24 Apr 2024 11:11:23 GMT  
		Size: 69.1 MB (69141969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9639faad589f24df455400b5cab49d34d3b334a666a1ca66fbb12a7b797f00`  
		Last Modified: Wed, 24 Apr 2024 11:11:16 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12887e6d454820115d0410fd4d15fc93a78d37e7640e13e2bf70b284fe051686`  
		Last Modified: Wed, 24 Apr 2024 11:11:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
