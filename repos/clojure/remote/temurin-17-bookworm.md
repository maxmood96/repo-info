## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:d79465d62c7adf26bae1d9fbd9447afc6275afe6ca9d60b7433df385dfef41e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1abe1ba8bca817555b0ed3af70d2f9be311a57b2320d9bc321a0bb3ab018ec9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274937963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ab6fbff2fc9cc4788651796da76aef7124efeb28a84e32ee1d693f0d87d174`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:22:32 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:22:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:27:39 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 12 Mar 2024 06:27:39 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:27:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 12 Mar 2024 06:27:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 12 Mar 2024 06:27:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:27:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:27:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d3e1168edecb607a9a702240c3146bfcd248cb8e0072ed8f1b9a687c433b12`  
		Last Modified: Tue, 12 Mar 2024 06:40:32 GMT  
		Size: 144.9 MB (144893222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1626b78c0c8d559eee638050ec5ff47c75c59ede2136cf08a44fbee21d86e0e`  
		Last Modified: Tue, 12 Mar 2024 06:42:29 GMT  
		Size: 80.5 MB (80491530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2e263d6382d5fde1b0bf215ef9b2ad9d7ba12b62cc85994188bbec3419b31d`  
		Last Modified: Tue, 12 Mar 2024 06:42:20 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd32539dd55b96f9760462d05eba1d490720dd3370a9f87a1c1056250ed214df`  
		Last Modified: Tue, 12 Mar 2024 06:42:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a534b64a8ae7d143894437a020b8d021b03bbf4645b2da5916e02c31bd38c16c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273568358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd48e8fb0e7588863e63ac03ecaaf158fba56e965943804224330f998382a5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:38:59 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:39:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:43:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:43:36 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:43:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:43:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:43:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:43:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:43:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a3ab6309e95d793e36791ae047faf4e012dfe9d2c539164c9626d54ab9fced`  
		Last Modified: Thu, 28 Mar 2024 02:53:43 GMT  
		Size: 143.7 MB (143720940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a273fdebc7bc10688c76d51af5130be93c0302a0aef5b2b14005e5d656d73a5a`  
		Last Modified: Thu, 28 Mar 2024 02:56:15 GMT  
		Size: 80.3 MB (80255415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4283fc985b120d7818a96757627d42baffe110c24cbcadd640a7baca0452521f`  
		Last Modified: Thu, 28 Mar 2024 02:56:08 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3271745718495ebd946e11e24b242a9107c0f683b0707e28b27ceedcbc3ad22`  
		Last Modified: Thu, 28 Mar 2024 02:56:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
