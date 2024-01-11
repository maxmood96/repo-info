## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c54317e2454d21ca4021796939e1069b07ccc6e55a7d5e706e9344877aa1c4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a8690c7642f4a22fb7b6d211d541f41176aab3f3c302aa76480c55ca787d52aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275320041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78182e3ac0217898fc8555854d3ff99ad9c7309e704e5e2d092fadddd37cc53f`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:58:04 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:02:02 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 05:02:03 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:02:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 05:02:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 05:02:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4828ea3928dab776906e18f4cf1d64b338cf2fb9966f9414f22c0c6cda899dae`  
		Last Modified: Thu, 11 Jan 2024 05:17:34 GMT  
		Size: 145.3 MB (145266366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ac39cd9c8bfe9000f30627a1a4579c998b48ff3b02b4bb76a22d50f9c28a4e`  
		Last Modified: Thu, 11 Jan 2024 05:19:44 GMT  
		Size: 80.5 MB (80491569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62ebba8f6d7dbefc8e41849418f62a15bafa0802278370b4cc038bde1b0640e`  
		Last Modified: Thu, 11 Jan 2024 05:19:34 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03866fa82cec686556b3ea31ea89f718e9a6b769b5630d7505186ada70cbcc12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271850723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4498962df0f7528d56d31a7befb182f1b37ae0be3aa7f8196c79972a02dee3af`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:58:59 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:45:05 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:45:05 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:45:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:45:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:45:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593f42435501ab6968f6cf2d6070608060a249b959ac3906a8d5dee7d8736304`  
		Last Modified: Tue, 19 Dec 2023 07:15:45 GMT  
		Size: 142.0 MB (142001822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f25594bf49a046edaf0d4b6c6231a15daff5ffdd7351cecc5ae938481e56325`  
		Last Modified: Thu, 04 Jan 2024 20:55:22 GMT  
		Size: 80.3 MB (80256027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b344c092b054a81ca4a12d76c7e740b40b7b603986e0321a66741638de13a9c6`  
		Last Modified: Thu, 04 Jan 2024 20:55:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
