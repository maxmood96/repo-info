## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:2724df1c1eeb3121c71c8e15bb92614fd185dad77fabddc9938a9f440abf2efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:feaca8a6d661fcbbf64e1cda575f0baa1c0240365e95700a1114afe0ae634069
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294772073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71198e01543b68abe0531fecd1eadf2ec1c9dce1485f555af1c834e5654a43c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:57:09 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:57:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:59:23 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 17:59:23 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:59:39 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 17:59:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 17:59:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 17:59:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 17:59:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac501d2f56220af0989f4867ddcb859a8c615b98ef9c55c1ea816f6a6ce37930`  
		Last Modified: Tue, 15 Nov 2022 18:10:20 GMT  
		Size: 192.4 MB (192431251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557657e9907e8dd773f515b043fbb052747a7fe6e369ba9ce39b47db098c7923`  
		Last Modified: Tue, 15 Nov 2022 18:11:32 GMT  
		Size: 47.3 MB (47301194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c83ed1e75d2e3b282687514a5f8a4a9756e8613733422a0bf9682652adb619`  
		Last Modified: Tue, 15 Nov 2022 18:11:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ba04b78a6d3d26016b74eb0f456b3ff1fcc5b5f18ff2aa7c9179ed3ee4214b`  
		Last Modified: Tue, 15 Nov 2022 18:11:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d6db592508c27c97770512737338ba738db2dfc108b0922befdbd4889ec987d8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292210500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8720b17c990bff8214950fd96be23df2590c5bcd9e694290898eacf0b06ab983`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:54:01 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:55:57 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:55:57 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:56:08 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:56:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:56:09 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:56:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:56:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee604ee1c814449c1e8223fcbca2cf78c6ba906a0de869dc5ae852d237e22604`  
		Last Modified: Tue, 15 Nov 2022 06:04:50 GMT  
		Size: 191.2 MB (191215218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0060bf4b95513acbfad01dbf987a815fe68a11829f5bcf5cd7e0e297913f89f`  
		Last Modified: Tue, 15 Nov 2022 06:05:52 GMT  
		Size: 47.3 MB (47294403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18110282d264bb7392c8797aa13e3869602b2ad598fb9335fed23dff9b51b333`  
		Last Modified: Tue, 15 Nov 2022 06:05:47 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3968fc50540498fab492f6d75b529e69c6ad17e1437fcd00e256fbf39d965e`  
		Last Modified: Tue, 15 Nov 2022 06:05:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
