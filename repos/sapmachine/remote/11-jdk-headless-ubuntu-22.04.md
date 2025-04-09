## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:5ca203ecbd8b81d141e519e128fd80d433b45c658019786ec4856cd01a0a5f24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:1ee6a026e8e11dfd44c6252ed0315124181d4b6d76eac3bd06176c4b873adf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229156187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec6f1ae8449b00751f67f8953c9a1faa151aedde405da92e367f3af162ec1d9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:19 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d500fe26706a8fc71890bc613e642a0013744bfb7cb62634ef34ede85b70ab0`  
		Last Modified: Wed, 09 Apr 2025 01:22:23 GMT  
		Size: 199.6 MB (199623822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:954459d1a9d7bfcbd1e519a50bc02e49eb3c60f2d5ee0ab2499121e6ec4a2da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2269332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911645e1ea4c6a1ee60dfff536310e6092b89930fb2c1a5ec1c8b60c1760a566`

```dockerfile
```

-	Layers:
	-	`sha256:fb851b0b555afff215a5153a0570038b7cfeebd8118541ef3ed2600db5371bd0`  
		Last Modified: Wed, 09 Apr 2025 01:22:18 GMT  
		Size: 2.3 MB (2260399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee706e6443a3126bf0b8fe1e12b24800621da353d1efdf3a279a26553ad6e6d4`  
		Last Modified: Wed, 09 Apr 2025 01:22:18 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json
