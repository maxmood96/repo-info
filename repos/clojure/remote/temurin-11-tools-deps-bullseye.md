## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:601dab8fc08cbf60cfd68db25d18c84c8584f4ef22aec88012cc6db529e18326
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2870f9955c93d32e3e0a420d93ca3cdcfd930964fef44fc6a62555d07c31c48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269607742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b07c989b41ab4ffb6a43a1e5dc7ebd05147b11b5c59ffbf9b1d0097412a76e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ecae3d381f485a2dbc99507d57957c4754b403d34787de14821ddfdc278b73`  
		Last Modified: Tue, 02 Jul 2024 07:06:57 GMT  
		Size: 145.5 MB (145504892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfd7185ac34c92a4f55b7fb97bea8b8f33272c0b5784d7feefcbbfbd46d4b2c`  
		Last Modified: Tue, 02 Jul 2024 07:06:56 GMT  
		Size: 69.0 MB (69020844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b335ca5f7d5865ed7488ab0241ba7a3e2d6ae4b65e30c7f53cc70225aae36dda`  
		Last Modified: Tue, 02 Jul 2024 07:06:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:693894fb85d96d802be77cc3073dbf4ab3e216e0d10c0a3f5c61e5447943b03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df42a8820c8ac3e5e11d1276f2f79b1a1e2392ee42046d2490ec8f4146b12a39`

```dockerfile
```

-	Layers:
	-	`sha256:71ed5c950607ccb470c6c91fec26c5c12be74569fb0a0c5cc7efff69f27195b3`  
		Last Modified: Tue, 02 Jul 2024 07:06:56 GMT  
		Size: 7.0 MB (6999790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46d83b6f7eb8b660f7e3572f62d941006b81fab067128137fb96e9740d04cf93`  
		Last Modified: Tue, 02 Jul 2024 07:06:55 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fefc01b1c8259f176be71a93db6d9eed4f882cf413f1582705b0080b29247d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265160293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c9c09ad5923d9b0a1a719f4a5f69ab1686ab4df2217347d702cbe084e75d71`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee87c36e87bb3bdbfe082f567adba704b3a12faa5430ffe9012e55d9f8698f90`  
		Last Modified: Tue, 02 Jul 2024 09:20:56 GMT  
		Size: 142.3 MB (142304047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f743b735815ca7e3de5a15fbabaaecacc8e2969f3af01b29476b634d9771a7`  
		Last Modified: Tue, 02 Jul 2024 09:25:42 GMT  
		Size: 69.1 MB (69133947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05e9bee2a519da0d5f2d4768491b2101a53ba5b804a1c8fa388f4fa2a0b88eb`  
		Last Modified: Tue, 02 Jul 2024 09:25:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5a0e5c5d93fcdef5342a1a5bc5e2b2987db5040f7f89bd10a9292781402c226b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90ea7396d21ac2ea2d6b2b82b6842c7cffa2e147e233480aaa4cf610c705591`

```dockerfile
```

-	Layers:
	-	`sha256:007984f80de6f1173b7e3cf35d399a1e6c0c6c01b26cf5a418c7612e9596c672`  
		Last Modified: Tue, 02 Jul 2024 09:25:41 GMT  
		Size: 7.0 MB (7005512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3197f1397e7b58206d417bf1858ea5de5902cf188cbb1ae4709a9ab56cdf773`  
		Last Modified: Tue, 02 Jul 2024 09:25:40 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
