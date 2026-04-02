## `sapmachine:26-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:74db33444f4e22bad0b20adc35b825e7c6f31844b0b36a11483de00099bcc1d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e90354277b4ef65ea073448e319684dc901f1e575d9794b55429061701828e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88342787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfc2be5dc0155ccc6391861e4a5560cdeb7a440424e83cb8919c7f9f139124a`
-	Default Command: `["bash"]`

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
# Wed, 01 Apr 2026 20:15:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb70668c5f7cc91fa7141bc9cb97606a59731b899a6f6615274cd33c37390b6`  
		Last Modified: Wed, 01 Apr 2026 20:15:56 GMT  
		Size: 58.6 MB (58606374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:046230feee2ce45aab289c31d5850736906296ac62349ac7f042d8742fd6dd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54375e2c9b62ffc55a5382df23cab2c9835cab976b898fc3460ac6ed1196fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:285227f01a4d9e651cb28c76c527df7404573c26a0f80118d1b743a88ba58857`  
		Last Modified: Wed, 01 Apr 2026 20:15:54 GMT  
		Size: 2.6 MB (2551105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697cdf6a43a982f8eeb9c30fc7c88da6575f10cbec65589c8a91362f735de2b4`  
		Last Modified: Wed, 01 Apr 2026 20:15:54 GMT  
		Size: 8.7 KB (8727 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d9873fed500804fff790f1bb71c2cef91a5c5a95bbbb0af26e0e23caccd67311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85175619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594db4a4a52373f4f9d44b91bc8a64c4d289ed11f418043f69f4d1993101d052`
-	Default Command: `["bash"]`

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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:15:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de45dc6d93a922f7339d775131328a571cc3e6c94397b9678e53a0a8bb0d01e`  
		Last Modified: Wed, 01 Apr 2026 20:15:35 GMT  
		Size: 57.6 MB (57568676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:583f58fac7842c92a475844122135af5e3e232c03a897eda1fdb9589734ac847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a2fa8d335404589845be76a71c7f71bf4da756733531a7364f079f8aa79e15`

```dockerfile
```

-	Layers:
	-	`sha256:66cbb14077e926e60199ba7edc81931c4932ddc66e96ac03a5d340b876f6c780`  
		Last Modified: Wed, 01 Apr 2026 20:15:33 GMT  
		Size: 2.6 MB (2550784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1a5fd18a7ddd89619f87c81a95806990386dbb4379bb5b58d0d239f25dafc3`  
		Last Modified: Wed, 01 Apr 2026 20:15:33 GMT  
		Size: 8.8 KB (8833 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1e5cc6b45e8a3395f3ddb1ce544337b17f6d8b43791ae9fd7e59098139858cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94323543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b112c6961ebc51f7d9668c54f31704d1d935a919a7dc7b9ba2fdc003a77eed7`
-	Default Command: `["bash"]`

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
# Wed, 01 Apr 2026 20:42:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:42:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 01 Apr 2026 20:42:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad55fa8f2c279f3180d00c92cc7e06ea2b4104c9a4c9bfd79dd3c1087f295643`  
		Last Modified: Wed, 01 Apr 2026 20:43:02 GMT  
		Size: 59.7 MB (59673883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8da743783cd7b8353d7529ea75599102ddb21e20da1cbdac3c11e07fb9ff9bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4311e49d08300163c061a94b00b326c7c243a198bb1b038d0c6a3d7eeaaea6b7`

```dockerfile
```

-	Layers:
	-	`sha256:5159b2715b96db35b2f36c4a0ef6d5c3ef81b95077aca1bfc9f34eea2b3818f2`  
		Last Modified: Wed, 01 Apr 2026 20:43:00 GMT  
		Size: 2.6 MB (2550007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a811aaabe5b1c26dce41de9c5ef1e095a4bda4e444e9378b741911b6e06e3e0`  
		Last Modified: Wed, 01 Apr 2026 20:43:00 GMT  
		Size: 8.8 KB (8773 bytes)  
		MIME: application/vnd.in-toto+json
