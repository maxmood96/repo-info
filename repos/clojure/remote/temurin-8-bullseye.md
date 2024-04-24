## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:dad18c7b2288256c28acf12e0481fb42655743e970c50c25eaae388eb09837e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:54884dc6de7f9c11c1b2cf78c06e8c0f974f33cf96d4413649c8f8e0149d28aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227717418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6a0457d3ed2f4117ad9e768c905b0868a1e0fd1fb49bab55348583cd07a67`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:14:32 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:14:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:17:11 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:17:11 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:17:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:17:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:17:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdc70d459841181e437388349fae966ee84cacccee8e9217b95eda3cf7bec02`  
		Last Modified: Wed, 24 Apr 2024 21:40:37 GMT  
		Size: 103.6 MB (103600134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db14344489c87692e5376edbe5dca1be3d6307d437874bc36fd413c61301d4`  
		Last Modified: Wed, 24 Apr 2024 21:42:22 GMT  
		Size: 69.0 MB (69017794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03064c4b422b9aedcf6a0827230580f4b9498f95a73ce745f0e0bc83f4753e5`  
		Last Modified: Wed, 24 Apr 2024 21:42:14 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3bea981d7d8b8ef4606c822e66b72ee07d89d74c0c32d46656ecf001f9c0b1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225582891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0c008655c423a3296f33c1a1413660e9913f3cd18b7158fb39a38bec76cae5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:00:28 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:00:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:02:33 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:02:34 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:02:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:02:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:02:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b10ac2f49582813d917176fbb09495d94affa86eed578334d80898e8e861343`  
		Last Modified: Wed, 24 Apr 2024 19:21:54 GMT  
		Size: 102.7 MB (102700147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402bbb4c46fa8c90fcef9c8b2cbfa57921e9bb80546264cb3b558a0cf2973509`  
		Last Modified: Wed, 24 Apr 2024 19:23:27 GMT  
		Size: 69.1 MB (69142168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbec3c1c9d1ffee5acccf770c30da7ef3e949f0a942b87d76d840e0d084d3c6`  
		Last Modified: Wed, 24 Apr 2024 19:23:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
