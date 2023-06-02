## `clojure:temurin-11-tools-deps-1.11.1.1323-bullseye`

```console
$ docker pull clojure@sha256:85c02dd4bf544493241f9140a854d73d3b407d3381011c538cf89058fa50e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1323-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b1896fae0a4935412b417db01ea114ef3003e4888da215b466b1bec3d3878f14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325477390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2143402622738abd638d66b5bc6ec3b2f9239ca6b25ac8e1ad2baddf5177c98`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:07:13 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 08:07:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:09:07 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Tue, 23 May 2023 08:09:07 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:09:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 23 May 2023 08:09:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 May 2023 08:09:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a637a166556170916fb88fe2f41e4f73c2a4d05f0bd97e2366c20d1c5a96c1`  
		Last Modified: Tue, 23 May 2023 08:16:52 GMT  
		Size: 198.5 MB (198549521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad285d6317c2f56b3d3ac83bc9673905cf81b60c0c792667bf8dcffd87378847`  
		Last Modified: Tue, 23 May 2023 08:17:44 GMT  
		Size: 71.9 MB (71878225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1582cb54a003253460673c2b60b2859a05f9e09fce75940916418ea0ec75622`  
		Last Modified: Tue, 23 May 2023 08:17:36 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1323-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b0dc6ca6492fc9010c1072b79ab7aba43970108c98d7cc3a3c4e0bc9e2b8a16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321012441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aff42924dadf9b7ae4b48817d776e2b12cdc02626822f617847434ae69d9f45`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:14:55 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:17:35 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Fri, 02 Jun 2023 01:17:35 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:18:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Jun 2023 01:18:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Jun 2023 01:18:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef10120da7ed1ed5a24c9b69c8e805daf6a8b4d4752ac5ca258e31f04763958f`  
		Last Modified: Fri, 02 Jun 2023 01:24:39 GMT  
		Size: 195.3 MB (195324244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d0c14512f9d630841e7bc886b34e542969f9576cd3453a7ef7651dc57e2324`  
		Last Modified: Fri, 02 Jun 2023 01:26:00 GMT  
		Size: 72.0 MB (71994967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613b0b4c87aaf5a3d06d1ed9c91e63289f3ad3f368bae0deb8fcf4d2a6eec064`  
		Last Modified: Fri, 02 Jun 2023 01:25:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
