## `clojure:tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:1c112ed546dedfeea356e81d7887ed2b8c50c669447ab99b0145faa535f9e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:83ecd9ab703245235fb50ceefedef4825d698a47b65155d75fcafb3d7efdfee6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288563020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43097506ced0e96d99820027871512326d8569ad157d3b9d8a60cbaeb784b098`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:19:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:19:52 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Tue, 28 May 2024 21:19:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:40:12 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:40:12 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:40:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:40:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:40:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 21:40:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 21:40:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7255341ada0815f7050c1e0ff955eeab000d16baf1e3acbd04a06bbf0f8989`  
		Last Modified: Tue, 28 May 2024 21:48:50 GMT  
		Size: 158.5 MB (158498258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa267ef7448abe7ec1a6a7c9b7d0099b22dd529fe96ad31a7ca27112f8bee75`  
		Last Modified: Tue, 28 May 2024 22:02:38 GMT  
		Size: 80.5 MB (80487357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9084b3647849eb218e56dc186ed4f7a6e8303c4717b5e466e73dd0f57ef853`  
		Last Modified: Tue, 28 May 2024 22:02:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c338ed955e2957a511112fbcf29ddacf4e476ef9f0779f60ff8fdab0409d473`  
		Last Modified: Tue, 28 May 2024 22:02:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a0528f9b7f3d6943e12ca0ee7b5f55cf120058c15e0b8f2ea96b66ca00edf24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286526473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96b7291e966cbfd2f1ae09cd5c433792e35fa5258b99b989c3a9a754e03f757`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:43:16 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Tue, 28 May 2024 19:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:00:13 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:00:13 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:00:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:00:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:00:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:00:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:00:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b5a53959bd941f43a1015323f50ba6e3858b9a2fb1453a7b61f9d4dd305dd`  
		Last Modified: Tue, 28 May 2024 20:07:28 GMT  
		Size: 156.7 MB (156665559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b62e43610312180688fdb781d09ac12af09b3aa25978a33a561b99edf580004`  
		Last Modified: Tue, 28 May 2024 20:19:44 GMT  
		Size: 80.2 MB (80246509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8a75eb7f52dee5817e7dd696b1fbb2ec2542bda5c9468d334d08065c0265c7`  
		Last Modified: Tue, 28 May 2024 20:19:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18a8459a26c621024132589b31939e8e551f0de046b47796fe6f53110483ab2`  
		Last Modified: Tue, 28 May 2024 20:19:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
