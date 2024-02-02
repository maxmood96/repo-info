## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:4151b5fac2cc763e58dfaf16f8f5c317329b678ccdaf91d401334a3b502dfae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e9065c93a2bb4d18dc6a2d9c81f1f3a0d2ddefeb0063c263a1f1b1ad2ecd179b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236211267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47407818727532613757db524fea11c0ea0821b91864d45620668115b15f8b51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:19:49 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:19:51 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:19:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:19:51 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:19:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:19:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:19:56 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:20:14 GMT
RUN boot
# Fri, 02 Feb 2024 17:20:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:20:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:20:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b6457fcb8b0261583156367d4c0b9e3b3d6e192b2ea1b69ebb7fdca7dcfc12`  
		Last Modified: Fri, 02 Feb 2024 17:37:00 GMT  
		Size: 144.9 MB (144893181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c781d08e3383159619d0ba067079d2eac0b2cb6168c58bc13f5eb01abc3aec`  
		Last Modified: Fri, 02 Feb 2024 17:36:48 GMT  
		Size: 1.1 MB (1079476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b37d87fb1586352b179367b9b240b37a87db46a249a46c9171a0c3209600bf`  
		Last Modified: Fri, 02 Feb 2024 17:36:51 GMT  
		Size: 58.8 MB (58820383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b4c40e5494e5a44b039bc83f862b45a83fa9696c39332fad36dfca0e9b3b99`  
		Last Modified: Fri, 02 Feb 2024 17:36:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfe25a39541a7fcaec4158cc38ca5b7e419f59642f6261b919c03025224787f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233672997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e750d35ea8877a9b1133968f71b1461a460e50b35815feb3b3276711bdb53b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:28:41 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:28:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:28:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:28:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:28:44 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:28:50 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:28:50 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:29:07 GMT
RUN boot
# Fri, 02 Feb 2024 08:29:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:29:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:29:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88be844818cddfb9d70282106952cd5c045d860ee8c5e21a6db93d7361155140`  
		Last Modified: Fri, 02 Feb 2024 08:44:30 GMT  
		Size: 143.7 MB (143720879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc83ffd72a1119230d88f5e846d88428c8c4faf0a588b64f1b7eadb1e60607e1`  
		Last Modified: Fri, 02 Feb 2024 08:44:21 GMT  
		Size: 1.1 MB (1066906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf98884b622e1150151ea20b4e18e23389667b68b57764b9594fdfd5d576f94`  
		Last Modified: Fri, 02 Feb 2024 08:44:24 GMT  
		Size: 58.8 MB (58820477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa65afc4212a9fc68bbc41be89e825eecd18452063535dc7f1cf37ae145d8f19`  
		Last Modified: Fri, 02 Feb 2024 08:44:21 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
