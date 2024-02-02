## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:3eff7b5f04f840c8f32ea3f5498dd7dee5a1d49e664d28644f146be30898507a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dee6d751bf8a2651c3a0bf1a956f3e71984debaca871cad42b6f1bc725243364
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274972175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acd562d98332ac1c8ea6e57c4bca60dedff971437860d80a5ff61d4cffefb8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:18:01 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:18:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:23:40 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:23:40 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:23:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:23:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:24:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:24:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:24:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e272de56020947d967cc38ae404bdf929ec35fa85009eb7fcaa4a05298c22e`  
		Last Modified: Fri, 02 Feb 2024 17:35:57 GMT  
		Size: 144.9 MB (144893230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90df156cc6e5f4887284e18d56892613238529da6c66bcf843cb918f19381cf`  
		Last Modified: Fri, 02 Feb 2024 17:38:57 GMT  
		Size: 80.5 MB (80494170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc197157918abfffd9f8c3cdc6ab28a5f5a543c0037f85f3d213e676a6479b52`  
		Last Modified: Fri, 02 Feb 2024 17:38:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d58c879de6f88d6168cb99e0bfd744d616eeeb4a6877dc62a7c3aaef21d087`  
		Last Modified: Fri, 02 Feb 2024 17:38:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6bab8999f71ca62ec9ee5fb5b933dbcf0cf0032e0d45a958cccf8d6206e5bfd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273596092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5fc139dad0c1d88d9c708766dbea724a78135538f7ce14000ee4a3248dc590`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:27:01 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:32:04 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:32:04 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:32:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:32:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:32:21 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:32:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:32:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2123fb31cbd519f0e5acdcb92c2fd15e1872407955fb24a687b068c997bb7e12`  
		Last Modified: Fri, 02 Feb 2024 08:43:27 GMT  
		Size: 143.7 MB (143720880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e841d82f894b4893fca08556ac1e99619853728f3040eddb33bde8efa44371`  
		Last Modified: Fri, 02 Feb 2024 08:46:19 GMT  
		Size: 80.3 MB (80258900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353da1825f6fdab184dac3e73749730db6f036c42a907f5840bf35b66fa82e8d`  
		Last Modified: Fri, 02 Feb 2024 08:46:11 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7bb377ef37e10ff1872ef5cdac2d5a73948c05f69887ed4ce3c91a9623b34d`  
		Last Modified: Fri, 02 Feb 2024 08:46:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
