## `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:13b690afbd5dc4d9b3ef6d10641438e717b43fb3178b572b4eaffcda746f64a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fa8b3da5e679c9794a637b5b1f00bd864118fc4fef33494b3da6832ac6a9814f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254910340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e45fb57b286759448223dc5604c9d1bf5157203d1e0b600017223e809bfaa9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac77978a3f90eee67add1fd5dbc9c2cf3f745ea5a79f17a0e78cb4761092d5d`  
		Last Modified: Tue, 23 Jul 2024 07:14:07 GMT  
		Size: 156.7 MB (156715516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de56d60e4f127ac005f5273a439ec8c5e930c5022ccc517dec7701f2de94d10`  
		Last Modified: Tue, 23 Jul 2024 07:14:06 GMT  
		Size: 69.1 MB (69067495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46081f306efb341e264674f76165b523382763cce5becebb4cab9a3cbca21d77`  
		Last Modified: Tue, 23 Jul 2024 07:14:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb7451b89127df33df09aea3abe76bb633e036e6242748cd55e2a4b53292f9`  
		Last Modified: Tue, 23 Jul 2024 07:14:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aceb04154e72eb8bc25861c25fcf488ad520fab9ba4fd925cb5b6e8c93b9c25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306d25ce082e32f1f86caa49074ebe934f02efbc154270dd3b9354844c3892e2`

```dockerfile
```

-	Layers:
	-	`sha256:1007e795852f351480cec33509febc460f021c2a2e31d680e1d21b4593b6b167`  
		Last Modified: Tue, 23 Jul 2024 07:14:05 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bfc3454c75d8d8dd8d2e63a3d9f2485fe93b166af61adaa407e13666b241dd5`  
		Last Modified: Tue, 23 Jul 2024 07:14:05 GMT  
		Size: 15.5 KB (15511 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f476ff04c11b748ea29fc41a330920ee7aef8a6fa941e73fbc1a943e143ad85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252714101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e025c416fdd4ad3f63ddbb1154d4d755a237791e5ee69b5566e5ae716ca425`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db123f60414e6579afa1a9d6b132dd9867e08b53008118b0883aaf2db50b2e7`  
		Last Modified: Tue, 02 Jul 2024 09:44:24 GMT  
		Size: 154.7 MB (154737984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8296f44bfdef8deed69defaf61f3ca7cbb710f1f3229bfd5727b838a2674d57`  
		Last Modified: Tue, 02 Jul 2024 09:48:32 GMT  
		Size: 68.8 MB (68818514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9395b81f794779455018ae9811fb36d007690b145e14d49ba543755c120ea388`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911c622b042c8bf9ea71fcd0b9391a1aec469f24b2ba32c69d50feec842dff3`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9570e779d186c7de6e5ae1831099ea4f539339f999cc14ca2e5aede7b4ad662e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c1d770a07bb4c0ab9f04d511da9736790a44806a34a3ea3e661a9161c9e269`

```dockerfile
```

-	Layers:
	-	`sha256:066a063d42be04f90bb221bc22776c35932957dceb1c18631748341fb636fef7`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 4.7 MB (4711418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7f923e1e8ba8f822ccd65fc2940f48ccb1e2708afe39da6ced2ba9c933818e`  
		Last Modified: Tue, 02 Jul 2024 09:48:30 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
