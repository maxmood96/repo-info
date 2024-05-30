## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:6dd67c9e1217c6eaeec91cb64d3edfcc75ecec7ccc2edc3a9828821812262dde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:01112be7d78635baf4bc13168359f659dfd9048d8fcb4046da9b1b417cea2db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83020712fa014fc9c10c61e22d9eb09eb543d662f53d81ededefbb71fe294ffd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24651d987a2e75e63964720e07e73969c555c53a3bb0772657a5f25cd5e5a1`  
		Last Modified: Wed, 29 May 2024 19:58:24 GMT  
		Size: 158.5 MB (158497991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bc0efe356c541549aee17ca2f588523340e5508e6c9e2484baa95d378505e3`  
		Last Modified: Wed, 29 May 2024 19:58:23 GMT  
		Size: 68.8 MB (68816493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c728f1cbff89c4a6eef955acc869275f2e1a966534e88d387b04407635bdfe`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea24a54e3489f5b4be5b5b345772794b801d304ca4407e140c92f4584e044fc`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:81999d0a9acde30897659a9e20f51257427be9d8c6d9b49a1fe4ba26cb7ffc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b66546704020225bb6ca5bda369e04b4209a50103b8bd6cfe6b92fb3064be3`

```dockerfile
```

-	Layers:
	-	`sha256:9e755d0beb902aa0269e03b7f4b74e1310a9864e8f50fb6961d8e701441c9f03`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 7.0 MB (7000438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cab113e1477da700c7b2d1baf4b97e7e5b9b71913504b1d5cbcf1eb63203a5d`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 16.1 KB (16066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:799239a8c1495367cf429244e8292d2669ba2630df2d82c637102a9dcebd791b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279335146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3fc0cc599ab93a03285e522cd31be5b9d44b596af33d93303a84f8e9b20925`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
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
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b2f7f90d51230d964aeaf606c67fed43aa8b9fc53ecb302d801a7ca98ba638`  
		Last Modified: Wed, 29 May 2024 21:49:45 GMT  
		Size: 156.7 MB (156665610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbb7ee5dff2217f51f9a9395281f2b32f94d1d4dbfbdda8f22daa87f53fbf8b`  
		Last Modified: Wed, 29 May 2024 23:48:41 GMT  
		Size: 68.9 MB (68929500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058edd1462d82d1e2c66dcb10c918479b9ed015eaf161cfd3783a5d7c309154f`  
		Last Modified: Wed, 29 May 2024 23:48:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2152a5d5041fe92d65de379c658b2836a9049b1122cfe546f9aea53e08b0919`  
		Last Modified: Wed, 29 May 2024 23:48:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f97783f41b7710a342d9f506a4795fe7f7037a139e4f33b8a064f54b76271c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dd1f898a821b3b9aefb7cf767c4a8625ae750ad2e2fdcf3b5a9f3cf1a24310`

```dockerfile
```

-	Layers:
	-	`sha256:6315468981b9c0f40e8e7eeb1ed1f03a42b1a8e9e6e240078ebdca04d89d4817`  
		Last Modified: Wed, 29 May 2024 23:48:39 GMT  
		Size: 7.0 MB (7006184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb30806c3a279e93057f4c5e4249408f699b3956dece9c858ca76a8fc735496`  
		Last Modified: Wed, 29 May 2024 23:48:38 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json
