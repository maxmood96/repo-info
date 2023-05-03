## `clojure:temurin-20-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:87b480fef2df934e55410728ccca9c7b1f71ddf7e5c1c3346c6c0b876592fc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:77839a42833725cb0683490a33b7e97e86a098039ce0952bd2512008db9ee129
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329744038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2210ccd2336bbaa14873533e4f0fdcbab1414ac853d4e7333478b965ab6305ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:32:24 GMT
COPY dir:02736280d197ac4d1b6ebf68d948efb46e7eeffd579505356f8c94946dbcce6f in /opt/java/openjdk 
# Wed, 03 May 2023 20:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:33:16 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 20:33:16 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:33:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 20:33:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 20:33:33 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 20:33:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 20:33:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b519f573684f5e9384b4dd8bce8687dcafb967c9c60cf34f85bc177e521ab3c9`  
		Last Modified: Wed, 03 May 2023 20:40:02 GMT  
		Size: 202.8 MB (202813974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e07805a1ff9dfca486ca38df715cf236d644bd85d746b53a7e4c5910b6f2b1`  
		Last Modified: Wed, 03 May 2023 20:40:42 GMT  
		Size: 71.9 MB (71879980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54eb2fa008d987141ee0dbaf1cd9dae7fca69fe88eaee999301838eaa6ed4fa2`  
		Last Modified: Wed, 03 May 2023 20:40:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ddb35f471f6c60922de5e0b426d762ee56ae126af1671e48fedf8d7a832650`  
		Last Modified: Wed, 03 May 2023 20:40:35 GMT  
		Size: 399.0 B  
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
