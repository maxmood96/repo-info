## `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim`

```console
$ docker pull clojure@sha256:6daea7c87ca95e4c3ea92a6fc732a77ea2a8cf8f7e73d2a27a7f534d4a8adb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:34298dcad8a1f6e30ef9d006aa9e214f7b12595577012710f247fd6bcdd1c92b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234946575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81c4dc4c2ca8bff4374d927c3354e3b9df658ddfdc9697e113aeae1efa509d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:30:06 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:30:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:33:38 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:33:39 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 20:30:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 20:30:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 20:30:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 20:30:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 20:30:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b214aac1e4f25666ac6825b94aba5501d4d8f133c4457fbbf9fa5777dcf69a2`  
		Last Modified: Wed, 10 Apr 2024 06:46:40 GMT  
		Size: 144.9 MB (144893128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fcf19b3bc5e34ba1d6724b85c1622c6eb2fd0e3f4bdd73adef669f2dc6ed66`  
		Last Modified: Wed, 10 Apr 2024 20:47:01 GMT  
		Size: 58.6 MB (58624692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6745ed1c16fdd434b97c32438bdfb496e65ef040069606dc7becdcc3d5ac7a6c`  
		Last Modified: Wed, 10 Apr 2024 20:46:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc5dd2fc18837b2bb79f65aca2490d5c40688824f2ea5057fc9f54f07ed935a`  
		Last Modified: Wed, 10 Apr 2024 20:46:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:463daae99eedc62c570391bcd2cf2416c5651b036301312169601b74ef0bf165
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232548849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffa54930aff363e3c9e35b7f9df06f2c7745178e9a2807818dd9284df9ac147`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:41:34 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:41:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:45:51 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 06:45:51 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:46:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 16 Apr 2024 06:46:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 06:46:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:46:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:46:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbeb97876b5dac3782043f1df2ea53c545e7b19ee4061e684a03256552ae431`  
		Last Modified: Tue, 16 Apr 2024 06:57:27 GMT  
		Size: 143.7 MB (143720862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29da04ceca43ee31aba8c0007c05d54c2e0277c0ef9ee98095f42ce0053851f5`  
		Last Modified: Tue, 16 Apr 2024 06:59:59 GMT  
		Size: 58.8 MB (58750662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3a7d0ff615152fbc7ed51d9c59573c34c7e2e0cfebe812faa98612cb716648`  
		Last Modified: Tue, 16 Apr 2024 06:59:54 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bb0351ecc2d15bfe87422766d742e9082c10015ca69a8521d2f6e91aa29444`  
		Last Modified: Tue, 16 Apr 2024 06:59:53 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
