## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:32276e346eaa4a9617b02bb8abe1d3d6ffe94bf7d212a3db038686948dc0612e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:528eaaaa1c87359c98e7c7f6623561801a8acd9beedc6d933f7ceb675b8feb15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269218712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73aba4da5ffc33f5a4ffb1452fdc04e13882d628958a038ea35a699257dbae8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:49:06 GMT
COPY dir:36f5164517b1d083643fb66b5ce80f151a1fd45f701835f30c768c906e72895e in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:49:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:51:26 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 04:51:26 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:51:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 04:51:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 04:51:43 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 04:51:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 04:51:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b56a069e7c2cce602b3c97a35f6b51d9429de11e3d7b2b47ebdaf03792986fc`  
		Last Modified: Fri, 26 Apr 2024 05:02:27 GMT  
		Size: 145.1 MB (145095338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5254734c22e9d9f64ba1a482c8a69b96a3a75c266de460f43a577de19114187`  
		Last Modified: Fri, 26 Apr 2024 05:04:04 GMT  
		Size: 69.0 MB (69023487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b81b2a7b215610ff95c26de66aa596c810c49dafb8c9e6b444400633a5f038`  
		Last Modified: Fri, 26 Apr 2024 05:03:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf03f90d1917ec28efb2f8cfaf528e4ea3954962bd82a9a39ad7135b53856b4f`  
		Last Modified: Fri, 26 Apr 2024 05:03:57 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5eb50de94fab2adf252a11e7feb88656f6c26963b279a92fcba301be9b202e2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266774112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8050cf8df0b3b614f4d13b0f42b493db10d1eb9eb65dae583a10a2f41420e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:31:04 GMT
COPY dir:c133644f5c07e30ba622e3ac6570b28080cd19be78bf4af55cfe492de2f59b24 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:31:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:33:09 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Fri, 26 Apr 2024 01:33:09 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:33:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Fri, 26 Apr 2024 01:33:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 26 Apr 2024 01:33:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 26 Apr 2024 01:33:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Apr 2024 01:33:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdec292b58e2b3144d6224079475782e80323512307f657853dcbef336a1ce35`  
		Last Modified: Fri, 26 Apr 2024 01:42:30 GMT  
		Size: 143.9 MB (143891890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f8714d098724d47306b9cdb4224032c1c459d2156086f9bb937d30c16489f7`  
		Last Modified: Fri, 26 Apr 2024 01:44:08 GMT  
		Size: 69.1 MB (69141242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bbd4223ed0fe77d8729b4c560c9bdc06fca5ee1e2fc02e978a3e21c767d96`  
		Last Modified: Fri, 26 Apr 2024 01:44:02 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792e9b64eec218022e72ead40c7e9f4c932e9b2b0e0921e1abe0268c63c0f348`  
		Last Modified: Fri, 26 Apr 2024 01:44:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
