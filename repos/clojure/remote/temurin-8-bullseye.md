## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:1f067398a4c7f65438f45b749f46585ad3e4e55d27f0b38155473c0b4794dd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2527333fa3c99640b35e4902ee2eb27a3c0ffe67f61efb7af914ba2c9603448a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205878730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aceb2b7cb35c5f06be43042c31fc7a4052badd73ec1dd655f6dc1770646f4dd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 01:05:42 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:05:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:09:45 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Sat, 05 Nov 2022 01:09:45 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:10:01 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 05 Nov 2022 01:10:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 05 Nov 2022 01:10:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f77be6fc7ee7a23862824d57222a5b7aab790f7c035085316a7a705cdf9f3d`  
		Last Modified: Sat, 05 Nov 2022 01:21:48 GMT  
		Size: 103.5 MB (103530617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea595060582b217a97cc6670d5870e0b8b58b3fea9b72e1baee71ed1918d8394`  
		Last Modified: Sat, 05 Nov 2022 01:24:13 GMT  
		Size: 47.3 MB (47301162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a977908c2c4c23a8c72a5b945d2b17e11422cfc68108ee5c071ad2cc2ebb2263`  
		Last Modified: Sat, 05 Nov 2022 01:24:07 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2ca22df56e5e0aff2f8442ba60faee1bb64d608b3b12ec0365b04b97400b60e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203623742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5915ce98b8165d061fb8fb5808e8d77bf85e3b0c0ab58a625b20cbeb9d772f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:07:17 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:07:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:10:45 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Fri, 04 Nov 2022 23:10:45 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:10:58 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 04 Nov 2022 23:10:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 04 Nov 2022 23:10:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee19b345ab323043bdfd21232589344dffd26f964f848e9862ddd6f0d36d3db`  
		Last Modified: Fri, 04 Nov 2022 23:19:59 GMT  
		Size: 102.6 MB (102626601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d45a1c1c838722746a3fbd1f59fa2efd15353dbee4eb14b90a9b0ebcbbfa2a`  
		Last Modified: Fri, 04 Nov 2022 23:21:49 GMT  
		Size: 47.3 MB (47294557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c874e93654a63d62b906150ae326648615cf6f86233d73d11d07105ad783ee2f`  
		Last Modified: Fri, 04 Nov 2022 23:21:44 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
