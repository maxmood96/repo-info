## `clojure:temurin-21-tools-deps`

```console
$ docker pull clojure@sha256:3469f384c48ca32432f2ed3a6c6a8aaf06d206b4b50f33c48dc81e0ddbcd9022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:ab36a76ea675dbe463b430043f01da8a1ba123e1c1233079325494e24321c517
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288568516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e76064690a2441278c83af9074b49a4a883933854bd0a5c646ce7442411fc5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:12:37 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:12:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:31:09 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:31:09 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:31:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:31:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:31:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:31:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:31:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c6c7005a90bce817446a105fdd2251e1a61cd5b2920bd66991722c9ddab1a8`  
		Last Modified: Wed, 24 Apr 2024 21:39:39 GMT  
		Size: 158.5 MB (158498251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9224183392da87c00f46691f8a92b85dc871882bc47f7f8f793de307b08c31df`  
		Last Modified: Wed, 24 Apr 2024 21:53:49 GMT  
		Size: 80.5 MB (80492962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9865d4c140e748405ac08b27f489f1325a33a6e13c6f35b893cf21e4fa5dd0fd`  
		Last Modified: Wed, 24 Apr 2024 21:53:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01582ffabb2388ff500948bbfef6d78441975263fff3e431ccfb4704b811b88`  
		Last Modified: Wed, 24 Apr 2024 21:53:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a654781168c5e116b8d77c0c303c0099ee68b6b2a25f00245a7286086ced4a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286538340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1700571c55e44bc8db58cacb1b8e4c971cbea67bb94419c3529e056085c70e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 18:58:54 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Wed, 24 Apr 2024 18:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:14:20 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:14:20 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:14:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:14:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:14:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:14:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:14:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169aa930d721e94ed3fa0e531f2c9589622a5daf25bd20ce451e14411686e427`  
		Last Modified: Wed, 24 Apr 2024 19:21:10 GMT  
		Size: 156.7 MB (156665540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a559e600d465fdc80e0348a2faf71137f3c34d1f0f983227ef514d5a4d8f32f5`  
		Last Modified: Wed, 24 Apr 2024 19:33:16 GMT  
		Size: 80.3 MB (80258441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240cf6057235c6e519c07e37591da46080d53662715be2bd98042ef5e8fa4bce`  
		Last Modified: Wed, 24 Apr 2024 19:33:07 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50064d5ed91f850c5defbe77f783e5a863805cdfca34383a176ce17c821a1edf`  
		Last Modified: Wed, 24 Apr 2024 19:33:07 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
