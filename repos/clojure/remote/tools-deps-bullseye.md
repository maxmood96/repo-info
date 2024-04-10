## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:ded4b5df70931d3f09efddff8bd0a5ac8e2924355cb926ee3817b77e6e3d68fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8a49a9bcfadb0147509b07d030eb0b6c774b84f16990cfa5638474cf2c6a6e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283690516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfd3b5d814f9232a4660ff4f501808bfb31b6c4ddc73c93b48df93bac89f8c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:34:36 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:36:18 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:36:18 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:36:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 06:36:35 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 06:36:35 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:36:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:36:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f0a1ef0e780f189b47b031f3bdc0699b1a799b72984d4e2dd0c6d0fca240b0`  
		Last Modified: Wed, 10 Apr 2024 06:49:46 GMT  
		Size: 159.6 MB (159582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfc4cd73e7b5cc7268a76c0a071cc4c28f1aac56ffdd48d767bca42269df92`  
		Last Modified: Wed, 10 Apr 2024 06:51:24 GMT  
		Size: 69.0 MB (69016367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fad9d2f1619a3991e4d0e4caa0681832f2d46d7f05a7900f15b9d3bd8a6ea2`  
		Last Modified: Wed, 10 Apr 2024 06:51:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dc6a1b5aa817fa540c6eaae02a180522e4d7ae8e9240a539ddca1e1a8b42ed`  
		Last Modified: Wed, 10 Apr 2024 06:51:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:00494831f0dc2e2274249e37ffa22e7fd2b74c226c50ea5a7b3c6ad2dd8a37bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280656575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a13c0bd7bf9aceb64b8cc9c75ba76e473b498dc58cf65a3b5b63528472ddc73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:53:43 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:53:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:55:15 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:55:15 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:55:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 04:55:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 04:55:31 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:55:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:55:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b88278549850c6cc680c4b894d8000cdf9fa49715a77007fd4d704649d6325`  
		Last Modified: Wed, 10 Apr 2024 05:08:15 GMT  
		Size: 157.8 MB (157784648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12619b172bee441346052950227b6a9cd469234eafdd8cb588dc0c3e7b548ba`  
		Last Modified: Wed, 10 Apr 2024 05:09:49 GMT  
		Size: 69.1 MB (69141735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b075eb3f5bc41a77c639b39ce0f4432b1d18d41eb6643cb8481bcbbaf04b9c5`  
		Last Modified: Wed, 10 Apr 2024 05:09:43 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9704369ad70e34c7e4839a63ed6075f3bad20e87e1ddeff0ac12544b545cb9c`  
		Last Modified: Wed, 10 Apr 2024 05:09:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
