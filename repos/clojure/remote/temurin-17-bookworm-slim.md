## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:9a394cd91a8b82aab58b02758a728d14e9d6fd43831b45865d8582b5d15190d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e25ce0b6eb17ec1ba944adfea9c25c5337110260e57aec424de3d9c06f5544c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243110051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccb1130f890e04722bae4564eaba4a0834029827aeebaaa5ef5cb300a84cb45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:18:40 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:18:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:24:05 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:24:05 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:24:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:24:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:24:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:24:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:24:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7efeba6e82ed6b263a3a20620e986ed4521adda8da2894ddc213ef6994c1f`  
		Last Modified: Fri, 02 Feb 2024 17:36:17 GMT  
		Size: 144.9 MB (144893201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0314da12c8d865f748583b3eb9469aba918bda88363a0c3493c32528a69f8c`  
		Last Modified: Fri, 02 Feb 2024 17:39:16 GMT  
		Size: 69.1 MB (69065362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc1cab23d2839d786b4cc59b5bb19b0eb00d35353a321d997cb8cbff437120f`  
		Last Modified: Fri, 02 Feb 2024 17:39:08 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e6c62d699793888851083a2f0c7a5e7f735ca6c2f6c26a658cfd18b460ca17`  
		Last Modified: Fri, 02 Feb 2024 17:39:08 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e0bd7b322c78f66ae22523af0271d64c8b63e9314214f5d9027e7ee1dbb593b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241722605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3cdda907584793289eadb22d54446bfaec19dcc9e2bd088e0715008177c1e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:27:34 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:27:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:32:24 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:32:24 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:32:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:32:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:32:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:32:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:32:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a2971378842cba2355c934edd4fe1c223f5b855eb23918cd0885b86957c0ae`  
		Last Modified: Fri, 02 Feb 2024 08:43:54 GMT  
		Size: 143.7 MB (143720893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ad760237183dd1b1eb7f4287600a3ca76dde3a0d28e9c2f20ae548ce483ddd`  
		Last Modified: Fri, 02 Feb 2024 08:46:36 GMT  
		Size: 68.8 MB (68819861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2929a330c29d663ac66070f91e937baa6b98754c14ad4438abe5dfdcc0f1b2c7`  
		Last Modified: Fri, 02 Feb 2024 08:46:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d951d256000e9903fe5a7688747e03dde965659fb588c38ded16993c87f3c31`  
		Last Modified: Fri, 02 Feb 2024 08:46:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
