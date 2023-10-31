## `clojure:temurin-11-boot-bookworm`

```console
$ docker pull clojure@sha256:5a2a4d051ac7937e8b6d42cdda86903897a3b344c779a2ef32186b2f2578b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b9609c253a2495dd6c0328f13faa59db5a7a53881a0c1ef5970b05de6ecacd99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259199879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9bb30a1d6c85e4fd3ef46b2e9dbb98d18d704fcc311e1b93fdddcd4f5a9125`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:42:37 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:42:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:42:38 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:42:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:42:39 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:42:45 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:42:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:42:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:43:14 GMT
RUN boot
# Tue, 31 Oct 2023 00:43:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c481232b4dd569227a4027f7e8fe05bdf82df7d8a599bad58c568e75323bbe`  
		Last Modified: Tue, 31 Oct 2023 01:06:42 GMT  
		Size: 145.3 MB (145266640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ec3efceb15b8000ca92d2994e71d75f8747366353840d3808e547b6708605d`  
		Last Modified: Tue, 31 Oct 2023 01:06:31 GMT  
		Size: 5.5 MB (5530321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449a5531acf48c04a282b3184c4481b27137466e0e0753c9481d8ad4354e294e`  
		Last Modified: Tue, 31 Oct 2023 01:06:34 GMT  
		Size: 58.8 MB (58820694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b88aa77a7cbd3f975662cacb4eb7dbfb706c7be43a32c5c5c07753413dd98bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255788362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d595d127760046d9b3162c178e85dfa6292871d1c95e1c3e867f4cf7bd6cecf`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:56:49 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:56:53 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:56:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:56:53 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:56:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:56:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:56:59 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:57:16 GMT
RUN boot
# Tue, 31 Oct 2023 00:57:16 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c4e8ef7ccc180ff3f55a838440893d12f85b3230824ad344a7d06524ac494`  
		Last Modified: Tue, 31 Oct 2023 01:17:21 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db98416ee0c7296e8974cac3aa3f11f91ded8f4c1dc6672156621817eb61770d`  
		Last Modified: Tue, 31 Oct 2023 01:17:13 GMT  
		Size: 5.4 MB (5353330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edb5d8a139866e5ca8fdd4469863228d46b5431d6335a15c271dbaa35ffba5b`  
		Last Modified: Tue, 31 Oct 2023 01:17:15 GMT  
		Size: 58.8 MB (58820500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
