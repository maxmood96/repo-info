## `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm`

```console
$ docker pull clojure@sha256:181fbcb2eecdb3126ac2757880501f5715798771fda3e980434bf0173ac8ba96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1e43bc811569169e6a3a650763b4a77a69d3d6588576af5004b412ae94e1972d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233636269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc4a8892c335d505233f4792ef5f33c74c3b0f25539795bffde5fc4a2efd1f6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:46:51 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:46:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:51:01 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 01:51:02 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:51:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 01:51:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 01:51:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fa82103c6b10ff303cbdb75dd172bcb17a9cea1c3239cb231b5ac7cde39c33`  
		Last Modified: Tue, 13 Feb 2024 02:09:22 GMT  
		Size: 103.6 MB (103591911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587ae70209aa1a415e24dba3b86f57c0005d558b906a0d784fcb5d5ddcad0cb`  
		Last Modified: Tue, 13 Feb 2024 02:11:28 GMT  
		Size: 80.5 MB (80491137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c1e4874bd581ab86e2d2b1dc2a3bcab73750b9fc2765740f5e94ea9d22ddb`  
		Last Modified: Tue, 13 Feb 2024 02:11:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d385d8736d6396c26e8adad221b15c9256cd00dcc0dc00eb10bf10dde970f5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232550273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492b378fa64bb890ab5b15a3ca489d678292f3f30ebd885152ae6e1aadf11db5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:54:30 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:54:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:58:07 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 01:58:07 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:58:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 01:58:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 01:58:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2d4e3ded6ddd5ff92452771ec0295a8a94998dcf58890b6cbe30fea243fb95`  
		Last Modified: Tue, 13 Feb 2024 02:13:49 GMT  
		Size: 102.7 MB (102703043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6676eb7ef7446943467e6c70c3f5e9e810033469d9a8118cb056fd4a33dc8fe1`  
		Last Modified: Tue, 13 Feb 2024 02:15:41 GMT  
		Size: 80.3 MB (80255651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc69e1a5ba388102a133480d4c94ed145dbcb050faeb943267eea91b4e014bb6`  
		Last Modified: Tue, 13 Feb 2024 02:15:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
