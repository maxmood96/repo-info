## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:1785f82ac37865f8dd29bd8f940472f89b2ba5e8b356f6fdad5f56edbc30b5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f47d50c5d2d3e38a777e4e46dc9e7cdd6aa88bf9001c3f42fbd93ec93b1b08b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235324267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded4cde11b7da7ef08782be8d862a331905495b65f1c78f263fe5a99255591de`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:24:24 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:24:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:27:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:27:55 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 20:27:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 20:27:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 20:27:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0c9a5d9034646068efcee2e089ff8f21c4e19e7eb8efdc59ac64d220c0f8fd`  
		Last Modified: Wed, 10 Apr 2024 06:43:23 GMT  
		Size: 145.3 MB (145271242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4176dd9c22619eedcc4430199b8833697dd20324857935025458dbc338717edd`  
		Last Modified: Wed, 10 Apr 2024 20:44:44 GMT  
		Size: 58.6 MB (58624671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e155518fe971e53ea496bec33ffb10d3c34a4fa18492d91d95fdc56ccd6a1422`  
		Last Modified: Wed, 10 Apr 2024 20:44:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d75033fb7302baa041d9381c4319774082decbfcccbf85b572717d64a38addd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230834189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6358316d4029509a5ab26ead9efa63c221d8677cd0494b2c1503c019941279d7`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:34:19 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:39:02 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 06:39:02 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:39:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 16 Apr 2024 06:39:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 06:39:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff05a7b30a1c1c5b0e61fdf5d3f92a4bba15507b0cd3761604069982b2384477`  
		Last Modified: Tue, 16 Apr 2024 06:53:05 GMT  
		Size: 142.0 MB (142006376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe9269803173b5493b1a95cc3bc9ce42a14d9198d6f63c4d032e696a1361c7c`  
		Last Modified: Tue, 16 Apr 2024 06:55:34 GMT  
		Size: 58.8 MB (58750890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3304d3a70d586ebd395a0cfe332eee0e06f354db657c122c7a2b698208a67be`  
		Last Modified: Tue, 16 Apr 2024 06:55:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
