## `clojure:temurin-21-tools-deps-1.11.1.1435`

```console
$ docker pull clojure@sha256:95e00148a2b558d2e09314d5879292ca2922a6b76e078e6c57f757d1ce1f6ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.1.1435` - linux; amd64

```console
$ docker pull clojure@sha256:aeec843c4088383523cf7d22c2f0281a7555040d3e2e9439c1dc09400ebd8bbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288684758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29acb54001a61a2358e531a94bc4c9fbb5ef7315b894bf0774760d4659b2394`
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
# Thu, 04 Jan 2024 20:51:39 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:51:39 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:51:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:52:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:52:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 04 Jan 2024 20:52:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jan 2024 20:52:00 GMT
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
	-	`sha256:164a9adf5c5b2b6ba5ad5b6b2bac376bd240c1d32dbfe40c6193291026c821b0`  
		Last Modified: Thu, 04 Jan 2024 21:03:22 GMT  
		Size: 80.5 MB (80491597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c83dfd91627ec647f78fc76722300f90031c2cada966e6f604af07195809`  
		Last Modified: Thu, 04 Jan 2024 21:03:08 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b4b77e1fc8abfc33af4ddc0fe476736bb865a04f0e1ee4eaeda03110722889`  
		Last Modified: Thu, 04 Jan 2024 21:03:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-1.11.1.1435` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:95a4634eac96dceb40076f871d56fd7f3ef2230ab7be4dab5912ed712f9b64f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.7 MB (286721050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d02e3f1d1f620fd38d7ecfbdb5cb2958144e7641c5f239429ff81b97bd2fb01`
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
# Thu, 04 Jan 2024 20:49:16 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:49:16 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:49:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:49:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:49:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 04 Jan 2024 20:49:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jan 2024 20:49:33 GMT
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
	-	`sha256:281e98eacf06bee336967a44b4868c4f457091f8352b5f642cf24b6e13fd773f`  
		Last Modified: Thu, 04 Jan 2024 20:59:21 GMT  
		Size: 80.3 MB (80255648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8ef5e66ff789f8cab474f70beaf9000b67aec3bb4117991104952a20502567`  
		Last Modified: Thu, 04 Jan 2024 20:59:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271d535170a82aa9efdce140466c575411acf2256b42d4a605cdcee1ebfb79aa`  
		Last Modified: Thu, 04 Jan 2024 20:59:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
