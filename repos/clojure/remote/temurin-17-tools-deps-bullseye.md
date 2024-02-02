## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:11c967540ec5c018e45b8fbf2adba6f6ffc1d5270c8c67c798dc15d1d16b709e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f44f7830c6e3dfd6b35f08051e750acfbaf4273a6e28163a48491797bc0bf092
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268971174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30adda95151b00662caa727d2bdf30bf5a88f3b7ce6eb4c3b3f984113d35434b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:19:15 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:24:29 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:24:29 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:24:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:24:48 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:24:48 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:24:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:24:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6042788be26bf5907bf073b4e97419650a74e28626818034fb050958a263abc`  
		Last Modified: Fri, 02 Feb 2024 17:36:38 GMT  
		Size: 144.9 MB (144893169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3441a64f8dac055db26dbb37bdbc5e6342ef48456511ac4c3f49fc58db35c5`  
		Last Modified: Fri, 02 Feb 2024 17:39:35 GMT  
		Size: 69.0 MB (69020022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e303a6c2ded009aedd65286eb422039eceb5a4cd8d6f228c978a570bae297b`  
		Last Modified: Fri, 02 Feb 2024 17:39:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df99cca4e7c6edcf009f14fbe2e23bb45967192f5d44004eeb947bd63d944a15`  
		Last Modified: Fri, 02 Feb 2024 17:39:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:abd4fc505e2d3fad8918e19e8e3b53ac6aceecb1af7940843e2e87d1ba818e79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266582663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895389efd82c8cac5a2c40ce597e216ef79c2c5bf27c220e33ed276352739d4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:28:07 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:28:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:32:43 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:32:43 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:32:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:32:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:32:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:32:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:32:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523444442ef38521daa043679e098a4bc371abf52c97c5b3cc69543c2795e1f4`  
		Last Modified: Fri, 02 Feb 2024 08:44:13 GMT  
		Size: 143.7 MB (143720935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b30405651bc4ecb96822fc8aaffd967fe3b4e5cac51c55c8356eef81c90eecb`  
		Last Modified: Fri, 02 Feb 2024 08:46:53 GMT  
		Size: 69.2 MB (69152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a3ab2afd5ffdec03b9395bd40b82a362e19cb29289ff47eab433ada0b345d`  
		Last Modified: Fri, 02 Feb 2024 08:46:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b0c363ef46bc6b1ef04b02d82eb3ff6a0edc0f224c541cdf070bc638ec2059`  
		Last Modified: Fri, 02 Feb 2024 08:46:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
