## `clojure:temurin-22-tools-deps`

```console
$ docker pull clojure@sha256:6238f95137cf215cd975ba71323fa1cb5b00e14d7c4d1ea382359e339bd4eded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:6e0d261fac590d6800ddacd0ffb2cd2d4ea160e73a0d7e6a3ea30f21bd2d5cd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286780156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0975b4d1ec8e367eddfc0852a5a821f1972aa751a0300210ca8875c7b165cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:33:25 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:33:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Apr 2024 19:40:07 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:40:07 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:40:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:40:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:40:26 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:40:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:40:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522be7a11b3bc6b464f347d214d53851eff99fc537af85604fa527600fc33d48`  
		Last Modified: Wed, 24 Apr 2024 21:55:51 GMT  
		Size: 156.7 MB (156714950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2250a109b09fa85ec22ff7d866f11953d595405db02248fa7b5dbf03a887c4fd`  
		Last Modified: Thu, 25 Apr 2024 19:58:56 GMT  
		Size: 80.5 MB (80487905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bcd04a51d1d64f2e62cf77f0f254f0ded30e484513a18f3ffab19176fedd27f`  
		Last Modified: Thu, 25 Apr 2024 19:58:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e027aa3c9060e4346a83b23db216f2bcdb37fa9cace70494cd491e3d95bc789`  
		Last Modified: Thu, 25 Apr 2024 19:58:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:95b3175cc9a73d74c197800360a0541743c0a82bf80d4df52a503e289dcfba2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284594858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dbd348fd5295589330cad1617ec98dc09b5ff7960d7f6cdc5e16e810e99b93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:15:58 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Apr 2024 19:56:10 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:56:11 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:56:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:56:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:56:26 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:56:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:56:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76692e349ab3fc28939969feb219a1adc5237e5df9daf81b4b08faa0c3cc5ea`  
		Last Modified: Wed, 24 Apr 2024 19:35:07 GMT  
		Size: 154.7 MB (154737723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7cdf7cf49543eb8b2c0e7044772b137199e9450b0f081a74086b997f77a173`  
		Last Modified: Thu, 25 Apr 2024 20:12:38 GMT  
		Size: 80.2 MB (80242779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506a593c6c046478ba1e3224f13c7a089eee83c4775fc2629da79ce1ebb94d2`  
		Last Modified: Thu, 25 Apr 2024 20:12:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a586720260b1d6808bc0a6ebb7efe213da7bbc49ec7e4945ba876fdaf684351d`  
		Last Modified: Thu, 25 Apr 2024 20:12:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
