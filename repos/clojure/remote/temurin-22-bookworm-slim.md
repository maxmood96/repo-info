## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:ce3df6d893aa2fcfc26ad5e83d9ccb21dba579955b4d061e320b5cf2209feb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:56f3d9d7ff7cfbb83a611256da366c053c87b35259f8d5b8327e42183a9b6f5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254931741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3100f24200433cb9de8e58a5d9e2f7da841136ed306ab3529bc3f3da1d98560a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:33:53 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:33:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:36:12 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:36:12 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:36:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:36:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:36:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:36:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:36:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3e6c4954995a12286c7c607c87255b378abd6de9a4684e27b7148dce8802c`  
		Last Modified: Wed, 24 Apr 2024 21:56:15 GMT  
		Size: 156.7 MB (156714969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc21720d62dcdfb5f231be03afcc519235a3b624e4cede4e47069b3c47160f96`  
		Last Modified: Wed, 24 Apr 2024 21:57:58 GMT  
		Size: 69.1 MB (69065273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddfc36e6af81c1c96db10c0f9ccf4bd832da6e892d1e5b4b16ba54a8d54930f`  
		Last Modified: Wed, 24 Apr 2024 21:57:50 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0ca335d56cf6fa162ad7c7bef671bfe2e7fd356de10fa1bc611cd242b7ef9b`  
		Last Modified: Wed, 24 Apr 2024 21:57:50 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a4f8e2f90df6bbcc2c8f59809fa7ad295a6ad9a73692d1479b871054b460baac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252738703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de3fdd9e5e28e96c99b01196d60b68567c98afe0ccc8d35e28e94ff73f73da5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:16:25 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:18:19 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:18:19 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:18:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:18:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:18:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:18:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:18:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcdc808de12c5b13586bf6281d40898af45806fdf28474ab372d97f3940be38`  
		Last Modified: Wed, 24 Apr 2024 19:35:30 GMT  
		Size: 154.7 MB (154737743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14611178c8bbdfd315704cbeca6b7a53a1a5dc12c1686bdd318d1ada176b190`  
		Last Modified: Wed, 24 Apr 2024 19:36:56 GMT  
		Size: 68.8 MB (68820006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7963249eabf4b98b53741f40716e0aa422a2fcb75e1ab359d1a98ce904b95391`  
		Last Modified: Wed, 24 Apr 2024 19:36:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3aa9842ea886d126b7baa851909bbb0d0185ee2ecddc1586a22353f24f1719b`  
		Last Modified: Wed, 24 Apr 2024 19:36:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
