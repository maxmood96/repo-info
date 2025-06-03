## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:4d6d2d0d911565594fd3d7b0b1a4a7be15dca1d170c140e675a5f124f53f0c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d2675e977d8fe38af57fca05219467a90b3c4c6e2c2545167ae3f65ef3c4b23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243047190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a61270e13183dab4163affb3120702f2d39f7b98a16a2e2fe220aa3c3be2ca`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f8e3e0c2ad46dd3d4ba5effaa8fded6288caa2f3986862a4f31249a218da27`  
		Last Modified: Tue, 03 Jun 2025 04:18:05 GMT  
		Size: 213.5 MB (213514187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:51e07869b1281d20a14e7525853222b0a5528ec9bf569b616a1db38ec6d12cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576293aefa9b5fa5e4032ae455a5a2dddf372fc7d998db172ab0cafe73c6b01e`

```dockerfile
```

-	Layers:
	-	`sha256:81ec57968c3ff281b32bf571cfbc89de1ef4d4a25772bb1efc1698def7fa5df6`  
		Last Modified: Tue, 03 Jun 2025 04:18:00 GMT  
		Size: 2.3 MB (2273531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d6cf8260a229de2d5026ad209ae4e3ea4403d556db854345281ddf33fbbb38`  
		Last Modified: Tue, 03 Jun 2025 04:18:00 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0189b074bbe10e0b25c1579a9e32d4d881f37e34c55eda8db381b0be46dc8351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239075463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd83b99fdeb3579d919615b48ebaa47af91457a8d241449283889d0dd525c07`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612907d6148f7a5a70515df1a563cc9ee0e94fb8903390dc29846d3dfcefd311`  
		Last Modified: Tue, 03 Jun 2025 06:05:27 GMT  
		Size: 211.7 MB (211719882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7d848f27184108c07edca4d1726a8967e9a02a731706c319e8af303999c5cd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e6c0695379e828696934fad2ebde8c4e30d0f9e05983e5c8970e539091532f`

```dockerfile
```

-	Layers:
	-	`sha256:01415913950876f472d4786b4b78b45a7d8b1630f40ecf7d47559257c0210aff`  
		Last Modified: Tue, 03 Jun 2025 06:05:22 GMT  
		Size: 2.3 MB (2273227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf418228f7906c3783606232a3d5d228fd3a83997638cc005b909115da43239b`  
		Last Modified: Tue, 03 Jun 2025 06:05:22 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6595e7bc30eed8f2e9df7056dff60cb89ffbd48881666ae10643250c05b53951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249067083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4f865fdddfe0a4850317f2d7d45b96e9c2434e66eeba7a5b2d29310a479d57`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Fri, 30 May 2025 23:35:04 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0911301000cd24c914fc4df4ec4bea8f44d85757a7a7e51885f715c674e69ed0`  
		Last Modified: Tue, 03 Jun 2025 06:08:43 GMT  
		Size: 214.6 MB (214626726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9090f8c69413db56cef9ff3175343280e90d2e7e1271c01cad6d6b5f382acdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4c1684fe33442e22374e83dcd49b1cf0e10535625fa6936c9501d59f047abb`

```dockerfile
```

-	Layers:
	-	`sha256:499781b24aa8e939af2ae8c8eaf5c851ec38f2ee3b0dfaa992daae52c008478a`  
		Last Modified: Tue, 03 Jun 2025 06:08:38 GMT  
		Size: 2.3 MB (2275638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdced6d3a9d4557058122bb0e172f463bb963d56a63a2ced3960410c0defca0f`  
		Last Modified: Tue, 03 Jun 2025 06:08:37 GMT  
		Size: 9.7 KB (9684 bytes)  
		MIME: application/vnd.in-toto+json
