## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:43f3827441b18e1af1aef4802086adcde56d2d23d79c3e80895c948b57f71417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ac03ce13636ef3729941d1a68cb1839f72ecbdf0fdf4cfd2efc26905bfc49665
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235319226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c299be2d90f062fb5709fcdd8467670ef4dcae9216dd2fc3725326daa27596`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:59:44 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:05:08 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:05:08 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:05:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 03:05:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:05:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765e80b34419cc4d75a074af22d808e72a16040aef302be6b97f83f87c3cea68`  
		Last Modified: Thu, 28 Mar 2024 03:20:12 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d8f5be43c92db68b85f4ebf7e6030cb0888224a78cfea6f775a5b7594320f5`  
		Last Modified: Thu, 28 Mar 2024 03:23:18 GMT  
		Size: 58.6 MB (58624896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afa8b4787470477f00f59c2c738c5e0ba1d56afa93f8e4b5c1746fa2977360`  
		Last Modified: Thu, 28 Mar 2024 03:23:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b504cbd94c3e492a56c1975fc0783100978bdaf1a3f18517f3a16da56e5fcba7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230829044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef94a3140cf4b0c7ee6e9f2f54a97c35e2eaa91887e1b1ceeadd7dc4eafd364`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:33:52 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:33:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:38:08 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:38:08 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:38:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:38:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:38:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff8a31a2022acad9a6b7593ce2e2b45a1ce4aeb662d6311f16bc5d6ea9a4339`  
		Last Modified: Thu, 28 Mar 2024 02:50:17 GMT  
		Size: 142.0 MB (142006322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9659fe0824bcecbec8a8a6089d92370728c71e7777b862f70421c713c08d36a`  
		Last Modified: Thu, 28 Mar 2024 02:52:48 GMT  
		Size: 58.8 MB (58750987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1983f5a5debf477d6f827cd87971bc9a766541e11995379beac98a6ec50a8baa`  
		Last Modified: Thu, 28 Mar 2024 02:52:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
