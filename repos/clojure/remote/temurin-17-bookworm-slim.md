## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:1d56bb141a31fab7c82df1a2abd90b5e7a750833ba07f6073d4333157cfaf460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fffa5eabf131487ebda451cf8602b3daab0d250b9c49ab6e53abc0a3d759e7ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243062981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4bacbb8e109a4621cbfaa61513aebd1019578a0e5f14f5f1ef438f1b277e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:04:16 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:04:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:08:06 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 05:08:06 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:08:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 05:08:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 05:08:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:08:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:08:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f048e54c11677788c22f8c8eb2f24de20279e99d3d9dc508ac867922b77d91ee`  
		Last Modified: Thu, 11 Jan 2024 05:21:33 GMT  
		Size: 144.9 MB (144873944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a350c57e76a9c0ea680f4a9e8476656e13db779a7ae1a90d61be7131fb0133`  
		Last Modified: Thu, 11 Jan 2024 05:23:36 GMT  
		Size: 69.1 MB (69062101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef6e63ab84886f80b812907886f2ee54551dd5406dff456c287b17cce9775ef`  
		Last Modified: Thu, 11 Jan 2024 05:23:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1c350294dac8c61c73b723a2f0040637fcca21cf9978836ef48b2633bce0d5`  
		Last Modified: Thu, 11 Jan 2024 05:23:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b87fd7b809df2560fe52a312ddce9ac051be17964bb7bfb41e1967cbab1f7ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241656801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85f0531a31c9786d5e27eef6c779f8a79adc82a21e67e7e82a4b49ac13fca7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:08 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:47:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:47:36 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:47:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:47:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:47:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 04 Jan 2024 20:47:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jan 2024 20:47:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ee60140f19529393a1624031eddbd14b1675cecae82a1f83a9055965ebb645`  
		Last Modified: Tue, 19 Dec 2023 07:19:05 GMT  
		Size: 143.7 MB (143681714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51f616f46eaa7ea2d6853e9a9b41cea2886273a12845343da6de4823b50d23a`  
		Last Modified: Thu, 04 Jan 2024 20:57:44 GMT  
		Size: 68.8 MB (68816803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e514273521c32196609c1783a1ed3c9172de7dbc949f0e34b8cc54da0b6644`  
		Last Modified: Thu, 04 Jan 2024 20:57:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d606bfaf9d24e7a814c8d2754cff3265893ae657cfbfa607792373b435c620ed`  
		Last Modified: Thu, 04 Jan 2024 20:57:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
