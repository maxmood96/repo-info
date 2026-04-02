## `sapmachine:jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e76c8922d99ad797357f94cc5d40fd519aadf90f48d4ac4a7c1afff6d3da18fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:544b73079a6e81136924cbef2dba0c2f150cc4890b0210d0b99c8de94d202218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255711102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c468980d5085c8dbec4d378ad4562660efeaf244340582522a0200038000c9dc`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3453aff15549f89fb3572b601e198e3c88b5240c5b7acea6ca5708ae2189906`  
		Last Modified: Wed, 01 Apr 2026 20:16:09 GMT  
		Size: 226.0 MB (225974689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:764a3f7dd55104b35cb69af0eaa76478efb34035b4d1dc8c6c340bf244903ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf6f77be87fcfbb078b471659b47099ea342fa09bc7b1a290ee60167bd0cd6d`

```dockerfile
```

-	Layers:
	-	`sha256:bf4435a8f958d6fe601d7aef1d376d9224afe02c4ba5303b06d664fc8f9030ea`  
		Last Modified: Wed, 01 Apr 2026 20:16:04 GMT  
		Size: 2.6 MB (2619593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1414ce92c873726d433940a67c61925a3aab9a6c4b460b3916a6bb61eb39b2`  
		Last Modified: Wed, 01 Apr 2026 20:16:04 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fc7d54269eb1ee665379ed5af33261fdf096b207798c0464095138cd1c09542b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251403795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1b847623bffbc8f5f06451310e9e34c1b2dfedd771efc2bfbb00ce5c5e91d6`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70e34a5efa1810481d9bb3d837c2921b9c74796200dc451e65394e17844da60`  
		Last Modified: Wed, 01 Apr 2026 20:15:48 GMT  
		Size: 223.8 MB (223796852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ad0bd4f400622ddd758f518fae4b1cf7041d10b110c1abc1c623a5e6a6789ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46715216abee9bb1460f9eda83e78a21aa19f87c2ad076c80a294c96f794fbe5`

```dockerfile
```

-	Layers:
	-	`sha256:385428ae5fd16e859c3388fc34732cbe1398ee43fe6abab926f0265e8fdcda1d`  
		Last Modified: Wed, 01 Apr 2026 20:15:43 GMT  
		Size: 2.6 MB (2619320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901ad8ca091f1e1f9e63ffdd7cca793ada119ca0e624c3e3ba38fc5e7db9985b`  
		Last Modified: Wed, 01 Apr 2026 20:15:42 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:00eea3d35056fb2d2f4d4729f2d8507c7ac018a8f5b214da7f99a369e1fa9ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261780059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569189008ed2f6a50097304e286accf01070665e74881a0053e16cc37cfd5e10`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:40:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:40:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:40:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bd6753a676d1b87e9c2339dac138500afae05ccdccee82acf2846d6d097c8a`  
		Last Modified: Wed, 01 Apr 2026 20:41:40 GMT  
		Size: 227.1 MB (227130399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:482179cf07fa062103ddb5d51b691701452bf48f82818304d77ac670d83059e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92540f6d3ac1f8f1492d65580f9a4e64cf3b0b233e6fb8d5b33de805f0557b0`

```dockerfile
```

-	Layers:
	-	`sha256:687fcf00d15cc19b01b8a069e548c666bf9630c5d5b7620d5b8f322c86df6cf7`  
		Last Modified: Wed, 01 Apr 2026 20:41:33 GMT  
		Size: 2.6 MB (2616585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:426ff8323409f8ca5bea282368a2fca5edd9dcd9af1b48b9cc6578d80f186589`  
		Last Modified: Wed, 01 Apr 2026 20:41:33 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json
