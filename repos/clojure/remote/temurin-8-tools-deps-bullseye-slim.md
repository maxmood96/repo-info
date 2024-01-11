## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:04b1779ad40f0d315228a293f7bfde0c0cb5c559da0b7ee62c62afe38f0782c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:96ab812c45ef4d81d213ee316c09d53745398f2833a3481f3495e0246cf5d05f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193646368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3f09993a6ccbfa54dda336e8310e624f75b3d7391e267baf6394cbb2086f92`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:54:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:57:37 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 04:57:37 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:57:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 04:57:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 04:57:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174aa11106f2d3d4da01484fac2da5df4e3ce9ec4196afe1ba0d6908551deaf2`  
		Last Modified: Thu, 11 Jan 2024 05:15:12 GMT  
		Size: 103.6 MB (103598261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bd4dd23675b574f214d4e95fc87778cb128b3310af00f6a7666d8f5ae3c228`  
		Last Modified: Thu, 11 Jan 2024 05:17:09 GMT  
		Size: 58.6 MB (58629537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0b6ccbe06b7366fc9375a25d14bd68b6626911b6a6c36a51751b00c818980b`  
		Last Modified: Thu, 11 Jan 2024 05:17:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9e31ad8ae943e64bc65933faec4602e268ab8bec46ebbace246952d811f90c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191522802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289154fb1dc10161295ea2ec1174beffa2d928003c6b19b0c9df1b3588bdade5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:55:48 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:42:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:42:35 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:42:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:42:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:42:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8460c2429b384c138ca104a8d205038e1877169d7a2d55c0430c97fdacb19c12`  
		Last Modified: Tue, 19 Dec 2023 07:13:30 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e784be0f2ac2655203f71d80c4e297445f5275f7c23c9ea662c66672986eb0`  
		Last Modified: Thu, 04 Jan 2024 20:54:12 GMT  
		Size: 58.8 MB (58756596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf70ba7f713a203e0ceb91a01345529e8d5b0e5d91c89997b1dff68a6756df3`  
		Last Modified: Thu, 04 Jan 2024 20:54:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
