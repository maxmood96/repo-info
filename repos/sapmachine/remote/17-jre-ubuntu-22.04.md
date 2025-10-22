## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:028ae30399f564d78c855f83c2c3dfd0b961653058ff0c7714d5290c9a6fa12b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:9dec938ebd2be2c6a741515f90d87f20c010039e0f19a25a6cfb3af49e1704fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83466762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb31269eee14a4e61cbae583e93a1b4dccde18aad3451b24880e3d648f474f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8293bd2d8231cc7b43f44756f75cab04850f3c0aae4293611eb59ac924ccc`  
		Last Modified: Wed, 22 Oct 2025 02:44:24 GMT  
		Size: 53.9 MB (53929944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:15888b56ed7cab4397921bcb74a547e5e03fe54017edf783cc1d4e04d8ff8362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6422b718ad87cfdbc6a461554528fa8008f0d63023162ac551edc186dcef741`

```dockerfile
```

-	Layers:
	-	`sha256:4e70a6a9d890493358c1ab926c593b403c8dc3779ea3b3d998a46f812a542090`  
		Last Modified: Wed, 22 Oct 2025 06:07:47 GMT  
		Size: 2.5 MB (2543639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6ef0b0ae08c18b51e462c212293ab68c81fab19e0b273637b46163fd910eaa`  
		Last Modified: Wed, 22 Oct 2025 06:07:48 GMT  
		Size: 8.8 KB (8817 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:920631d68d686013b8345b63cb6b250f015fdeca974a76b91f60571d40aced2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80694522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45baa19343a8e94b95bb1c1180f3bc4938e41a7bc6e73d1dd9019b265c16e244`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0447056a045cf6361c02fc376dff61f7a9083661744c829f60d7c9f487b6e2`  
		Last Modified: Wed, 22 Oct 2025 00:06:50 GMT  
		Size: 53.3 MB (53311415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b56e9159f33b1504a632902f9544f5522c848a391fed832b07dcc08c3effe469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c9a78346abeb2286db72f0cc53ebd0468a108e884589ed233e01c8ec863cb`

```dockerfile
```

-	Layers:
	-	`sha256:9d478b9f6eec94862bd5e3e7617d0557f12c039a5e7d9dd4989d59cb0d47fcd7`  
		Last Modified: Wed, 22 Oct 2025 03:05:41 GMT  
		Size: 2.5 MB (2543321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d32f5b5e44e97a34b5ebc3a850e965f409fdcf1018e5df92ce159d2a883e2c70`  
		Last Modified: Wed, 22 Oct 2025 03:05:42 GMT  
		Size: 8.9 KB (8921 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6700ebc45a9cff80b4a4df6af7ac9f8a064d4d9b7ab0ccd606e47184c65ac2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89391562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a6a65aaf629d339e546fc309140b6f551d1d6bf3764a908a414c91db98f97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4259d8033f30bc4b649845e2525112964031b105224cc1ebab96c79633621343`  
		Last Modified: Thu, 02 Oct 2025 04:53:16 GMT  
		Size: 54.9 MB (54944773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d298b32060629a4b9c4656a063f2ca15e3e2388ea5349296293ac7517f8cda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2550615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4498495c8cc5767502832b98078aac26a227cc0ccd36f54ea8073845a4199b7`

```dockerfile
```

-	Layers:
	-	`sha256:f9c06c66cafa218abc6c78d9b02d6679ad5d760df2e1c00b07eb318e7fdf629c`  
		Last Modified: Thu, 02 Oct 2025 06:05:51 GMT  
		Size: 2.5 MB (2541754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c54b8e66ee3db410b9cdc9e5fb787344d35f879440410fdddcc2b072055c8b1`  
		Last Modified: Thu, 02 Oct 2025 06:05:51 GMT  
		Size: 8.9 KB (8861 bytes)  
		MIME: application/vnd.in-toto+json
