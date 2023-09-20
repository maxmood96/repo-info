## `clojure:temurin-20-bullseye`

```console
$ docker pull clojure@sha256:80bed8f3869d09390e2cd0d75f774e33f4cbb31b32e6a4e8e370a2a251e1cc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:54646491ecde8ee9cdd93d75b770ec00aeb98eb6c33d3da01b80b419a68de072
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280727579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2791496d698b6ae657daa0fc19f457dec4ee83254680cdf9facee2f4d63c95e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:30:40 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:30:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:31:35 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 20 Sep 2023 07:31:36 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:31:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 20 Sep 2023 07:31:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 20 Sep 2023 07:31:53 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:31:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:31:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a007c5ad34070f89dbff4bf982cc317cb01a9169574dbff83d366a9de54c350b`  
		Last Modified: Wed, 20 Sep 2023 07:39:09 GMT  
		Size: 153.8 MB (153791726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa7f2b2064a6c0322fa55b5f205d6b161a3adaf9bc901585bc2a539ae7882e3`  
		Last Modified: Wed, 20 Sep 2023 07:39:49 GMT  
		Size: 71.9 MB (71878124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7f5ebb9b9d864ea2906ab74febae23178ea121630062a49e5eff39443b45db`  
		Last Modified: Wed, 20 Sep 2023 07:39:41 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b10b9761b7d95987976b0fb1cde744cdf8e42631405c6f73d9a650c41a03bb`  
		Last Modified: Wed, 20 Sep 2023 07:39:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a3033b0d454c0163c27ec20abef39f1a154f8f49ae1a8ceb2659490f12ed7ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277823601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e314396390766452cccd3c61fa6e1140ec43704b86de33c0eab398477eedc7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:11:44 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:11:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:12:35 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 09:12:35 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:12:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 09:12:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 09:12:50 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:12:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:12:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc354c706869eba40a152aca0c1d130fcc77393eba6caeec4c0c4b6b5a1cb1b8`  
		Last Modified: Thu, 07 Sep 2023 09:19:09 GMT  
		Size: 152.1 MB (152120013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cde097c5c8ff7f8b5f52bc956e7afc07c01ea318f2f0dd29527a66f96e0118`  
		Last Modified: Thu, 07 Sep 2023 09:19:49 GMT  
		Size: 72.0 MB (71997856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9159f768e3e56d545d903b7ce40fce885e085f8d54fac2e6b8933cea2834c324`  
		Last Modified: Thu, 07 Sep 2023 09:19:43 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dce5cc1d6b6d6529ffc59eddecb909301f614acf54c27506a6839b8addf24e`  
		Last Modified: Thu, 07 Sep 2023 09:19:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
