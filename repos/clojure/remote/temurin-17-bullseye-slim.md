## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:247b51901c310b79d5c11d231ddb4998abdd1ebc4e565c0849d6ee69535a5ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:343aa65e1048f4493397d0d4c4958b40a62d8fd4b63240ce24e1a981cadae639
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234940970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762b126842285dbef39d08b5d9a25ade5bb105fd58d008147a5bba8418ee3b44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:55:44 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:55:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:07 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 31 Jan 2024 23:59:07 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:59:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 31 Jan 2024 23:59:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 31 Jan 2024 23:59:25 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:59:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:59:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada2cf41cb8c5a69262cd16ed219afecfb15a02b85a90f3f7b04709e0dc6dd35`  
		Last Modified: Thu, 01 Feb 2024 00:13:12 GMT  
		Size: 144.9 MB (144892503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0c2a00f45dd322f90f06ccdc011aae807a99c33a3f7c229f71f5de128a65e9`  
		Last Modified: Thu, 01 Feb 2024 00:15:13 GMT  
		Size: 58.6 MB (58629624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db28bf1a0645086d86cdd1ec7f88d2bca86486001b27486c6fd4e2edc102e7cf`  
		Last Modified: Thu, 01 Feb 2024 00:15:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8525ccc262d11bdb0464ce8a6bbf64567fb95afb7427fba8ccb8a609878e176b`  
		Last Modified: Thu, 01 Feb 2024 00:15:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e0ded67cb0723ec0310d3c667bbdce21790e2e80beb3040ed4b59cb287dc43a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232542864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a95de5e543e506558375cf9646631843009f4d2c98e43020fca538942ff273`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:31:13 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:31:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:34:10 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:34:10 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:34:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:34:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:34:25 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:34:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:34:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772d5b458459761483051b45f421f5aff8c05038820ab7bed52a988cb2718dca`  
		Last Modified: Thu, 01 Feb 2024 06:46:25 GMT  
		Size: 143.7 MB (143720888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc4f954d23756c4d09d8cc4a36791e5b3cb0bcc3e59304599bf4769e0bca8b4`  
		Last Modified: Thu, 01 Feb 2024 06:48:25 GMT  
		Size: 58.8 MB (58756629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6859ebda2c68a8ae4d861f1b80227d23119944c4fe192bcdedba197f8c933fd5`  
		Last Modified: Thu, 01 Feb 2024 06:48:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3ac78365ef754a5d3500b09ae91eb7bff0d2dcc9d42429e300abf51a820eeb`  
		Last Modified: Thu, 01 Feb 2024 06:48:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
