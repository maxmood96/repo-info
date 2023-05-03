## `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye-slim`

```console
$ docker pull clojure@sha256:fbac8409456ec92ea5b044f1e23b41a06e115081470d6443f5141e984a2d5550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:29f1b33ff2c19a5e78ab99b246c8bd829c549d00965195f69c18fa4186c308eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291463870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7b787fac4ce20e2790f47e6676900908d80d3aa16ff87f95491eb2a8060227`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:04:09 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:04:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:07:39 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 26 Apr 2023 20:07:39 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:07:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Apr 2023 20:07:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Apr 2023 20:07:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4732512befd268374b48fb0d71e1d7b92ee077512c8190c2a7378323351f7fb`  
		Last Modified: Wed, 26 Apr 2023 20:21:00 GMT  
		Size: 198.5 MB (198549520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e0078bec6ff9027d83389c18165997e14e4c6d3d40c5193643bc5efd40f495`  
		Last Modified: Wed, 26 Apr 2023 20:23:01 GMT  
		Size: 61.5 MB (61495507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628025206a1364fea0a8d5eda13451aae7440c07488b171457147d8bc810b60`  
		Last Modified: Wed, 26 Apr 2023 20:22:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b2c4fb9f42107503ba212b61208763330a78005ce139c14884c859fe4d3debb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286988160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d73532d3e561f90ae3831aaf8b80f3ea189aff606cb32674dbee6c4472177d5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:46:48 GMT
COPY dir:8d5d0106b2c3fe64c4905be44080473b7828ffb48e0e107739a7ba7a3cb627cf in /opt/java/openjdk 
# Wed, 03 May 2023 17:46:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:48:13 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:48:13 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:48:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:48:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:48:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02fdca64c090abce4b51b43574d16ea2ef8901894d1cc771bbedb52a44a6ba3`  
		Last Modified: Wed, 03 May 2023 17:55:07 GMT  
		Size: 195.3 MB (195324206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9016544a86cb4141c5304b49c826dd0e447910d04cfe65a68174a60d409972`  
		Last Modified: Wed, 03 May 2023 17:55:59 GMT  
		Size: 61.6 MB (61610606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4250773f35f9d27f4b90400514535c557771441c4ab2a7e684a11d5ef70e7cb0`  
		Last Modified: Wed, 03 May 2023 17:55:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
