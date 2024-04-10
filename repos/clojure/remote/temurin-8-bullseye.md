## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:e56a7332ad8123e22bf1f23dd23fea318c786d36aa664d29cb3ad52a7238660f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:378b20d01aab5ab8c9cabe6ac1bbc9e43a24fbc58217695a68b92933a7843bb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227699140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bc14039fd37d70752364f5128e6b68caef3e3fd91c9283cae76527ff942b60`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:18:02 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:18:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:21:48 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:21:48 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:22:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 06:22:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 06:22:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c58dda9fddadf47ec61579a42c98d54a9dbbe36bc23256a7472bdbc9d7d1a`  
		Last Modified: Wed, 10 Apr 2024 06:39:37 GMT  
		Size: 103.6 MB (103591916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139209e61c72098d791199ba03c1a004eb0f709f38042ed6aa39c882b67daa50`  
		Last Modified: Wed, 10 Apr 2024 06:41:37 GMT  
		Size: 69.0 MB (69016341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2001544e1d736a72da6b2536234b01145f8202e46550e63282da8b4bc5a048`  
		Last Modified: Wed, 10 Apr 2024 06:41:29 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51aa12d8530e7a58243f40fb1ec85975ad0b52f20e5d5437b4e020710047fd56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225574302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3c4a49b5c8a7b0886ff84bad865671d9463cfcdade61f17457530afd2fd0ea`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:39:24 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:39:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:42:31 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:42:31 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:42:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 04:42:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 04:42:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4356e798bd14d733012e92b998ac0cebce255bbc6b9b566fbd468609bb72b42`  
		Last Modified: Wed, 10 Apr 2024 04:58:22 GMT  
		Size: 102.7 MB (102703041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8f8f7825c692d2a1bc71baf387b0e67156357d23b768d1762d4f428715fb3f`  
		Last Modified: Wed, 10 Apr 2024 05:00:38 GMT  
		Size: 69.1 MB (69141468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd68046426f79485771dcac250bbe716fb1a3348458c4fbb8a7ca01f2e911ec`  
		Last Modified: Wed, 10 Apr 2024 05:00:31 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
