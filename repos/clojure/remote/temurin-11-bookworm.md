## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:2a17a1c8f74d727c7b03cf8dfca419b84bcf3945a26ff4ac66f04dbb0f2acb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a94b3cf452a12f86d2f14abe7d147671c3609d6bb347ce9d7c6d798d405fbd90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275574646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4265705b5992e72c1101f11c4f9d31e0f2d88df5fa82561213721b782585a8ff`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:19:18 GMT
COPY dir:27feef64ab9493a1c978ebf5ca0dc5d8ce2aa9d0441a77081243d3ab0f99637d in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:19:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:21:48 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:21:48 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:22:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:22:07 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:22:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2383bb2fba492f68230638def29657a1b193de16639ee31045aaa9ce717d0`  
		Last Modified: Wed, 24 Apr 2024 21:43:55 GMT  
		Size: 145.5 MB (145504714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a396e469a54c9b9ec6df5a1022dcd73f691c04967b45f6f34c687487742c980d`  
		Last Modified: Wed, 24 Apr 2024 21:45:52 GMT  
		Size: 80.5 MB (80493030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87aae404215d26f14c63bd279d33775f8ad0f290e61f06156446192ea65bcad4`  
		Last Modified: Wed, 24 Apr 2024 21:45:43 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd57bc890c09d508954a898d3a77f35ba9d39c8ec10d56d9ef9bd3584453e130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272177096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f501e474cccf523d501fb4a2d5993a7cc61cdffc5ea4fe0a3176d6164fc126`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:04:33 GMT
COPY dir:ed1d7b3eb6412a67cc5fb5f9ef1702ecc8bb34e5c226d446c2bffff7a9d8d2bc in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:04:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:06:49 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:06:49 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:07:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:07:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:07:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12591c55ea618c50d976c3e69782f55f21db7a3c276904b0b5228e94ac67b064`  
		Last Modified: Wed, 24 Apr 2024 19:24:42 GMT  
		Size: 142.3 MB (142304377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b55d3c7caea9bc2fdfb1554a56d13dae26da801c1a6d408cb76ac77692b2c81`  
		Last Modified: Wed, 24 Apr 2024 19:26:24 GMT  
		Size: 80.3 MB (80258762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50924107b250179cc21476c9a356ab24735cef2c3d174a11070aabbc21d21f8`  
		Last Modified: Wed, 24 Apr 2024 19:26:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
