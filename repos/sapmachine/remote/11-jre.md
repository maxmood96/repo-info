## `sapmachine:11-jre`

```console
$ docker pull sapmachine@sha256:6f6882a6843c14e5af4d7f844ea1065864a30ed85a0c69d37e7a4066b8d1646b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:8ece65ce59fd33a511920c790a477ecfcee808ff42e34e236e52e6a2a117820f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79796175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25431aa13aae2a4b2732f6704073a7d59a6ee89942e6fc914b5626f6c603abed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 21 Oct 2025 21:30:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc87173dd1fd9786d7fde7dbc99af79777284931e3b84ff19158cc446cfc47c5`  
		Last Modified: Wed, 22 Oct 2025 02:44:58 GMT  
		Size: 50.1 MB (50073028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:88033a5fd1349c70f028d05fd2180a5e4a65c903c01521426cd59de5862c5983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e29c1200fa28fbde71978918f4e6e7be8432756ec46fd3827d05de763633620`

```dockerfile
```

-	Layers:
	-	`sha256:1b522f5f9fea71814853ee53757872843116b92eb15c3698ab70ca1d8e563f86`  
		Last Modified: Wed, 22 Oct 2025 06:04:48 GMT  
		Size: 2.5 MB (2523633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdad9305bb40320ee378ffcee6a383eb00737180172a646340fe968e82b47893`  
		Last Modified: Wed, 22 Oct 2025 06:04:49 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json
