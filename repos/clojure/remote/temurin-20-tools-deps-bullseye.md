## `clojure:temurin-20-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:f5db3bc48860130d08b8b24734c2b1baf5a4a137df5dd51e7b6c99778b5c48f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:453f5fb4f00cb69ba3d7abdcd54204b4a44462e378a0eadcd1e804e3f214c208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329747552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e80dbd0adceb11c7a800dfe53acbf1718cf75c8805a576eeb02045d02d88b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:10:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:13:39 GMT
COPY dir:02736280d197ac4d1b6ebf68d948efb46e7eeffd579505356f8c94946dbcce6f in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:13:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:14:55 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 26 Apr 2023 20:14:55 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:15:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Apr 2023 20:15:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Apr 2023 20:15:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Apr 2023 20:15:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Apr 2023 20:15:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b402b4320892bdb85caa49b18246cc5f2191ea41c99055bf527dec7ff31783`  
		Last Modified: Wed, 26 Apr 2023 20:28:17 GMT  
		Size: 202.8 MB (202814013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bfb893e7a730b769bccbd72b58a99e19c2ee431cfa25b2fd140a8d776eeeb4`  
		Last Modified: Wed, 26 Apr 2023 20:29:22 GMT  
		Size: 71.9 MB (71879787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e87f28b409e6be2f9bf349f8206a06e00021b46855f111f8c6d3accdf47387d`  
		Last Modified: Wed, 26 Apr 2023 20:29:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8a0af7c44ae8d2cf32f0159a99821ddeb38110820fc0c423efd90609a09150`  
		Last Modified: Wed, 26 Apr 2023 20:29:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2a46ddb2afe4e6e0cb592554803f6f57e4a5fc04cd6d623a402e64fefed86b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326848664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a50ff2283eb9bf3624734dd7e3a58794fda505e773df9dfdfef5dc92985d34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:50:56 GMT
COPY dir:f555428af67a610819205eec573e23f479077e0999818ee9dc0f3375599d21db in /opt/java/openjdk 
# Wed, 03 May 2023 17:51:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:51:50 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:51:50 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:52:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:52:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:52:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:52:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:52:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36920479bae8d1066a3a1a6a393a93488050f287679dfa1464398b3e153f95f0`  
		Last Modified: Wed, 03 May 2023 17:58:03 GMT  
		Size: 201.2 MB (201157996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6650c77683c890b8fbe83b4a73896fa6bba8842f9223ebc9fc2dac619cde4751`  
		Last Modified: Wed, 03 May 2023 17:58:38 GMT  
		Size: 72.0 MB (71996947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad42de45609da53011c5000ef9562ee6e29730985f13a78fd6e609e6358cab7`  
		Last Modified: Wed, 03 May 2023 17:58:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6589cf05b54b181cbc924b4a3379165fefa540ceb62131a2874a3d1c7bdb7d67`  
		Last Modified: Wed, 03 May 2023 17:58:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
