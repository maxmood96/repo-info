## `sapmachine:25-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:e84a1b1026651f1f9b64810acb59f3239eff899447f96bdfe2ed3a6f5b1961ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:158b05669120e09cef4fde1f562806086d58a7cb6f33273a269045da6e780527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98698963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b6aa4b16fb2244b29e56981edbb89a41f1152d5274c6814eb86de375e31d3b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d6961eafd5b9caabfdc855f37dbdc7aba926d9e5b51cdc32c0b72154d61ec2`  
		Last Modified: Wed, 17 Sep 2025 17:34:53 GMT  
		Size: 69.0 MB (68975513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a61e9e60dd8b7d83cee0de48c5a3f478528a76d7eedce8ceee64da81fdec7baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6cf7d607375789d3590620ce7c91977c1210fd9a45dc6a6c991fa7cdbed643a`

```dockerfile
```

-	Layers:
	-	`sha256:c0b5f02e28ed789e7d817ea75d141fcb49b4a3fd64a7085251afaebff9f44773`  
		Last Modified: Wed, 17 Sep 2025 21:11:25 GMT  
		Size: 2.5 MB (2526608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f3c232f493c2fb14dc2942bbe75abe2dfdb2c785c4ac6d3682a0ad32a3157b`  
		Last Modified: Wed, 17 Sep 2025 21:11:26 GMT  
		Size: 11.0 KB (11002 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7a92082c20c3025f15c743337bcb4976d259072d727f49c41d37cbe3e1281c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99032635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcfa83dbfde639127c81ef61aded317fc32777280a391727a552015f5a37098`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0df485ef5735317c96130386faa55a14f4f9e5805ff91db04787fcd21f8e3e6`  
		Last Modified: Thu, 02 Oct 2025 01:33:18 GMT  
		Size: 70.2 MB (70171060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:697517b5a79b0ccb1a11773dae3b02da059c2fab1ad3b6e04691dfec2239f0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6988231fd3182952a10c5772ca38e23bb92615d02a5e5a6c6277ed62c2f1d89d`

```dockerfile
```

-	Layers:
	-	`sha256:49ce43cac19e7eeb8fcec6398bebf342986036b05c6a1fb92220b97ffbbc7c0b`  
		Last Modified: Thu, 02 Oct 2025 03:10:47 GMT  
		Size: 2.5 MB (2527157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb42d05482c593c200090f4037dfce30fd2f1d9b58844bf548450b6cc99b2791`  
		Last Modified: Thu, 02 Oct 2025 03:10:48 GMT  
		Size: 11.2 KB (11190 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5e305de8ddadfa12d26dae1fdcaa58db27df386c411524c280301cdfe03dd322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106843304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14f56bcb38901b71c401b797250bd82dd8c4fceb263f6343fc8c4372e430277`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eb62c34c15cdddd5b94ae59eabeba45ad2dcf60055f3e30ad4f001c81eaea3`  
		Last Modified: Thu, 02 Oct 2025 04:15:27 GMT  
		Size: 72.5 MB (72539757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea08aa0c48f0ec6044db10862769835480865daa43a8cf0d88871a944ec1af28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d0eb45c56bedae9a8edc283e5d46903b5c285203bcfd8b6dad4af05fc0f677`

```dockerfile
```

-	Layers:
	-	`sha256:85b7fa1cb04c5693f2bf6d9e4bab47964f8d167bd26ab0fb89c6abd2b1657240`  
		Last Modified: Thu, 02 Oct 2025 06:11:03 GMT  
		Size: 2.5 MB (2524077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b2582a821b9ff07893a77c2168ceb955cc975b1aca1cfd960a730797508bbf`  
		Last Modified: Thu, 02 Oct 2025 06:11:04 GMT  
		Size: 11.1 KB (11088 bytes)  
		MIME: application/vnd.in-toto+json
