## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:0ae58806d3209907476ab9fd6e1f12e88d0ed3e9fe796a368f1c17d0a58e1fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c78604ea9c6d5452395cdd28509e5bf7b1794e5bcb06ef893dcec26ed566b05e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234941449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4846715c4dc7c69f9c483388925093a6c15444b668077e835e70179ddd467e92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Fri, 02 Feb 2024 17:24:54 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:24:54 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:25:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:25:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:25:12 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:25:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:25:13 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:cbd570123c67bdde61a6192a89eaf520fec3f157d0df58b78f3eb1ebf457116a`  
		Last Modified: Fri, 02 Feb 2024 17:39:53 GMT  
		Size: 58.6 MB (58629420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95103548dc6d9f29a158be06768d442f97c8bc47398c90a952790e391fa3ac15`  
		Last Modified: Fri, 02 Feb 2024 17:39:46 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8512602613e56399caf7505ac10f7118b70b15175ffa3e5afed0bec0298e39`  
		Last Modified: Fri, 02 Feb 2024 17:39:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9abf59dd2ad6e56d5e7d4693e95197a4f05736258b802ecf08e03641167b1e1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232542465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06ed38a6d78ab811a7efb99569990df0d9e6a616e408fb81c2a549bb8d9d9f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Fri, 02 Feb 2024 08:33:03 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:33:03 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:33:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:33:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:33:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:33:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:33:18 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:29d6c3b6e1fea297f8cf06f6c1fd9ba2e92e4acf832636127b7022f289c49e0b`  
		Last Modified: Fri, 02 Feb 2024 08:47:09 GMT  
		Size: 58.8 MB (58756229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89927a096c3023ab5a6b4ea6b30df6f087477d709338f17746f64768f576b068`  
		Last Modified: Fri, 02 Feb 2024 08:47:03 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa376fdada8bb941e561f66846ef29878eb5d9eece515add1dbf872a6c4aed4`  
		Last Modified: Fri, 02 Feb 2024 08:47:03 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
