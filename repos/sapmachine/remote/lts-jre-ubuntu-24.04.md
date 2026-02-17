## `sapmachine:lts-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:53d1dc303de6daa7a69cc6f5a2558d30ee4fa0d06064515800fe26d34245b790
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ae2882fd834c22e1f6e993ea573a925708be39dd054c0b0914a24386bc8e1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87457833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedaf613af496127990e79a2c61e52dffe1e0c6db1cedc1b8a94487f97d8ce1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:33:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:33:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dfaa78ab15a17612d9d9e1cb64f1e56786d22ef41164b6e078802b3c0a5d2a`  
		Last Modified: Tue, 17 Feb 2026 20:33:20 GMT  
		Size: 57.7 MB (57730222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:efda3420d63d646d767e117c564335adf87a5948f340ea8d1fc518b6579d9755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2540693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d3d1816d3f344fe5e1dff039f0b5d903a15c60a87a793bb39be70e3b681dc9`

```dockerfile
```

-	Layers:
	-	`sha256:50306baf62f8608402c48955319bcb9f3a92134f79559a0e14d2c4b681deed90`  
		Last Modified: Tue, 17 Feb 2026 20:33:18 GMT  
		Size: 2.5 MB (2528400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0289afe0a4b29a145abb31709f6086de95bad694c3096f29da49ee2d0ee1c554`  
		Last Modified: Tue, 17 Feb 2026 20:33:18 GMT  
		Size: 12.3 KB (12293 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:75c269be19ee98f38a7ca646477c0e72c015dcdcaf2295887c328e8fd48f6ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85566958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0842df2754af318f0801c7bb350fd6687f308d5e169ccbb1ade71d93b08bfe65`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:32:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:32:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc06c70042f4709245b706e81430082c5d5ea50f01d7766faecd828a8f94f56`  
		Last Modified: Tue, 17 Feb 2026 20:32:28 GMT  
		Size: 56.7 MB (56701838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c1a7058c231e8b6f70fe2db1cc4056e02859662d000a0bcd647509d54257adf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78a9f56b5fbafbaa91389f900508b1b8d268fa72f5ea997a650f8fc0e7343c7`

```dockerfile
```

-	Layers:
	-	`sha256:82c87ce169335a879efcdf9c84a495133e65d9fd8486427be218a9cad92b82a4`  
		Last Modified: Tue, 17 Feb 2026 20:32:27 GMT  
		Size: 2.5 MB (2528997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8346e0ebec07971c8507a7cb90e6b1301f31e5440070f92968130dbbda8ba7`  
		Last Modified: Tue, 17 Feb 2026 20:32:27 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b7f0f9cdb7d29f7ac02a09800760134456febb301c5d2e058e2a251f4be1e119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93045837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3640edaa48d5ecbf1b7dc2c37f44894fdde6b54a9002fcc88c8884625ad6da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:19:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:19:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:19:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3a9b7c34b820f9dca62c36b3aa582b26bb6ca2e772b77bce346df8a31623d3`  
		Last Modified: Tue, 17 Feb 2026 21:19:43 GMT  
		Size: 58.7 MB (58738931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6d5c60481a10b06fad0a1d484c8e9172b06bf424d9635f92b830a653cfba568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccffffd4c24b259a767c6aed65be052ea96dd90ab3d844d5cbfe669d946ab31`

```dockerfile
```

-	Layers:
	-	`sha256:341af6e1a0bdc48dbfda61e0ab42467bba1fa0a5eee2cc904bbcfe42fa00b8dd`  
		Last Modified: Tue, 17 Feb 2026 21:19:42 GMT  
		Size: 2.5 MB (2527310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6267532869a46622fd1ab493e097e8143294b46d1791f077d8cd83d6cb107c`  
		Last Modified: Tue, 17 Feb 2026 21:19:42 GMT  
		Size: 12.4 KB (12403 bytes)  
		MIME: application/vnd.in-toto+json
