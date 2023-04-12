## `clojure:temurin-20-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ae86eacd742dcdbf02ab2a03a067c2eb7592d176c3469aa169835e30e4b0226e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b274f496b2885cee323397e9c428c110899cce5feb8a463397607a31949071ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295708544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d040f2d0466cf1d27b2f3d66836c337043bd5b482d031a6a7c20ba9297c28a5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:17:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Apr 2023 00:02:12 GMT
COPY dir:0f9b663d61413099f20817ab55258941c09987290b8ce360d0fb2fab00ddddda in /opt/java/openjdk 
# Tue, 04 Apr 2023 00:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Apr 2023 00:03:33 GMT
ENV CLOJURE_VERSION=1.11.1.1267
# Tue, 04 Apr 2023 00:03:33 GMT
WORKDIR /tmp
# Tue, 04 Apr 2023 00:03:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c949c9ba24ee46a2c57c6e6aeff262ebb0ff8112ee2367b3dbabd2f2df75380a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 04 Apr 2023 00:03:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 04 Apr 2023 00:03:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 04 Apr 2023 00:03:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Apr 2023 00:03:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1df19d48bc926027d1479479f53957595037adc9dfef4239fddd493092a056`  
		Last Modified: Tue, 04 Apr 2023 00:11:24 GMT  
		Size: 202.8 MB (202800592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7721c2c1e91823b1c2640cafbaf88c1c4b7dff79ef2baaaa3fae1847cca39b6`  
		Last Modified: Tue, 04 Apr 2023 00:12:24 GMT  
		Size: 61.5 MB (61495532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231a9747abfca55b04bf1e055590619280634cb33838cec93e3d212ecfb13f1`  
		Last Modified: Tue, 04 Apr 2023 00:12:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8def1f3b8a55d8d59b2d83917c20fea68662a64aab9f12f2ff34644eb42fb3ed`  
		Last Modified: Tue, 04 Apr 2023 00:12:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:887cd59378a58e56fa37044cee1b17f4a48fb02ca93dcde275f9d6d4afb9bd2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292835396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacac59b916290a3a0e8db1cc3f3e3844cec9261f5f9aacebbe41cf76a937b87`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:25:57 GMT
COPY dir:66b65f1974fed4b5bc3675e6b378c93a3ba9feeabfec7eeabd6d1d0b07fd5fa4 in /opt/java/openjdk 
# Wed, 12 Apr 2023 01:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 01:26:44 GMT
ENV CLOJURE_VERSION=1.11.1.1267
# Wed, 12 Apr 2023 01:26:44 GMT
WORKDIR /tmp
# Wed, 12 Apr 2023 01:26:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c949c9ba24ee46a2c57c6e6aeff262ebb0ff8112ee2367b3dbabd2f2df75380a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 12 Apr 2023 01:26:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 12 Apr 2023 01:26:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 12 Apr 2023 01:26:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 12 Apr 2023 01:26:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ac14b41f3aaaeba0605fc04f599b4365bfd232c1b3f11a8c1c5c7c4cceaa9b`  
		Last Modified: Wed, 12 Apr 2023 01:32:54 GMT  
		Size: 201.2 MB (201160129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efa70c1f1b0b5738ed715809bbd678ad022957dfb4546bdca8c99a56c9c7a24`  
		Last Modified: Wed, 12 Apr 2023 01:33:26 GMT  
		Size: 61.6 MB (61610427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504854ca047e7a125b059e55a0430ee9b90e3b0ae6bc6a79d34b5737d9fbf72e`  
		Last Modified: Wed, 12 Apr 2023 01:33:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c02d605e6116d870b98e71af8686474aede8e1eadb57e7a594b31bd81655818`  
		Last Modified: Wed, 12 Apr 2023 01:33:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
