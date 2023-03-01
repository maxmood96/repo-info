## `clojure:temurin-19-tools-deps-1.11.1.1224-bullseye-slim`

```console
$ docker pull clojure@sha256:36e7387d04b1f9f386c1efa16f71b31de172ad3a378d47855178e09fe505575a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps-1.11.1.1224-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:98f7a4504ffedcbf108ccdcd19dca357a7434603d68050c36bc386e1c64b6f8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (294011028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecdce9eff07d8d9f15535a69c7e2f82c0818f9c4a6d1fa970b27984208b5b5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:50:20 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:50:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:52:16 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 07:52:16 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:52:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 07:52:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 07:52:33 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 07:52:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 07:52:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b3ccae27fe03c16494d3c8f769e2249b243d16240726cb9587a989c25ac8d0`  
		Last Modified: Wed, 01 Mar 2023 08:01:12 GMT  
		Size: 201.1 MB (201112994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d4575b416cc7cd784218671c89f0d2e0af020d34b57b70e4875ce4a1288ff7`  
		Last Modified: Wed, 01 Mar 2023 08:02:12 GMT  
		Size: 61.5 MB (61485616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccae6b8002aaada90d54ee9ac727171539b9b0f45fee08abbc54f9c09c29dc2`  
		Last Modified: Wed, 01 Mar 2023 08:02:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f376646dfc72121d22e030d5d27f4cfcef9af6adc8e28ad6b338cdea94aeefb`  
		Last Modified: Wed, 01 Mar 2023 08:02:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps-1.11.1.1224-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d976e68825fa6da0c63d92c8537f43503f04f1e0d92ab3f774fa15ef30dc692
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291518922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68113b302051822c132562b39d248e069d23cf5d2ab1ed9e1a6f078d27419f9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:45 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:11:25 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 03:11:25 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:11:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 03:11:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 03:11:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:11:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:11:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee23dab4c9395b25d6fc9f10fb3db021a5fb12f2747057b25dfcd66add5df0fd`  
		Last Modified: Wed, 01 Mar 2023 03:19:32 GMT  
		Size: 199.9 MB (199855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a897effff5e4faec05b07d862da8d6e4a46620fb006c90212daa16952e7c63f5`  
		Last Modified: Wed, 01 Mar 2023 03:20:27 GMT  
		Size: 61.6 MB (61599891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacaf616f58c4cba5b684b65acba9da9ceee2aaf3c5f555ceff284dffbbc62ec`  
		Last Modified: Wed, 01 Mar 2023 03:20:20 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e2d15cbac75204cbfa8e1c89c5876fdba764d00d6abdf4f16e378223f90b84`  
		Last Modified: Wed, 01 Mar 2023 03:20:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
