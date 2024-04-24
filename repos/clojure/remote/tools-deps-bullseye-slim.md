## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:7baaf87808a338187eafa4d0c18180e04d25ee3fb20e8e55835595e67e8260b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5fa23a40528704f65e301727f3ba86c707c728de656d46ebe10e285112545886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249643858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4641dbbb4dcbf739bf1466bbcbca0f28b2676e0c312a88667d59f4d4cb3877`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 05:17:30 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 24 Apr 2024 05:17:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 05:19:08 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 05:19:08 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 05:19:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 05:19:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 05:19:25 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 05:19:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 05:19:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0122fb05b50c366de7397728a8413e7060bd93f5939ec27fd1b2258452f7e592`  
		Last Modified: Wed, 24 Apr 2024 05:34:12 GMT  
		Size: 159.6 MB (159582900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa27e3371d54e5925c6b192e52491ca33b3dfc7aa469da0f1d5aa3204d704dc`  
		Last Modified: Wed, 24 Apr 2024 05:35:45 GMT  
		Size: 58.6 MB (58625677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec12eb63fdab5c7fdef5d659640689f87225a3e9c25d895a4932c94374530265`  
		Last Modified: Wed, 24 Apr 2024 05:35:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03acc5b610626d90b7683f3d92e703d8fc4565317184cc563d68acb5d227b855`  
		Last Modified: Wed, 24 Apr 2024 05:35:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4afb1a2e35ca3989d87a0145600e32334d93c8a76124e33c37054cf373f0bad2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246612771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cb8a3cfb019fa4171f942d51d25144311ccbafd362911b80a6399b74523c42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:54:11 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:54:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:55:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:55:35 GMT
WORKDIR /tmp
# Tue, 23 Apr 2024 23:49:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 23 Apr 2024 23:49:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 Apr 2024 23:49:26 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 Apr 2024 23:49:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 Apr 2024 23:49:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b67ff7ac9891011b10ba71782c75705ff5b8eb07e3f792b13082d2a7c3c42`  
		Last Modified: Wed, 10 Apr 2024 05:08:38 GMT  
		Size: 157.8 MB (157784670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0da095ffe333303a150fd212356d9087da69ce9032d81ab929c7690c060fdb`  
		Last Modified: Wed, 24 Apr 2024 00:00:26 GMT  
		Size: 58.8 MB (58750775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20e9fe7a46dd024ebf6e2dd28754664f9f2732f8e26ddb5ad412bdc238e5434`  
		Last Modified: Wed, 24 Apr 2024 00:00:20 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d21371ab5bcde5998bd39ed3bbcc54692d345a48374df2013620956b0f223a3`  
		Last Modified: Wed, 24 Apr 2024 00:00:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
