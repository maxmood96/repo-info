## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:844c2f2a4e637a93c4d918e2e07da3ccb5d578de98cdcf92543a7fba3d409a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:be72343b2be3ef5b09ebd17c3e0a8f72e1a2c50e46b5eb392a820be06f29ea3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274945302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4223fd1931f8ac0604fda9232ba08e1087afb725a0cee67a7d81feb35b366e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:28:24 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:32:29 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:32:29 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 20:29:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 20:29:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 20:29:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 20:29:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 20:29:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b999bb736fb5383b280a1b864a56049c77d7594a2a6e4588d3878a085cd0164`  
		Last Modified: Wed, 10 Apr 2024 06:45:39 GMT  
		Size: 144.9 MB (144893128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8f95508e238c90855e59168186a0e10239b8364dc7a55a1e36d611922df860`  
		Last Modified: Wed, 10 Apr 2024 20:46:07 GMT  
		Size: 80.5 MB (80490797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7e7fbf4b3da6ada20fa61b178d4411dcecf64c74213f905b23e6ede9027ee2`  
		Last Modified: Wed, 10 Apr 2024 20:45:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80845159807b685d75a8ea67474ef1aae9ec13d789926519dc59416865597af2`  
		Last Modified: Wed, 10 Apr 2024 20:45:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f7327220a63b12ae3059917bf16b51cebc4ab9065792ccb820a1c730ec1e5c8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273573498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0bd26c1b15a4b820ad21bb18dc32cb1336e6aea587ad9a64c871e3fa66c041`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:39:54 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:39:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:44:51 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 06:44:52 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:45:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 16 Apr 2024 06:45:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 06:45:08 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:45:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:45:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dcc5b8f551d20033bdca50f902d2c3b3af7fec3505e396be6c53b53c2db834`  
		Last Modified: Tue, 16 Apr 2024 06:56:33 GMT  
		Size: 143.7 MB (143720933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c253996651c9943debb3320d7e64e0f595ba5288d0b5164041ccd2f8c3ca17`  
		Last Modified: Tue, 16 Apr 2024 06:59:09 GMT  
		Size: 80.3 MB (80255282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee9c9a1948a36e8f9839919f1343236d74d4ceb88ad37d603bf5883f74de94f`  
		Last Modified: Tue, 16 Apr 2024 06:59:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3b857b5fc8a09561c0bf3f2a3b87b1df313b6feb4019c22c3c21623db5f187`  
		Last Modified: Tue, 16 Apr 2024 06:59:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
