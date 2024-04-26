## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:5aadc1af5b55e70367c71551447d7c12288571649049d4fb6e1e409ff6d6f64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5450b2b036f5be8d3eb0ba4cc54777f93db743bb4687fda3e80651856031d569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275160609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e4508bae63969e56c4aede1e3945954ea59a269e646d30b0020d9991ca7a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:48:14 GMT
COPY dir:36f5164517b1d083643fb66b5ce80f151a1fd45f701835f30c768c906e72895e in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:48:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:50:37 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 04:50:37 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:50:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 04:50:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 04:50:56 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 04:50:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 04:50:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68f41a200673397f6db72f4f285fb1bd01669f6c938e7545d78f9d2e286d84a`  
		Last Modified: Fri, 26 Apr 2024 05:01:47 GMT  
		Size: 145.1 MB (145095359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4eb3da3c26c261c164e49c23a9f909608b1741914326d5e05dedeb1576e53ef`  
		Last Modified: Fri, 26 Apr 2024 05:03:27 GMT  
		Size: 80.5 MB (80487952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b6c69118c99e6513590438fcba531d703a1655636fc81e3921d5fc6c53d901`  
		Last Modified: Fri, 26 Apr 2024 05:03:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a904872833e4eef3fbef6db0d644b0d4b82735f2bdd92e9fdebeeb9c8f93b81a`  
		Last Modified: Fri, 26 Apr 2024 05:03:18 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44b82a331ddea8352c21194e05b03f75626098eea19771ef7b13083e2efdebce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273749295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b97569efcc47722ecdd66e5e40847f2922dda5b202aa73985ec55939e93a47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:30:13 GMT
COPY dir:c133644f5c07e30ba622e3ac6570b28080cd19be78bf4af55cfe492de2f59b24 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:30:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:32:30 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 01:32:30 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:32:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 01:32:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 01:32:46 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 01:32:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 01:32:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5df1836a504630ec34112f2a10efaf7369ebe2518cad1c1768047705777c1`  
		Last Modified: Fri, 26 Apr 2024 01:41:52 GMT  
		Size: 143.9 MB (143891886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc043728aa74479d5dadc0e9a579560c32a709428899ee511e32b10e8493b5c`  
		Last Modified: Fri, 26 Apr 2024 01:43:36 GMT  
		Size: 80.2 MB (80243052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223ab923aaf492044a71f735f1e5fda60e0887c8bd27dea603efadbafc2acabf`  
		Last Modified: Fri, 26 Apr 2024 01:43:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462235bf81d3a07f88dd97f13d9ff43d9509d99f35e62aae5d351aafa7adde1`  
		Last Modified: Fri, 26 Apr 2024 01:43:29 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
