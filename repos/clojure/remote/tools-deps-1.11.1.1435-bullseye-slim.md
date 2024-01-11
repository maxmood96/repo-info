## `clojure:tools-deps-1.11.1.1435-bullseye-slim`

```console
$ docker pull clojure@sha256:53bb28c3e711166d4c881988c7b7fb090a44a097fed7d30e30700a6ca16061a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-1.11.1.1435-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:49f952f8e04552df49fdb3debfae75a09765fb8532e1bb54c578deec9d03487b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248678927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19089efaac4b0b247363497ab86fab5c41f0d451ad0cbe95eda04bfe2a7dd16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:10:11 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:10:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:11:51 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 05:11:51 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:12:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 05:12:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 05:12:09 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:12:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:12:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef36e12111e37e575e53c3a23687c816ab06002dbb25a2a5abaeab9e64b9362`  
		Last Modified: Thu, 11 Jan 2024 05:25:51 GMT  
		Size: 158.6 MB (158630540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7272ed467bfe693af1d19a3ce86e1b233d2e79211b02b499c758f850b56121de`  
		Last Modified: Thu, 11 Jan 2024 05:27:31 GMT  
		Size: 58.6 MB (58629417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98641066f7dfda44e0b85952d2869e99dccecdbc4ec354f75a569a0244e5816d`  
		Last Modified: Thu, 11 Jan 2024 05:27:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56149b486462f70c343caebb0a73514dafd69b743e1b3623965d751b9447953`  
		Last Modified: Thu, 11 Jan 2024 05:27:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.11.1.1435-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a94af2a0f699fe22adf1efe905f369723717d7e8ca736cef0b422bbfb38c9b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245693135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947e0c0a20ec991a72229db8269eeed7b258ed6aedf71d983838cfdb2ab83b6a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:09:07 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:09:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:50:14 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:50:14 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:50:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:50:29 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:50:29 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 04 Jan 2024 20:50:29 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jan 2024 20:50:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c125c1ca87fdf704a7b920d25350427184a9cfec1b320aa3f11cdac7f0540885`  
		Last Modified: Tue, 19 Dec 2023 07:22:59 GMT  
		Size: 156.9 MB (156872108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6758c5da0fb2a67c6687d59cfa213cb8a245e5cb693e134f92c848b30495cc71`  
		Last Modified: Thu, 04 Jan 2024 21:00:36 GMT  
		Size: 58.8 MB (58755959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b3f12bf12682e4a606ddb0c34c05e2c5c6aaec4b2149c05618ed7d8602958e`  
		Last Modified: Thu, 04 Jan 2024 21:00:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d9d4ccbbcac2a7bc5b2c363ce51ecb18c4c3f7d6438c8679c4d2eea608f09e`  
		Last Modified: Thu, 04 Jan 2024 21:00:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
