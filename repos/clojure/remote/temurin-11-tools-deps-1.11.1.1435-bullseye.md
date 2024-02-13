## `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye`

```console
$ docker pull clojure@sha256:f4366973d8ac53d02447175efa776d368784aa488dc9246eb08cf8aee086fd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:65f3858208ea9e73ff6fbef5b546c798ab49b5b1781cb1c2942646eb32fa3bd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269372762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337e113b2e3cf68fe84218c68a05a6f27a551754ca7843d9f9935b40778450af`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:53:54 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:57:38 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 01:57:38 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:57:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 01:57:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 01:57:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281fd91f06e23fb8bb875dacdbb6833a4d72153ad3b5edf098143c2f04ff19a3`  
		Last Modified: Tue, 13 Feb 2024 02:13:32 GMT  
		Size: 145.3 MB (145271028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c9e6f2449075c2cea24ff728d43e4745f071e2df5ef952e4ba621a86751401`  
		Last Modified: Tue, 13 Feb 2024 02:15:40 GMT  
		Size: 69.0 MB (69016280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9081d7d5e5fa5f4b19bc10d94b1960aca9b44a97682239962a1e915b92bf9a1e`  
		Last Modified: Tue, 13 Feb 2024 02:15:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d745561aa90440c364ecbba1e37437f2dd078c25bad73471398abaeab662ef24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264870077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca6dc0eef5acd585348b88ed221f1f73daf74fc43efe3eeecbe425911f1148e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:00:36 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:03:46 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:03:46 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:04:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:04:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:04:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c186ed2a4be59e96efae471350e604eb9aeb2c333085eb5710177787530416b`  
		Last Modified: Tue, 13 Feb 2024 02:17:46 GMT  
		Size: 142.0 MB (142006384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b160600e399c2c65ddbc9446c42deffbe0e34e3b4bcc7b27d1955d33651fd95c`  
		Last Modified: Tue, 13 Feb 2024 02:19:53 GMT  
		Size: 69.1 MB (69141593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19562ad000e88e9f640e90cc637217de7d1da1d54f53f052ac48d64414b7f2e`  
		Last Modified: Tue, 13 Feb 2024 02:19:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
