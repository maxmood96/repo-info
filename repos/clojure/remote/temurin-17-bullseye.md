## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:ecd3d2ce21e0b20abb2f90038ed581f61622ace6237c81b52d58881aa3cebdc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e08509d405b7da84ba1e68b4d1e502eb5710a2b78dc9eaaa3f4f372929ea8b20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319361737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4e7dbe127251554a806de3423765ac46d776eafe41d9879791ba016a3b3fd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:00:30 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 09:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Mar 2023 19:25:28 GMT
ENV CLOJURE_VERSION=1.11.1.1252
# Tue, 07 Mar 2023 19:25:28 GMT
WORKDIR /tmp
# Tue, 07 Mar 2023 19:25:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "11a5997124d7469578a78f145e68fad6eccd32bf7086979f6abbf19739c85930 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 07 Mar 2023 19:25:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 07 Mar 2023 19:25:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 07 Mar 2023 19:25:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Mar 2023 19:25:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af3cfa1077c96a1e1e95d33920a57958b6fee43d21daec1543eb1ab68b0b9f6`  
		Last Modified: Thu, 02 Mar 2023 09:15:46 GMT  
		Size: 192.4 MB (192438234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fe99b9e752a005bf4e3a73bb5563394a980c1236abd2bf09bcce5c44b819bf`  
		Last Modified: Tue, 07 Mar 2023 19:36:01 GMT  
		Size: 71.9 MB (71876564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fbfb35afdb28ce14fea49e926313664d19849aae294e50fc28adec5d135533`  
		Last Modified: Tue, 07 Mar 2023 19:35:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc950f2c916d69a252b26d19a6a7383145cdd5e73f8393797ddb264a3ef2c0a`  
		Last Modified: Tue, 07 Mar 2023 19:35:53 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e643f3861ac0e2a715f03e78e46a325779cbc8dc696718fed297a36bf3316a80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (316951997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09287918c9e53d3575af911b40b417d92b89adc245718cb85d833a786a5a5a4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:02 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 04:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:57:00 GMT
ENV CLOJURE_VERSION=1.11.1.1252
# Thu, 16 Mar 2023 04:57:00 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 04:57:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "11a5997124d7469578a78f145e68fad6eccd32bf7086979f6abbf19739c85930 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 16 Mar 2023 04:57:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 16 Mar 2023 04:57:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 16 Mar 2023 04:57:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Mar 2023 04:57:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e865ee4af90df7b29aa63a7c22bf36683c14364d7edeb49331fd07b992650cd4`  
		Last Modified: Thu, 16 Mar 2023 05:07:49 GMT  
		Size: 191.3 MB (191260402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45470c04664039616b491b6760986c2dfb8ea1d8f04245389a80d8bd646c24cf`  
		Last Modified: Thu, 16 Mar 2023 05:09:59 GMT  
		Size: 72.0 MB (71987363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58faace382083693705cf995128c628388bfeeb2b688df387adb79123014b69e`  
		Last Modified: Thu, 16 Mar 2023 05:09:52 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210fcc7119e40573da33e1ba3965c195f3f64da74d852c32c74d958ef55f4722`  
		Last Modified: Thu, 16 Mar 2023 05:09:52 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
