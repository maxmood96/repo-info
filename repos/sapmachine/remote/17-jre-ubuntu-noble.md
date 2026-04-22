## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:25751a887059502bcf72a6b1935dc070cdc9abe399ffa9030e5b4c4c0ccc77ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:0815a972cf66da338fb33f6ce4dfba3d0ea86f802e5ac8974ca264dc036d2d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84665241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c6dd8eae412cd8fc632653eaa94831d28afe2547b798262b89551218903497`
-	Default Command: `["bash"]`

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
# Tue, 21 Apr 2026 23:05:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:05:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbcda6d828b71b7af2c53a831636b0ecd67821f5e6dfb31be37392e6c41d0a4`  
		Last Modified: Tue, 21 Apr 2026 23:05:45 GMT  
		Size: 54.9 MB (54932263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bfe701fff3e9721e6fc4541badc2610e7f50ba75a07120a484bdd4bf8f8e1dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c8bdeae6a0c0e4796de3a169949bd5e2f01468840b669eade1c410da6b4c8`

```dockerfile
```

-	Layers:
	-	`sha256:94b6b0f4d42d52063d9584526f944405d5eccd24d1d1fb372117c354109e5f68`  
		Last Modified: Tue, 21 Apr 2026 23:05:43 GMT  
		Size: 2.5 MB (2520695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96c97bc18aac7fb836c8acf125ac2c7eae2b859bad5110a650815657ebb3fa2c`  
		Last Modified: Tue, 21 Apr 2026 23:05:43 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2d073f658e8830beaac6cb4f60478c06af2765a9a4ff3c2ee8b8f366ad4153ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83245530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788f1d2db4a4bccdb90eb539917ca75aaa6b4eacfb13ea9e01bec742fc3572fe`
-	Default Command: `["bash"]`

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
# Tue, 21 Apr 2026 23:06:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:06:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:06:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25af59fbdac5d25ddce3d7abfb4aa9bd1ced4d58e06d19d067fbe24b1fc3db33`  
		Last Modified: Tue, 21 Apr 2026 23:07:07 GMT  
		Size: 54.4 MB (54369745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:97fa847cbacf33e09479b09881ea45c20df82665bceab00f62ced31841d09291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec62e3255900f36d9048ca9021b4e44090d370edc9db3ee18cade55baf0d53c4`

```dockerfile
```

-	Layers:
	-	`sha256:8f5fe9957d2b41b29a6382f7616b9cf4e1e049dec6706411f60fe32a0bc7fc5f`  
		Last Modified: Tue, 21 Apr 2026 23:07:06 GMT  
		Size: 2.5 MB (2521211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6cb9761eee45e57ab26561fe1491034b376d4a11badec73c0c94c1951ba732`  
		Last Modified: Tue, 21 Apr 2026 23:07:05 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:05d0a52dea351cf4bef445c4783fe5e1d4059e29b5d01c4a95056b7b83f127da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90538964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3e90e0c823588f2db5e19848527e0a634aa2292d7cd78b7849e3e1c7d36f7a`
-	Default Command: `["bash"]`

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
# Tue, 21 Apr 2026 23:32:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:32:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:32:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c596f24809ab2b8fb97b3f93cd34b359e6c6082804ee501588b63aa1a8eb9b6a`  
		Last Modified: Tue, 21 Apr 2026 23:33:26 GMT  
		Size: 56.2 MB (56224786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:adfb8394d3ff83be04a633c3216057917aae49a1c2142a3580f1f5d28734dfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca06049c7402e41f1a1bef3e229dc6423ddd0d93751f1775d711b19d63899cf`

```dockerfile
```

-	Layers:
	-	`sha256:7b240deebdc7f171e6ae6377770a42c5d1c282f8511e964b7833fee822e08888`  
		Last Modified: Tue, 21 Apr 2026 23:33:24 GMT  
		Size: 2.5 MB (2520193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3251d0a12ceeb8fe39ad95e4256200a7457f5b54c940fc37db9b2aa9750b8f87`  
		Last Modified: Tue, 21 Apr 2026 23:33:24 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
