## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:1ce79e47c70a9eae1d283c8da7f1f3eb6a5b6cc0621ff82ecd98d056b5fc5ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3a2ea4fb2b72c645e8f071a9cbb64705092beb9fe0f89c3b4b59872792cb4440
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268952573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c926b099e7bf554b2eb87c5706ddfb5c8abfab24cca7c76ce17e95da6fc4044`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:04:51 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:04:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:08:30 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 05:08:30 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:08:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 05:08:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 05:08:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:08:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:08:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d0fbad402cd2919fb4faf35c70ab5f613bf878017c5eaf98930d965c12791f`  
		Last Modified: Thu, 11 Jan 2024 05:21:53 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c89d1989a120e98cdf0413f0b57998598d669cc0a44d3ff405b52eeea5f4a61`  
		Last Modified: Thu, 11 Jan 2024 05:23:54 GMT  
		Size: 69.0 MB (69019930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b903d3ae6ea1449f3d8317e405cbc3912d5a22ad60b2b86398e144e23a10d2f2`  
		Last Modified: Thu, 11 Jan 2024 05:23:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316c81c7c83245eb8010e61134556be0587f6c116389daa4bc964e5ca099f1dd`  
		Last Modified: Thu, 11 Jan 2024 05:23:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e43ae895fe0531960a1b319e123e41043e15ebb2e998182cbbbe7da27b99cf88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266542974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47edd2a169325d8111658f1d390963e36032a3f3e605cbe414cdf8bcc61616de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:55:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:36 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:47:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:47:55 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:48:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:48:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:48:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 04 Jan 2024 20:48:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jan 2024 20:48:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd07311e78c2924fc080a1762e027781ac7b4ae611c86133314aba5a664a33ef`  
		Last Modified: Tue, 19 Dec 2023 07:19:23 GMT  
		Size: 143.7 MB (143681714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2b3018807abaff3d44a3f7a3daaa09bb3dc6f3580fca632e31d14f195e4cb4`  
		Last Modified: Thu, 04 Jan 2024 20:58:02 GMT  
		Size: 69.2 MB (69152151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10878d3abae2454b9b78f476a265ecd99f5c43490ee71e95f4f147507c327f45`  
		Last Modified: Thu, 04 Jan 2024 20:57:56 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca2a971367d0a4104c98ada1ef257505233e6cef51352a010cf90c4352c8047`  
		Last Modified: Thu, 04 Jan 2024 20:57:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
