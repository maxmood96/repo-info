## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:f70e03e9b960c3018f7283ec33c44f0401da809c685a71acd5e8174acf2254be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ca6b000784746a3c0d0b98ccbb5bbb87cb25c608136bdaeb07314c61a85c27ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217491832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea683d28d62b20887cc2bacac7140b7962c9d01d21fe64763f19112f852fe4a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:11:12 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:11:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:11:13 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:11:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:11:13 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:11:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:11:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:11:20 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:11:41 GMT
RUN boot
# Tue, 12 Mar 2024 06:11:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f31bb2ac672ca1059b0a6512d1f8cff2a7c1903786626e25efe760c3e928e3`  
		Last Modified: Tue, 12 Mar 2024 06:34:20 GMT  
		Size: 103.6 MB (103591905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51fe6c1e668f011dc11198e1ceba56b316bcfd3a4418768995ee2d1630f6e35`  
		Last Modified: Tue, 12 Mar 2024 06:34:12 GMT  
		Size: 5.5 MB (5527084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec152c1665dc00614a8f0f660d815f4553137a610c097dd70a7e7dd2f830ec36`  
		Last Modified: Tue, 12 Mar 2024 06:34:14 GMT  
		Size: 58.8 MB (58820647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:579a8b19387eb2c2b7a458d32dfe8f41e325a345d1938751cb62235a7dffb544
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216469932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8541ab45fb550c30744d748d479fd320f96443bfd2d02da3cda31ba3b07aa1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:37:54 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:37:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:37:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:37:56 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:38:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:38:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:38:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:38:47 GMT
RUN boot
# Wed, 10 Apr 2024 04:38:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd52f7c6791dfa000d5ac11d0908c05085ecf85295a21261c6c20087e418c71`  
		Last Modified: Wed, 10 Apr 2024 04:57:52 GMT  
		Size: 102.7 MB (102703042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da262b97ee642e262acb86d92cfb9d898ff56b57c3bf695540df58aa62c1beeb`  
		Last Modified: Wed, 10 Apr 2024 04:57:45 GMT  
		Size: 5.3 MB (5349521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbbfd118b4631cb6862034779e499485b7229ac689d3d1e308975a6f0632efb`  
		Last Modified: Wed, 10 Apr 2024 04:57:47 GMT  
		Size: 58.8 MB (58821104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
