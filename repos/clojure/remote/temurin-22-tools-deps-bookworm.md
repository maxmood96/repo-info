## `clojure:temurin-22-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e53c40ce5e8cd03ba50499a6fdf96361548efa75b7c94c9689a9cb0b3bb75918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5547b06be8bede5c18b6729d75c45f489d2ee3acab277d2b0ccd5ce8fa64069c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287950028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96e744bb7325ca83ca5c63cbdea1f0a4d0a2747e76cfef8630f635fb6a969a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 05:19:37 GMT
COPY dir:657bb663bfeaa42d669fabe632e75f73eae3c4aa2d4e78ab7b29311c6e01254d in /opt/java/openjdk 
# Wed, 24 Apr 2024 05:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 05:21:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 05:21:35 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 05:21:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 05:21:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 05:21:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 05:21:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 05:21:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6903d0b90d3010b36564da31fafa94f8d2f4f7e095c382ea65aff2043e5bf995`  
		Last Modified: Wed, 24 Apr 2024 05:36:15 GMT  
		Size: 157.9 MB (157879806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6475a1bcf90e2ce17d0401cc9b2c60e2c7e5c27d2e706d9d3577c8139ad1b8c6`  
		Last Modified: Wed, 24 Apr 2024 05:37:43 GMT  
		Size: 80.5 MB (80492921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0042e1f8e655e0eae83dbdb575d5414f9e43c1c91ee02c3ebbbae20a7e94e60`  
		Last Modified: Wed, 24 Apr 2024 05:37:34 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422533421583841d9858410b1e940b61b85b5792754e9f9103048923b45577b8`  
		Last Modified: Wed, 24 Apr 2024 05:37:34 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0baffcf40cd4a44ef2f3af443c4c3f4990ecfa5631503cf22ae8e0e00a5de34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285734558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5594c699e8080f74fc9712ca955962343d713404c1d7ea0ae9fff016c520a641`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 10:54:56 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 24 Apr 2024 10:55:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 10:56:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 10:56:35 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 10:56:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 10:56:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 10:56:51 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 10:56:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 10:56:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c069d4c96085ab377619d2867ab1b0bf254ae480c4f59184023e7170a9bccc3`  
		Last Modified: Wed, 24 Apr 2024 11:09:28 GMT  
		Size: 155.9 MB (155861707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f5889b20b69b796d16ccf111bbe699a25e27674a56e4cbf73f7d78642558f`  
		Last Modified: Wed, 24 Apr 2024 11:10:46 GMT  
		Size: 80.3 MB (80258493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab670fcd34367f5e9cea79716b7d843602849b90cd7c364507c73c4bf0896106`  
		Last Modified: Wed, 24 Apr 2024 11:10:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879e3f2249d44c59fe24316234eed62ac9e087cf2920fee8cf12c26ab2ad620`  
		Last Modified: Wed, 24 Apr 2024 11:10:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
