## `clojure:temurin-21-tools-deps-1.11.1.1429-bookworm`

```console
$ docker pull clojure@sha256:59814cf7309d36022aa9d16cc4ed4f2bb5b4df6908437653e773e2b2290d5380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.1.1429-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0f88ddfe77fb525878d5fbf00d9f7274db04bfd0f88cd41b05a1be093cbfc88e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291758012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960902c228b8729effc912da4c3ac4fcb621415c2a3c081d091ba8361f35418e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:51:14 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:51:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:11:10 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:11:10 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:11:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:11:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:11:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:11:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:11:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6c917134ec1d6c9331c8ae8af04565c663063fb65e29c7dae617f6106f7871`  
		Last Modified: Tue, 19 Dec 2023 07:14:38 GMT  
		Size: 158.6 MB (158630566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c02e0798158feea37ccdf27e15fd58590f5679c0bb556428cba10f93671d3c9`  
		Last Modified: Tue, 19 Dec 2023 07:26:42 GMT  
		Size: 83.6 MB (83564852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd1794eebe8c5ab93b947e0888d3d6f736e20687e958e2d67e3b4f962cbb7d4`  
		Last Modified: Tue, 19 Dec 2023 07:26:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db22aa6b5ca2ff5d8700308a3a5c0cb0496ffddd207f7855dc15194350e224aa`  
		Last Modified: Tue, 19 Dec 2023 07:26:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-1.11.1.1429-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:99fb8f85e3556fcfd40413b642e0c58ca59120410890aacabdc287bcebfabfae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289779623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b8ff56cd7e6dc7a022f9c7af04b2c42a8ffc05fb6304b14e971266df52f39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:53:37 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:09:31 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:09:31 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:09:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:09:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:09:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:09:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:09:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1808780032a4c7370b9064c00f6989f956dde542d1e7d624e90bca73cae8b224`  
		Last Modified: Tue, 19 Dec 2023 07:12:31 GMT  
		Size: 156.9 MB (156872127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6421ace190d5b069b21b4b3ba818d87fedafe46fbd63cdb63645ff68beeca5df`  
		Last Modified: Tue, 19 Dec 2023 07:23:20 GMT  
		Size: 83.3 MB (83314222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc55412c152fb05518cb52e43553ceda6618b5e58f35e15a804a22f7f557c78`  
		Last Modified: Tue, 19 Dec 2023 07:23:13 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a60a0a0addd9d04b10084c7161d01206c94a1d2f0efdd3c348499d30bca184`  
		Last Modified: Tue, 19 Dec 2023 07:23:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
