## `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm`

```console
$ docker pull clojure@sha256:8b8c136e6cb1af1f9ae013dcc328e8119ca5ecdbe77dbeefe16046452b9948c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4c4a62c6c914d4057fb31043f29ee6734a09b2ad190a9121c514476f62626cfe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274938608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243ffc4126d16a19ac7ea1550ec1768fc90e674399cd71a9867de11246946cc1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:58:26 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:02:33 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:02:33 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:02:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:02:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:02:53 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:02:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:02:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2b2416bddbb63a5143aa0f8648683db64ee3be3e1734dd6322b14594ad178f`  
		Last Modified: Tue, 13 Feb 2024 02:16:23 GMT  
		Size: 144.9 MB (144893174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18e421be8ae63fb12ca245be1e818a0bd755df7d682c89528ddd97ff8891106`  
		Last Modified: Tue, 13 Feb 2024 02:18:34 GMT  
		Size: 80.5 MB (80491813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef89ba6e339caa8618f969bbbd62aed45a91d3296745ffbdca00447a45489e7`  
		Last Modified: Tue, 13 Feb 2024 02:18:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c96260af9a019f5b218439fd7d2f49d8c9c96eaddfa2c9aa9fa8a54004b6ac`  
		Last Modified: Tue, 13 Feb 2024 02:18:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de2ade69c9670eeb87658f00085fab7a6fba5ba0bdb643d94056763bab1b9082
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273568418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227afdeef5188a8e7af2e526a1d42a44a366ff2d1486a8c1a02734c7b4e5cc57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:04:30 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:07:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:07:56 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:08:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:08:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:08:12 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:08:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:08:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26243f51786db2e7088b824a2ea36718e48c26cd4fa4cb18d5b3c2d53b067358`  
		Last Modified: Tue, 13 Feb 2024 02:20:34 GMT  
		Size: 143.7 MB (143720886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143b8e33ba80a1c973cda1e45f17a1e859136ea3b0ecdeaaf893539b4fcc9e5e`  
		Last Modified: Tue, 13 Feb 2024 02:22:34 GMT  
		Size: 80.3 MB (80255553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3a7dc239a53ed488a736ae9ee461048c96ee5e39cb036a2ab5f12d801135f1`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5559e2ffecb5f3fab4d31b9771159c0244f435ff141af726e22dd7de8989a02`  
		Last Modified: Tue, 13 Feb 2024 02:22:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
