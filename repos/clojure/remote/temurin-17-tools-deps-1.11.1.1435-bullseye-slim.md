## `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim`

```console
$ docker pull clojure@sha256:63f2ab68eba3eea90c0e0df131a08dbe8490f019d7a13968a560e4a74f6a298b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7880909e565dd4179e803a105127325965bdd0e4479696e3a592abaf13833069
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234946846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4052c99e4ddd057409ef44c4d893854c0a9c55ff04d48a6217f3fcee29ce0ea6`
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
# Wed, 10 Apr 2024 06:33:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 06:33:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 06:33:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:33:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:33:55 GMT
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
	-	`sha256:0c315ef8966ca94b080e084d00dab61fc97139fc81c3d34b5f4cd51f2a184b07`  
		Last Modified: Wed, 10 Apr 2024 06:48:37 GMT  
		Size: 58.6 MB (58624963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794ad065c76855149c224ac664c4cb4eea7549b2b0aa08beea010709d64f9c06`  
		Last Modified: Wed, 10 Apr 2024 06:48:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354532e5e25f9d76fc34d82c4779a90c414b77e7a3f9c945d104fe9b3583bce`  
		Last Modified: Wed, 10 Apr 2024 06:48:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ac2e4ade56e582e6e08b32bb07fbb17d85dccf2bb0e2c5e9f26ed6bd81b054a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232549131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191821ba5d9479ad05b7b0e259431c3a269fe8df337a80e23e80cbd48c1d94d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:49:50 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:49:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:52:48 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:52:49 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:53:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 04:53:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 04:53:03 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:53:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:53:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b297b0c3afc17da47d0f29478d0d2915f1dbc665d37c692e3982a3ce7ab9574c`  
		Last Modified: Wed, 10 Apr 2024 05:05:18 GMT  
		Size: 143.7 MB (143720891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ea0d672ef79628a2057a1eb86df3acadd3ca65bdb2e72aefb19c7b1f16d13b`  
		Last Modified: Wed, 10 Apr 2024 05:07:10 GMT  
		Size: 58.8 MB (58750916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9d71991b13868fa5f380e01bb12287165fdfe69ccc70b2772ead6147e6fbd2`  
		Last Modified: Wed, 10 Apr 2024 05:07:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3ebf024b256620df1a2a009a0f5f451aadf2441a7f7127648eb8931f619677`  
		Last Modified: Wed, 10 Apr 2024 05:07:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
