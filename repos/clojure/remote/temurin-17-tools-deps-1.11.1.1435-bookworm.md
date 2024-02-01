## `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm`

```console
$ docker pull clojure@sha256:b09cc5b3acf4ee935e71c9bf9bde54154b8ac2185e499c5e94a78dc48260b189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:493038450f64fac572332499c1a84dd23c19204d18aadeb5ddf11543fa6b2d01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274969936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51cd66d2962b033d01d6b0d44739215045669212870bdfabc4be997b24997f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:54:01 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:54:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:57:58 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 31 Jan 2024 23:57:58 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:58:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 31 Jan 2024 23:58:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 31 Jan 2024 23:58:16 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:58:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:58:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905caf01436c21afb3e3cd4e9723995acc020cdcf8335a6ac61199bf19d74e37`  
		Last Modified: Thu, 01 Feb 2024 00:11:59 GMT  
		Size: 144.9 MB (144892527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a5eea4bec907a7c57107bc041729618f1d19d86a2953d7c9a1fddca83aa9d6`  
		Last Modified: Thu, 01 Feb 2024 00:14:15 GMT  
		Size: 80.5 MB (80492638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21476c9cf640a028680727a194e86564b7f38a41cb0005c04e1c51262c98fec0`  
		Last Modified: Thu, 01 Feb 2024 00:14:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1cc4029c5c21d84e2e6e115dc14329b571bdda9ea4e128ed8a7fdcb3a9aad1`  
		Last Modified: Thu, 01 Feb 2024 00:14:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0ab4332413a82b0e9e6f9161e398267e8aabbd01c78a17341297ae0854ebd3cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273596267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d20d2edb89457da4e60b845f359ae6b9201215b49914afee8f4c6a077a6eec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:29:32 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:29:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:33:11 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:33:11 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:33:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:33:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:33:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:33:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:33:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897b1db3cde970641a7e5eb09c234946039c6c77786e114c7eac70c67203419`  
		Last Modified: Thu, 01 Feb 2024 06:45:28 GMT  
		Size: 143.7 MB (143720907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7b3ccbf60f2cc59e37e40650dd5d650b8347946aba083bcfc9a92c3b881ca8`  
		Last Modified: Thu, 01 Feb 2024 06:47:28 GMT  
		Size: 80.3 MB (80259049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fc02e6443bbe7003ca7b7d66b0c39cb17b35f678dd89d82a165d6ee3df8047`  
		Last Modified: Thu, 01 Feb 2024 06:47:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1a6ea5c8b74bf8fbe0edb9d5d5d3dc89e2e4f24ed52f6d5a1e56b472b7db98`  
		Last Modified: Thu, 01 Feb 2024 06:47:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
