## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:40da7af27b9ca63aaccac7ef241b36a1a96cb38d87ba3617682ee1acf3479bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:879f31a00571c5075ea479d799914d78b440746a4490eb1c2cb1c6c2ebbb9ab7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243458313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd14cbaf3cb1ee473850840dd6e65e0244aae96f64f2253f60a5ca7b161f75c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:58:35 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:58:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:04:19 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:04:19 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:04:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 03:04:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:04:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a6ac31b34979fe9ad3cbc392d1e9236c7163db662ad2db2662f3d8c2227e1`  
		Last Modified: Thu, 28 Mar 2024 03:19:31 GMT  
		Size: 145.3 MB (145271203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c659a9bdbd604636182788e4c1be8ded7f2ac7d0a3c2f972eabeb88020ada71`  
		Last Modified: Thu, 28 Mar 2024 03:22:43 GMT  
		Size: 69.1 MB (69062309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3bcd28f4a712e8a8b9c511fbebd9668f258b5e2c5b6a5c79feb580871f0913`  
		Last Modified: Thu, 28 Mar 2024 03:22:34 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1cf6cad3dbbd09dc4d29b16da122285ae5d3c5acbc08f33536b05f6328384ec7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239980414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57837a5a39564b99aafc6fec7b5d488dd93755601e86f610c3f56a6564e203b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:32:45 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:32:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:37:28 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:37:28 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:37:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:37:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:37:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819794f44d5487fb5284f90132fb8e3a770cac3a81ff8a43630aa0ffcd999db`  
		Last Modified: Thu, 28 Mar 2024 02:49:43 GMT  
		Size: 142.0 MB (142006296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ba3c628c2c21df0b3e760a65e9451dd15686db99a1264e4310e7723607eb56`  
		Last Modified: Thu, 28 Mar 2024 02:52:16 GMT  
		Size: 68.8 MB (68817069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498f5c9fbe841bbd2591399d2401786b4a57c9549eec5519f8d467031b87448d`  
		Last Modified: Thu, 28 Mar 2024 02:52:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
