## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:1b2c3348f1afffc23f63f0c539e7097eb013dcf11a828e7bc92c9bc67eea8948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d891264e7386d55b9215fb03d720bd845d047997884be04b52cc2c74d37894d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268994902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3502d776aad8de26bf1e08c65d1df60f4236a0c9ccd43b4a92204b17ec454c5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:22:28 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:26:59 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 16 Feb 2024 05:26:59 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:27:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 16 Feb 2024 05:27:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 16 Feb 2024 05:27:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:27:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:27:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868da7564e4b1e4da0fe7d569a33bd39a03d781e42fcb9924379b0ad8881c350`  
		Last Modified: Fri, 16 Feb 2024 05:37:07 GMT  
		Size: 144.9 MB (144892562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ebbcd2173c43321c35124f4662b1f2e97b56c7cd419026c51992053ccf7f0d`  
		Last Modified: Fri, 16 Feb 2024 05:39:32 GMT  
		Size: 69.0 MB (69016485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716e8c1f55bb4e1cb1b8cddd9c97fd0fe78af892bdfec9475e707bf0e3b48c80`  
		Last Modified: Fri, 16 Feb 2024 05:39:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9094456347cc812a3d43b505701346006b6fecabd1cc780390423e016b62621b`  
		Last Modified: Fri, 16 Feb 2024 05:39:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4ac9dc6b9402476dd33d4c7eab2592223d60127bb1610e0c1f5cf45dd7c5f23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266585118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bcfe3f221b09daf6e245baaf4e5b6fa09cd19f873d4c73fc7c0bd0f47ef3f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:05:36 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:05:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:08:34 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:08:34 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:08:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:08:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:08:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:08:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:08:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b93abada80d7a4cca39f20b2fb149ebf7e2868c862d216131fb6c28cc287e7`  
		Last Modified: Tue, 13 Feb 2024 02:21:10 GMT  
		Size: 143.7 MB (143720884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0879f400ec710b65fe27c5c9d1f958fda93e8c57b34c1f20a5a3ff345dc00a83`  
		Last Modified: Tue, 13 Feb 2024 02:23:12 GMT  
		Size: 69.1 MB (69141735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5468191070e869b5b82a8dd7c0d445490a90789d2d668c3c08219d73e138f6ae`  
		Last Modified: Tue, 13 Feb 2024 02:23:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ff7afc4835558acfbd9af6dc04bf82cf320f71bbc530574f4604711cbd9a6a`  
		Last Modified: Tue, 13 Feb 2024 02:23:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
