## `sapmachine:ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2cab15026ab27d737ab8fbee8220b3bd72df87466b6b5fbdd8c9f0be9bf749e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7a74f7bb68b479634f7af1fc956376eb5ea3d668b6a952c2738d4b4b0a00360e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265754149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a31d724c84c0cab8d211d37350efc05a8429785c1097d61638a0eaf90c473b`
-	Default Command: `["jshell"]`

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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65354830e4ea032cf75d8046f111e56c89817184619b98ccd2edbcc3b83df04`  
		Last Modified: Thu, 02 Oct 2025 09:23:43 GMT  
		Size: 236.0 MB (236031138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:60e0d8bfc979bd3167bfbddfd5a63b9571685c74781b4abe0d9b58b9f5ae5af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5828481b72da324b6d9b18fabf1a8d9f0859b8e8cf9d120eacedbd795374e0`

```dockerfile
```

-	Layers:
	-	`sha256:c93e4270f47e558c9c40d0870ed57662d6c1d415aefcc39fe8adfb5f0e9d0d29`  
		Last Modified: Thu, 02 Oct 2025 09:12:06 GMT  
		Size: 2.6 MB (2598219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd02df574177a5c7dc75724b2db95f039d09cae770d722b5a30ddea9b47140c`  
		Last Modified: Thu, 02 Oct 2025 09:12:07 GMT  
		Size: 14.8 KB (14779 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:07dbdaf2931286ed843faa7680be41247377829d5970fc25930cb2b9e49c806b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262511739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5fab96e75e916b2a56a38ea069e45e4167256d3310ffaae08f53351fd871af`
-	Default Command: `["jshell"]`

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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526072f9bf013cc544e774f4dbe054ff1f5fbaf55f176df5adc7181f772276a`  
		Last Modified: Thu, 02 Oct 2025 03:34:30 GMT  
		Size: 233.7 MB (233650164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:80e53158d4311d502f124a8ca0f45987d6b7fc65abc713d0174703ff95609b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd98dc6de440ce2887a9e78f282b13db87aef1238ed597503573eb193c4a3391`

```dockerfile
```

-	Layers:
	-	`sha256:8708dbcf08a96b3c1abbbbbc289fdb75ed68df5ab2cd00664acdf88cb98116e9`  
		Last Modified: Thu, 02 Oct 2025 03:10:04 GMT  
		Size: 2.6 MB (2598912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcdc979db020382602c053f9797614b846f71c698c595ac9be04ee41f6608b3`  
		Last Modified: Thu, 02 Oct 2025 03:10:06 GMT  
		Size: 15.1 KB (15111 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4ff765f20fd578b26d8f919406463ef88cf813aba017837dc58dfca79bb544b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271422842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7775612951297bb9d2a4f39300ed9702a62bac0a50a144d155edbd7eaf756e3f`
-	Default Command: `["jshell"]`

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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2916723ef805077b21c00c74bd83d47da74ee190f326e7bab08e1a68cabb2f7`  
		Last Modified: Thu, 02 Oct 2025 20:50:48 GMT  
		Size: 237.1 MB (237119295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:14ff0ba63fe33c73061969f58eaae2971f17f447365c490b428ae1056cfb7e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c7c9b12de4724d3abba78f8826d6546f5c6cf77472f56c4c873170eaee514e`

```dockerfile
```

-	Layers:
	-	`sha256:18f42e4dc729e189cd7968acbe9a982817473f63aed60cab07f3bbcdd0394cd4`  
		Last Modified: Thu, 02 Oct 2025 06:10:20 GMT  
		Size: 2.6 MB (2593826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d133a71c5706b3f330bc02bb8f0cc1da2f0f716ca94e51473c04f9b7a7fd0a`  
		Last Modified: Thu, 02 Oct 2025 06:10:20 GMT  
		Size: 14.9 KB (14937 bytes)  
		MIME: application/vnd.in-toto+json
