## `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye-slim`

```console
$ docker pull clojure@sha256:d4ecbad73f5d2bd2fc56e8bdb8020916e69fae14775d972f6a9d2b388cea6fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d2e05570263b81bb868f12a7f70fe54b0e2fccf5ea6a82904042dc70912e14b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235324598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87beb758754f3dc510a49e75c21e0eb1b20df3fcf0a5466e1b15668cf452bdc1`
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
# Wed, 10 Apr 2024 06:28:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 06:28:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 06:28:12 GMT
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
	-	`sha256:2e726227cde3620456c8e19f385a061e25b06fa255931a96178039136c46f255`  
		Last Modified: Wed, 10 Apr 2024 06:45:16 GMT  
		Size: 58.6 MB (58625001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5477966d0e1cc26d075d53800f42264fa4682ded96daed488e8d63e7204cd4`  
		Last Modified: Wed, 10 Apr 2024 06:45:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1435-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2783c63e669f724519a5ba3fb8f359ff40649fe9d1f01df30f6c39b0db193690
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230834175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cb1ba43aa210a178f3b91e17c9c3e4705098cf1772dba54d536dcaec7ba903`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:44:53 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:47:48 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:47:48 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:48:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 04:48:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 04:48:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9f0cb0cf9f2a91955c0e3d73d286f38239bde001a4ae6b8442625ab39f1197`  
		Last Modified: Wed, 10 Apr 2024 05:02:10 GMT  
		Size: 142.0 MB (142006303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fbd5cf0070a2c3c8bd244f7f3d3c907d52c68a86e875fdcaf81f5783ec3d56`  
		Last Modified: Wed, 10 Apr 2024 05:04:02 GMT  
		Size: 58.8 MB (58750946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e439e03e0549734e294921b93b97185d1b59c46e635090766c0702a5c8af0a3a`  
		Last Modified: Wed, 10 Apr 2024 05:03:55 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
