## `sapmachine:lts-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:deffaf1c3e26cdbee814206f7c3d812049be6b34735588a2580b0425edbb6220
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:af6f29c844d49f53665f6c44c85e961a302f53934487e6e19bb2486a1a2f5b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89416998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926fa71027375f529919313d0f72ec9a3e809bbfae56a2f478591ebc35c4e5e6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d02fda6d8fb2aaea02fdf781122f51b4dfe83a7393f18ecd65b1a8366893a4`  
		Last Modified: Tue, 25 Jun 2024 22:58:44 GMT  
		Size: 59.9 MB (59883244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09dab71989071ba798beffbcdf11da703101fbc2181eafd3bb31c108c4a416d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04be9dbd64df6d865d3f3ec358821513a0d1a1da925266e0c2814db97884eaf9`

```dockerfile
```

-	Layers:
	-	`sha256:2229b3d9fb5719d9c1282e56b0ce2495bb653c2143a6fb9325ea3a4bf6c3cea1`  
		Last Modified: Tue, 25 Jun 2024 22:58:43 GMT  
		Size: 2.4 MB (2359977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fbcaf81fdd19e248fa77a442eb057bc8c6a8199a2fcc4619db06583715cb97`  
		Last Modified: Tue, 25 Jun 2024 22:58:43 GMT  
		Size: 9.2 KB (9243 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4b2e815ea275f4b3595adf0a3b7a00194efe3c1cb2678deea4cfa1ee20549f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86290808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f32999bd07b48a0b148c3b680cbbc98cc6b0af9a6adb9b1a0dac8969907937`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039176196596b8b83f43b8fc4f224096fb9e7603c16afda8313dfcbb2638514d`  
		Last Modified: Wed, 26 Jun 2024 00:08:57 GMT  
		Size: 58.9 MB (58929026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a7b652c1a9b568662aaa6f37e9bf250de31312cef02ecafa63da218af2ea8e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06825022d4a8866fccca1863a39a5c71ccbb5c2669a172c53d35f883c33630ae`

```dockerfile
```

-	Layers:
	-	`sha256:cb1c20f080f86dd0712ae98a8415667121743ce4f68d0334770a759f5ee0e984`  
		Last Modified: Wed, 26 Jun 2024 00:08:56 GMT  
		Size: 2.4 MB (2359681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab9454270fc137d705366bc31c59b32175da8bef98c653cc1b230a2a3f502835`  
		Last Modified: Wed, 26 Jun 2024 00:08:56 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:641c5f75bdc3cebdc2cdf3e3d9ca8fa02b9c9a6a548699b59fdba8a863757f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95893843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d9f8afa00f54b7e471b0696670d8296417ff6cc98c9a9110c55959c24e97c4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0695937578c60f19feb0e88fd833013f7dd6f2a9fa1699b1c8c03c80019eb0`  
		Last Modified: Wed, 26 Jun 2024 00:37:00 GMT  
		Size: 61.4 MB (61433150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6cc662b327ece045c775eb84da4729d8b1b223ea7f86a3cdac84c622f3d7340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1014ad1305d4eb94fc701a99569f2c8408cb8f557539537d2fd15c1c1e4254f`

```dockerfile
```

-	Layers:
	-	`sha256:f3ff08497861a1f84d689fcd35a35e9e3bb5283eb72ddd67f07bc1175af172c9`  
		Last Modified: Wed, 26 Jun 2024 00:36:59 GMT  
		Size: 2.4 MB (2363968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf6a8b6dbedd3dea0362fb403d1846df3d123c005426eb4c1c7e2d8e6490fe8`  
		Last Modified: Wed, 26 Jun 2024 00:36:58 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
