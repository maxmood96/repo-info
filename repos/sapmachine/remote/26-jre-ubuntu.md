## `sapmachine:26-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:788c4d47fff488a259371edb304ef795b60848910a180549bc3685b4a383d43f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:a2348605bde4ea52e216ccd82e56192b633618a4b1b238252dfe29a86d99b3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88732326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8115235e5dcc2c0c6c780ea03065e9d55bd5c8ceccfbc2389b0019ccea3e1d46`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:32:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:32:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a3f60f5301365806e19281f50f930dedd0ae0d2431d16b8eee4200c63b9e4f`  
		Last Modified: Tue, 07 Apr 2026 02:32:27 GMT  
		Size: 59.0 MB (58998867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:97024d25a1dc85daa49b3f8f02ea2787a780952f0bd47a6fa576d3e37abe8bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2534816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511daed1e5f5554eb7c3a81385693db465ea32c88e4e343b02920c44b7a85f7f`

```dockerfile
```

-	Layers:
	-	`sha256:a564fc2ef8073a9ced04c4508b114d5c396ab35c01fe647a2a877e91fd783f68`  
		Last Modified: Tue, 07 Apr 2026 02:32:25 GMT  
		Size: 2.5 MB (2524848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c4f0f97eec7c776fc8fc07b5cc7c64c81a3b60ca1e5f112caddedf3c06f013`  
		Last Modified: Tue, 07 Apr 2026 02:32:24 GMT  
		Size: 10.0 KB (9968 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d5e234e8c57d70dac04277f44c1cb01751826df73574317ca8921628746c0bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86880971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b7db094dab5e14f3892505c23ab08e3546a5bccb8f939c09c78e6383acec52`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:38:28 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:38:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:38:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217e9fb9712f90d4219d18bf26688c2e972f2a34c5ed37bd1e6aff9177a59b6d`  
		Last Modified: Tue, 07 Apr 2026 02:38:41 GMT  
		Size: 58.0 MB (58006896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:478eae06e340db1ae6de0abbf51914eab0bc16cc7eb3c51537777cfd38375aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae13d4b63df77f4a81dc399b7d5068879388acad3c8be07dbf623c8e05fd808d`

```dockerfile
```

-	Layers:
	-	`sha256:2484992d1b647d4400310fd719937cd264ec6c42d1f1d6d153524002dbc5eecb`  
		Last Modified: Tue, 07 Apr 2026 02:38:40 GMT  
		Size: 2.5 MB (2525361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5198cc6a9bc5f54913ae7c37a8824533eb291123435bb371b49493dfbc17f2ce`  
		Last Modified: Tue, 07 Apr 2026 02:38:40 GMT  
		Size: 10.1 KB (10121 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7c1e0b75fc5103626813c3b8860fb0c4bdc3f99d036626361d864fedbd2e6bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94470603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5551f3840bc62ce8cabf29bb0b1143ddf1969bc42452a6393d8abeee536bcc0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:00:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:00:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 09:00:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a162cb2ae672a56a2796ec1546bb7c01a940e3647f8724af8bf9be1847b6adf`  
		Last Modified: Tue, 07 Apr 2026 09:01:32 GMT  
		Size: 60.2 MB (60157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ac00f9fa4237b18e434732a3d115f11a5ffe77f841f1ba38630ed3f00d06ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329da9b9374144639aab412f30d02633981727cc3700253cbee78b53b861741f`

```dockerfile
```

-	Layers:
	-	`sha256:8c9c68393ff73bb2d7c73f22551c3753c99cd846677261e8cd5f9cfb8bbcb236`  
		Last Modified: Tue, 07 Apr 2026 09:01:30 GMT  
		Size: 2.5 MB (2523716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:150f41a0f3c5833e19151f5097e3de409867a9322025c2f15f65b17f01d75c5d`  
		Last Modified: Tue, 07 Apr 2026 09:01:30 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json
