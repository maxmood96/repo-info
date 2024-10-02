## `sapmachine:11-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:416cdd9e4097c78b20d12e9824db5db44022ff6319554e989d9fe74e3ed13c7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:78b36c6fa448e5dc224df8257844d2fd37522f3ef2f7d3b080196012ed6ea915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75802310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e38197248e106d928a731695258ee6c9a9a3f75bd1892ce6f00d694989cc97`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab64aec7025a1bff7b9054901a25d4c36843bb5ebbcd039f2b1f3a76c33ca18`  
		Last Modified: Wed, 02 Oct 2024 02:00:01 GMT  
		Size: 48.3 MB (48291258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f1684a63e4118c1652f7437a8b4c294da9e55a4a8c83e82a3a836e2bb051ec67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2063116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082f93b1347d5f5807bd3fd051c180fc4738d54dc695749617ae7982cd9ec0f1`

```dockerfile
```

-	Layers:
	-	`sha256:341fb0cd0b79fab9c1f49f4ab8a970d608cf2f4a2db8c063217d7626cb8af362`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 2.1 MB (2054433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcefb110fe6dc536f7289a299a25dd715675f721097ce8a0637138fd61911ca`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 8.7 KB (8683 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3147fd2daaf43482875cbf9d53dcb8fc5df9429e48235c43364fa259f527ba85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73587269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43df638d50998d5c4e57c37f69405f529eba3e97c7fd12753b63174cd3eb54fb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac4563a827090afea54ada474a3e41af4fd473dfb6d4bcb1d8096170e962bff`  
		Last Modified: Wed, 02 Oct 2024 04:10:48 GMT  
		Size: 47.6 MB (47613677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:495d4e705aa0e037b1f12ab53cd13f1afb29c4d501affd8a88baceeffc32f0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2063469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946aa893ac4dd61b622a3b3232c1bcf19ab3ce14dbc1e28d4931abd70d66f492`

```dockerfile
```

-	Layers:
	-	`sha256:60dc4b58ce6f63371947ac8e9f3b17f38e7323d117df5f7c5ad84a1423f1b079`  
		Last Modified: Wed, 02 Oct 2024 04:10:47 GMT  
		Size: 2.1 MB (2054688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:132c4ed91bb50076b6d52e3421b9468defb2653d6096ea881f864671b56eb58d`  
		Last Modified: Wed, 02 Oct 2024 04:10:47 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:49d30758bbc5b007520ada05dd08f07c6a3fd07e064f3c2415c171c28e41e3cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78459818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93847b4a0395f2a0631c41e768310b5d6a575650d1b279ed4d01bfdbe8db306a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6227bb4d7050fcae52a127b68537ff2e746946d875db166efde6eb425a8b5335`  
		Last Modified: Wed, 02 Oct 2024 03:30:01 GMT  
		Size: 46.4 MB (46383484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a5f3f3150d89a93ac8a14eafc8034371e6e787ce5f7864a7baa80f5a430b1dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2066862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59b7bc03d0147af251b81704f1f679d215e3fd06c2ab5007df4f9616ffd5b1c`

```dockerfile
```

-	Layers:
	-	`sha256:5c8267efb8a6a8d6c2033436cfff7edad477a7cfa506c672a92ae6feaf2c7dd0`  
		Last Modified: Wed, 02 Oct 2024 03:30:00 GMT  
		Size: 2.1 MB (2058141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34459bb8851e9dc3a1abeb8113c256f32bbe763b718b0203eb2afe1b0414eb22`  
		Last Modified: Wed, 02 Oct 2024 03:29:59 GMT  
		Size: 8.7 KB (8721 bytes)  
		MIME: application/vnd.in-toto+json
