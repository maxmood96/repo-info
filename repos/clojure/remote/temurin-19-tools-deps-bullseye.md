## `clojure:temurin-19-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c3536cf9eb9c9d8b4f6880fad65df639623771649bc1424cef3a3b99178532d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a2047ec70c916a068b2534c9ade0a169e373ae6a30a83ac7411823eb79182869
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303444059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc62db47b47f560da8d8cc34edcc1a97c930161d31d16c3feb3dbb9358748cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 18:00:19 GMT
COPY dir:fef581854733ec7202f8c807463b9e1952aeb6c7a002719c7e54987e50ea4dcb in /opt/java/openjdk 
# Tue, 15 Nov 2022 18:00:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:02:23 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 18:02:23 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 18:02:39 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 18:02:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 18:02:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 18:02:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 18:02:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e73ee1e6eea684a2802365781fb7b0537b3dd818cb1ce939242a8029132be`  
		Last Modified: Tue, 15 Nov 2022 18:12:23 GMT  
		Size: 201.1 MB (201103445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f8014dc6628bdf938bebde789e69615a0e6ebae24cc0f756dc517a0832c27a`  
		Last Modified: Tue, 15 Nov 2022 18:13:39 GMT  
		Size: 47.3 MB (47300985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f214c21dd5810279a7e039aaa1a5173e6fd5aa8b4682400d981460b5634b8c`  
		Last Modified: Tue, 15 Nov 2022 18:13:34 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544c4960ddca5a83d3f0acf0ac5f32c31e6b53fde9fafb2be95eea8739afcf1e`  
		Last Modified: Tue, 15 Nov 2022 18:13:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c56241e09e100d2b7cd029ab0607bca9307c1a600ecae7cb4ef1d3897009994c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300859572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf56b1cdaf56de7538d0f2991fe43ec39e6b88db7806f82e18c9ce00270938`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:56:38 GMT
COPY dir:4138443eebfda1a2a245638d5bb568645bd34d79b66d39a3be31b5ac6b823d6d in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:56:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:58:32 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:58:32 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:58:44 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:58:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:58:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:58:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:58:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fdef0df9660bc53c8d91dc032dd6670451891d34a69da37129f03671d76128`  
		Last Modified: Tue, 15 Nov 2022 06:06:38 GMT  
		Size: 199.9 MB (199864458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca698ea899cc9adf249a47c7830489a6542622f7a22db05cef83f74304de9ee`  
		Last Modified: Tue, 15 Nov 2022 06:07:35 GMT  
		Size: 47.3 MB (47294236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b8914123d7358ca8bf708f4cce10559ae1aef7c9f822b67f9f00531dee36fa`  
		Last Modified: Tue, 15 Nov 2022 06:07:31 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18862e55129df381f5467c7365825133e0f7c7257eef27127def650927627fab`  
		Last Modified: Tue, 15 Nov 2022 06:07:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
