## `sapmachine:25-ubuntu`

```console
$ docker pull sapmachine@sha256:43cd96d44c08408a04d953c86083fa58743be393aa57bad2882781a1b42e2c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:38f01eb978d4e65e7c42d30d118298ea5b012132f61945e9fff16124b7291afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6411313a8bf3187f1509f1bffbdad2458745b66f5cf8a5735d57a37968e8024`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe89b5c4a3bd861f4dd6d16089945ab0b061e1a1a0d9e1b858a526e0ebf40c`  
		Last Modified: Tue, 21 Apr 2026 23:03:53 GMT  
		Size: 222.2 MB (222185103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:39d5e9baf4b5733fecbd01159389fea874156e4613e43502f8f59b508c87e25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1645585bb34db8bf41868cb7853c43ba5f28675c4c85ec2ffdffe65403b64be3`

```dockerfile
```

-	Layers:
	-	`sha256:5df1b7e0a637a47703c245b0dad3e6533a03028f75fc3b69d03abb42a45d8c5b`  
		Last Modified: Tue, 21 Apr 2026 23:03:47 GMT  
		Size: 2.6 MB (2599461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06fbebddcef77b37958116bf9076f3c24409c43496da145c307e54da1e1c377`  
		Last Modified: Tue, 21 Apr 2026 23:03:47 GMT  
		Size: 14.8 KB (14842 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3e69ce75c66998663a371f49d27a94cdf83a4ad0820b946dd8ca8486d30a566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248866285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d016d191880cc5709d1ff6e25b4ea5760ce027b6b7269dcdcd5812b5375162`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:04:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:04:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b2565ef4daff9da8eb2ec43bc93c9094fb39f959a542afc23787d6a927964d`  
		Last Modified: Tue, 21 Apr 2026 23:05:00 GMT  
		Size: 220.0 MB (219990500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e8a6171d77a7579cee7cae5a2737945ab25982b85ec4468ab888e87d28f2e2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf210814fb070fef63538b07cbd6ba18ccd9681ba1977b7c7f378e46d66bc4a`

```dockerfile
```

-	Layers:
	-	`sha256:029f398da93443d1140c7bbcd623bf2d7cca0d6c58c8eff54e0de78532337220`  
		Last Modified: Tue, 21 Apr 2026 23:04:55 GMT  
		Size: 2.6 MB (2600154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3531b7218bca7e8d37811a6dbf4b05b2efc0ee157df626a239aa5a4c6cdcba`  
		Last Modified: Tue, 21 Apr 2026 23:04:54 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d6b3a775fcffd183a7df677b245c160997dd919b76c7d2a54c0c87a442dc94f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257220495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c675727238d2bf416133ca9a5d9fab4f7664dacb29297c9314d6888fb1e30c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:11:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:11:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:11:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90c8d735fa60a55b356f1c948b0394ca219df8aacbbd25292dd1492212183f2`  
		Last Modified: Tue, 21 Apr 2026 23:12:09 GMT  
		Size: 222.9 MB (222906317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ab695bea99aacb7a46d81509bd6ef158fb97f5b3b434e9ec8193911f20a9f4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e417572a6636bb359a77b90f5f6098b2c0bb511ff33c76a8c51cb98ab9b074fe`

```dockerfile
```

-	Layers:
	-	`sha256:8011146bb69ed9a0f7cc1af2ba2688ac1b6c77ab59db3789fca5dbd93c6f737e`  
		Last Modified: Tue, 21 Apr 2026 23:12:03 GMT  
		Size: 2.6 MB (2596485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1aed2cf267b00512288e964dcbc8103fcf9792ca051cfd2a8ab2a64f380091`  
		Last Modified: Tue, 21 Apr 2026 23:12:03 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json
