## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:7a4ac1cdd695245c24dec07df0b7de334fd438eecc8eac31781571abad28a0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c73a05df86f79aa9eb5fa64f99d1122031f9d889790afa24a1533ea0227e27bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256714982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57334b3d679e250c9de6235f205a3a52275b1f419354c60584a754b0c4efb64e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:29:18 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:29:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:31:33 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:31:33 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:31:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:31:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:31:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:31:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:31:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7462f33b89bb1c152a23b7ab72eed1d7cdb12b31a227633d49c79427162abc`  
		Last Modified: Wed, 24 Apr 2024 21:52:14 GMT  
		Size: 158.5 MB (158498295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fc8e7f8f6a821cff097ff76436aa72b3f72442b18a1303d02f9351bdb08fb9`  
		Last Modified: Wed, 24 Apr 2024 21:54:17 GMT  
		Size: 69.1 MB (69065190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7ba97c22f9f9c13a34409e3676d09168ea74560d37ca4ca540ec358c1de811`  
		Last Modified: Wed, 24 Apr 2024 21:54:08 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326b9e44b2ff8d471d059533e3f125c369c0c7ccf41f2d318248ffc23b0fca0a`  
		Last Modified: Wed, 24 Apr 2024 21:54:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c61052569bdb15cecc6aa30d7e78bb1f060446bb4f20699d5f751ce6699c0600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254666158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db2cc4560f1f1ba7e9067b5bb60328f0c1c11a25047e31435914d6d8c8cb42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:12:51 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:12:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:14:40 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:14:40 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:14:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:14:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:14:56 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:14:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:14:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b59b9a60b19751e0df08713db8963a0fd972e4179b83db306f1cc7095416af7`  
		Last Modified: Wed, 24 Apr 2024 19:32:00 GMT  
		Size: 156.7 MB (156665539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3164d31ad69f932ccc01eb06db9066121c5a1b6e28f6f33793d5baaf35b5f862`  
		Last Modified: Wed, 24 Apr 2024 19:33:44 GMT  
		Size: 68.8 MB (68819668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eac99b7f3e7b97de75a444eff5e7462b85e3e9e5e9ecc4a5cbaabb848f76887`  
		Last Modified: Wed, 24 Apr 2024 19:33:36 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6bea781984e950ae3e91d865d19853492fd6436f43ea3805a1dffda2bb7f72`  
		Last Modified: Wed, 24 Apr 2024 19:33:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
