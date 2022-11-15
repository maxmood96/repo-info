## `clojure:temurin-19-bullseye-slim`

```console
$ docker pull clojure@sha256:8916b3bb2da195b093d4874c2a201071efd99ca5c76cc7e2a18f0a1c4abbdf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8e7c2d353be6b4abf24090412858c2e8736e940a07e6763fb61eba20d10bc090
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (293990464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58fd08074d4dc03bfac6325b7fe73c6f43dc6bef422d5d9a93de97d09dcd538`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 18:00:50 GMT
COPY dir:fef581854733ec7202f8c807463b9e1952aeb6c7a002719c7e54987e50ea4dcb in /opt/java/openjdk 
# Tue, 15 Nov 2022 18:00:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:02:43 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 18:02:43 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 18:03:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 18:03:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 18:03:01 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 18:03:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 18:03:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e4d14fce57d69fb74ccc6b172b6b0d98f6dec24907274ddcdd4c3eefe4947b`  
		Last Modified: Tue, 15 Nov 2022 18:12:51 GMT  
		Size: 201.1 MB (201103395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c7a67de8fa02afdd58845910a3aded0e95fec1f714368ea6054e48e6e7124c`  
		Last Modified: Tue, 15 Nov 2022 18:14:01 GMT  
		Size: 61.5 MB (61473424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d0b24d46508034ff5edf72ccb5e44a43f9c1a0996d03647810c2283e8130a2`  
		Last Modified: Tue, 15 Nov 2022 18:13:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34b78b7cfafbe5344405db071455e65d2968945d0ef38f44d84d3cd7aefb138`  
		Last Modified: Tue, 15 Nov 2022 18:13:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:adbb53aa99e5546411c2131f60c14bbbe6f6fe7f2e35d7def75aa3f9b6efb8e8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291519487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9594ca9cd02b92cb91308cef408612c42020218c2b9eb5910222aee5cadb2109`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:57:11 GMT
COPY dir:4138443eebfda1a2a245638d5bb568645bd34d79b66d39a3be31b5ac6b823d6d in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:57:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:58:48 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:58:48 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:59:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:59:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:59:02 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:59:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:59:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e822da9eb481d8723150163c7ea4b157d85c48d2dde40328d24aac329303d4f`  
		Last Modified: Tue, 15 Nov 2022 06:06:59 GMT  
		Size: 199.9 MB (199864406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afee09c7d6d8fd5b877d2bb972b1b67b549142d610bd26efdcafd335e712c37e`  
		Last Modified: Tue, 15 Nov 2022 06:07:52 GMT  
		Size: 61.6 MB (61593460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f10b3f2a102f51495d75188591b522ec95411513d25085ec940329a578b39a`  
		Last Modified: Tue, 15 Nov 2022 06:07:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a569f6ee0bdb5fb943b4270a639fe5e4c609760c2777ba1e0e25ca1dbf4dc6d4`  
		Last Modified: Tue, 15 Nov 2022 06:07:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
