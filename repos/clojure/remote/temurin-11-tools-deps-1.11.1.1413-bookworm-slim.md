## `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm-slim`

```console
$ docker pull clojure@sha256:dbd8ca00bca0616b69f302b8bed6f425d701f12e6fd203242ba0e44bb31597a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c217fd6529fbe2cfd7a796b532e53852f7984ff8ac048597ed885afa4676f0c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246350009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4738d07bcaa5712b24e386c749ef53448e73d52f199bfe05aa921c8699b43d94`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 09:54:40 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:54:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 09:59:57 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 09:59:57 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 10:00:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 10:00:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 10:00:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4050ac330d97fd84a1d6329cccff3c6d67aeace4dadb496e6d7467c8568e3c1`  
		Last Modified: Sat, 02 Dec 2023 10:14:01 GMT  
		Size: 145.3 MB (145266397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19200c1e01181e6f10d13b8d82101a2bfc5b5568093c3e525c2b069e3dfff11f`  
		Last Modified: Sat, 02 Dec 2023 10:16:43 GMT  
		Size: 71.9 MB (71933087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7a2b646dd305d6ffd2d686a9a97e4a0b3f6e0278e3e05206a1a38aa2ed1290`  
		Last Modified: Sat, 02 Dec 2023 10:16:35 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5234a3dee4d965a0bae9e8a5442e6ba9a1f37b9b1a1279cf40e274e5b5f873c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242877042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5cd2631a7c4ce6a27263d02abacd740d8e740be20c8553f4412dd474b8ebcc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:45:02 GMT
COPY dir:201fdbb3aef6b177b9038d3dd5bbe865568281c78c7bc0c153b57943d571a0b6 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:45:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:51:22 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 08:51:22 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:51:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 08:51:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 08:51:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499cde67ef4ddbbb49efba4d14e85c99ac1dcc40592a7b8c7cac48b4f81d299b`  
		Last Modified: Sat, 02 Dec 2023 09:03:55 GMT  
		Size: 142.0 MB (142001789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d183d7c3148396ded8ba0053be7d3afe8cf2d293f421999848be7f7abbfcb0`  
		Last Modified: Sat, 02 Dec 2023 09:06:27 GMT  
		Size: 71.7 MB (71695358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6082f6ec0f921b0d6c4c5650fdfbb99e919baab714f7927049dca5db987bfc3`  
		Last Modified: Sat, 02 Dec 2023 09:06:21 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
