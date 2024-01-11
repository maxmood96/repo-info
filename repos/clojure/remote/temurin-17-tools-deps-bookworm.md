## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:0c996ac093671ed8336848874dc78d7b693a67ee39d66d427a340a90b1537c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b8faace4ff0b8bc70d154cb756e924759abf114bddbaa27d5d6a3cd2824d2be9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274927339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e734ffa8e4fced04d7b61ae9a10a2e0d34cf3d411f21e8ba8bede5046c5ffa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:03:43 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:07:42 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 05:07:42 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:08:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 05:08:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 05:08:01 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:08:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:08:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108338e55df135d6bc601717541883bf916e61c490583967476dc73e4809007f`  
		Last Modified: Thu, 11 Jan 2024 05:21:08 GMT  
		Size: 144.9 MB (144873964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104d46b80396703fd8038deb8b4c1f93d4ca35cb34874c24f54de992b3de48ad`  
		Last Modified: Thu, 11 Jan 2024 05:23:16 GMT  
		Size: 80.5 MB (80490870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c6480ceaf58c590f5c6af754967844a4fae21f996beeca673cd4dcad785087`  
		Last Modified: Thu, 11 Jan 2024 05:23:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ba857901c615012cce068c9839dad13125da2c736ace19430cb992f6a896d3`  
		Last Modified: Thu, 11 Jan 2024 05:23:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4bb192c50df6d224bd27e4b7a70ac3abe0b1443d1ca8a2320c9110a56f0f29e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273530066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c68cbbcd7e85d53b49db84d7d00c7ef80f598c113bf13f8858e4c161d867fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:03:36 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:47:16 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:47:16 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:47:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:47:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:47:33 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 04 Jan 2024 20:47:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jan 2024 20:47:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c921ebaa0e3aa9234b54378bc303467ff63a194e02c492c4836def5239e7f3`  
		Last Modified: Tue, 19 Dec 2023 07:18:48 GMT  
		Size: 143.7 MB (143681701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36973e74e9279927290f2bc0521e347c508f023930c7d0f4b99a8b6be67b1962`  
		Last Modified: Thu, 04 Jan 2024 20:57:27 GMT  
		Size: 80.3 MB (80255093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03041ca8859769275b879f53e0c2f534c2beda1b92caa47b1fe3ed4d2d47fabc`  
		Last Modified: Thu, 04 Jan 2024 20:57:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8604102bfa12c4e0fe359b1b3b92d173265ca323571c510913b162cddf00dc`  
		Last Modified: Thu, 04 Jan 2024 20:57:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
