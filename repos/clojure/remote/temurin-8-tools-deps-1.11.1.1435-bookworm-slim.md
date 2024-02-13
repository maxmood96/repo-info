## `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm-slim`

```console
$ docker pull clojure@sha256:7d1abaea65648e68dec03b8031e45936b909c1dd1c8d91e7cd5f9022b85677f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bb51f1d68866dfd49e173cb2c25935183f8538bb5ee0bab13da31203647e5744
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201778957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafa0e1321632b9134ea9f59b96657306511d6e9406b14bd1dc4ef4990bf5f58`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:47:31 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:47:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:51:26 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 01:51:26 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:51:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 01:51:45 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 01:51:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e1a9cbed5cc87e9380774cdf6c1211d2a3f6e261065440396d798b85e10c29`  
		Last Modified: Tue, 13 Feb 2024 02:09:40 GMT  
		Size: 103.6 MB (103591878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34b6f618dbd267d53d94b19c9dfbd09698081cae516d3a5821ebe7e1cd2f4e9`  
		Last Modified: Tue, 13 Feb 2024 02:11:49 GMT  
		Size: 69.1 MB (69062372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6689c6e8a478ced45716aaf67b4a02cd98c74bd117bb0e4ea1194ff7d7f1158a`  
		Last Modified: Tue, 13 Feb 2024 02:11:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e6787c55efc85875725f91c166fa7ddc6cef67e26f0e7a83b229f31434e8a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200677409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276ea267d3f0c50167736025166b64e6c3d644a3aefbd92f4ba13ae8c9f5b948`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:55:02 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:55:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:58:26 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 01:58:26 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:58:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 01:58:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 01:58:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8cf35b6ab4ec7d12cf1c238b357320865b8bbeafb18d87da48bf11d86da22`  
		Last Modified: Tue, 13 Feb 2024 02:14:05 GMT  
		Size: 102.7 MB (102703044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8ef4441eb16a31c3a998ef4508bb6631a034df77d84aed42409113eb392317`  
		Last Modified: Tue, 13 Feb 2024 02:16:02 GMT  
		Size: 68.8 MB (68817386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae80f5db6fe2a53e1ba5b263ab47809a790c049d41b51c237e84947e8a480a`  
		Last Modified: Tue, 13 Feb 2024 02:15:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
