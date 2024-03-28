## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:785413a5ef403aa06944b98245859bc1ac171785997b767512ad3e0174c56046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d96f9ed6473f25eb7189a94352940290f43ba73eef0e868c02b970118c547eb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275315283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd233ca16327032205778925e4712c9ef50d96abfa24d9bbae547ed816bd541`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:58:02 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:58:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:03:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:03:55 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:04:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 03:04:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:04:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a875645a27e3ccc8bfba72105d6bf6ac46ec1c8cbe99056efaa0a86db4bfd0f4`  
		Last Modified: Thu, 28 Mar 2024 03:19:12 GMT  
		Size: 145.3 MB (145271224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10561b80483a4d27e01ac0dca81adf6368788194aa9be13039efa33958cd9503`  
		Last Modified: Thu, 28 Mar 2024 03:22:24 GMT  
		Size: 80.5 MB (80491246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c644afa400c7995bf1438c9b963ebf8033335fec6225c40651015a7c92f81c2`  
		Last Modified: Thu, 28 Mar 2024 03:22:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ebdcb1a0477fbf98b60132bdd7cd7d13e26180c6c77c86e9a4e3319f9ccf57e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271853070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa8542cf952547a334c84e11d1eee42deba976c1fb44c74d48a53f61291007c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:32:13 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:32:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:37:05 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:37:05 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:37:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:37:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:37:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095e0c8804330303f34a1bc5a23f03e613b1984ea526d87d9d7910e9b5449ef4`  
		Last Modified: Thu, 28 Mar 2024 02:49:26 GMT  
		Size: 142.0 MB (142006296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8ec46cea8d39bfba59a489113155d7b79d118619d8cbf1cf1450df00a209cf`  
		Last Modified: Thu, 28 Mar 2024 02:52:00 GMT  
		Size: 80.3 MB (80255171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11627064dac803abe7748f1a0e0b7cade96fdef8db3762e5d4e6711c13b31fd5`  
		Last Modified: Thu, 28 Mar 2024 02:51:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
