## `clojure:temurin-8-tools-deps-1.11.1.1189-bullseye`

```console
$ docker pull clojure@sha256:816ad631e5d80466f9b0f9fb2357aa7a58e339ac45ffcd2b3eb183a365d9ebc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1189-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:914c32f108d9bc659bc3f341fb2d52174035a3fd0b5045d87f22fe3d0fd19480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205870992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8975d11b1f271f9baf465a2300adf3ef419377556b4099935cb8bc9cd980296e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:50:31 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:53:08 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 17:53:08 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:53:24 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 17:53:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 17:53:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc3c1232a71c325547fbbeb2b9de7293ab2fac0425f4b1e29f33f7ba72c3686`  
		Last Modified: Tue, 15 Nov 2022 18:06:30 GMT  
		Size: 103.5 MB (103530622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52f33ee6f3fd29a1586275fb3005b3796899e6f42b84fdc36a51cf4fb299625`  
		Last Modified: Tue, 15 Nov 2022 18:07:30 GMT  
		Size: 47.3 MB (47301139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd93ca725268697e6340bd81426e7165695f7151ef645d7e898901f7f3fcf8`  
		Last Modified: Tue, 15 Nov 2022 18:07:24 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1189-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d486e5df65904d83cad07c36a034848cdaf2a7f2069a3a0a210109d759ae667c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203621454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5fb98a0b8b740ed291b222345cd6d1b93cf8e7c71ef69a4428ab56d3f015ca`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:48:27 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:48:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:50:46 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:50:46 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:50:58 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:50:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:50:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046fabb8a21ba00eac3c1d47151d833a4f75a4a53165082db8407708793358bf`  
		Last Modified: Tue, 15 Nov 2022 06:01:34 GMT  
		Size: 102.6 MB (102626606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38aad5c80862299e4d74ef954bdd6a63df849115429ef5d18ba329020a5ca769`  
		Last Modified: Tue, 15 Nov 2022 06:02:29 GMT  
		Size: 47.3 MB (47294369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b793777a5b5eaa93b2976c9e828eb83425ee2993451fe67c21ecee0ce9d2a`  
		Last Modified: Tue, 15 Nov 2022 06:02:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
