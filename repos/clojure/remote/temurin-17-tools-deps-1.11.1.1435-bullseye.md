## `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:58c12e691c595be7500117516828c5481964feb96add5402d2cabccd39961f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:97da343cdefe19ec16d84b331558272f36b1375b727738bb24162678872104f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268970124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c116762973e43cb981ab89079aeaf6ab36df6be85eb2c9abc336bc58f74c9d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:55:09 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:58:46 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 31 Jan 2024 23:58:47 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:59:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 31 Jan 2024 23:59:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 31 Jan 2024 23:59:04 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:59:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:59:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56f94c4ac8cf1517e75f20daa59713855b2a987cde3f5a473b73b8fca109c`  
		Last Modified: Thu, 01 Feb 2024 00:12:50 GMT  
		Size: 144.9 MB (144892488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e88d220549e9dc341b669bc62c1a4b03018b821a9f7c3a296f771032ef0f39`  
		Last Modified: Thu, 01 Feb 2024 00:14:53 GMT  
		Size: 69.0 MB (69019653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fde33d304a6dbd6b7678ce0436e96cb82901172e9ba3491e06e72f307c08ed0`  
		Last Modified: Thu, 01 Feb 2024 00:14:45 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca3c6f51573ce4b8a93c4b9a8a9c1745a9ffc8ccf34d4bea7ab879771b0a863`  
		Last Modified: Thu, 01 Feb 2024 00:14:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f9d99325d90d374b8df379c81f668e9ce8f481bdeb445de651391e8b829c040
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266582169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72acf5147301a9a99c018376f82147664e397085876cc3c309b0b3be899e083`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:30:38 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:30:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:33:50 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:33:50 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:34:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:34:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:34:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:34:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:34:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6d482f02e3b5ca72660a5fbf5cf406658f20ae04eec88846601f7517b97b36`  
		Last Modified: Thu, 01 Feb 2024 06:46:07 GMT  
		Size: 143.7 MB (143720894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c528a8789375708bb9e29b95efb8b9395c0e2efda5cb2406227867931e6e5951`  
		Last Modified: Thu, 01 Feb 2024 06:48:06 GMT  
		Size: 69.2 MB (69151991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c124bfc9499c7f689f4af2558077fe6119cb71ab2b92755d26e2310b35549`  
		Last Modified: Thu, 01 Feb 2024 06:47:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ea49d707ba2179834cdbf65ca0113972e574163a1b20e8a14b69ada8c7724e`  
		Last Modified: Thu, 01 Feb 2024 06:47:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
