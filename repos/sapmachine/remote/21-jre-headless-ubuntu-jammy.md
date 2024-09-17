## `sapmachine:21-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:fc769ae407bf9bc7bddfc13e68a3e78487c1b0433dda216dd9e0438e0363077b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:fb1c423a724c06e2026dec58e15d1333bf97ab1ec55c87f543adb2f3841c7d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88262100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f5aec634e48f2f052abc5775005d0b537da73df547933ad367150fe9292b57`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbebd286ab9fe1c68d065057513544ced0f15387b9beb7904a271ad5d0b0529d`  
		Last Modified: Tue, 17 Sep 2024 01:00:49 GMT  
		Size: 58.7 MB (58726412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:63d8f13d29b40e4729f86b57ac578ea9a2fe3075d3c179270e7f872704a8f5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7231b391fc3f23c2b72811a020473cb652d38846eced699c6aba1015f50626a`

```dockerfile
```

-	Layers:
	-	`sha256:26a3d55897c4af81a2038ba16c83cb8a24e5b2b100dceeb2e1b0cc92b013ca9d`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 3.2 KB (3163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c60ef2fe719552725cd6a142e03ef4a3add5d13fe34ea4442976249b221c2c`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2d2a1fe984007373e19d7a1b877bf5fb567fba2391c288e08c2737e0468cf675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85137582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee81da809d11bb7eb60ec1db7af740fab7a232420c8d0b7765017a1b472ac44`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6afd84c4c9c9204ddc02c3b190ccf10e083507a66a9a1948aa4a0da43ce43a`  
		Last Modified: Sat, 17 Aug 2024 04:23:14 GMT  
		Size: 57.8 MB (57778899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8920ce385567229476142fad8e781c01633f71499a73c20f1cfd7c4a7eed89a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b67b87743133de900f70cdac33124b887a7d98e6c962e5f2a3ca70b5fc17b2`

```dockerfile
```

-	Layers:
	-	`sha256:a11c07ea6b5702014ddc9d0f1facc1fc306f30c386bff6cc2c3282eb91d417e4`  
		Last Modified: Sat, 17 Aug 2024 04:23:13 GMT  
		Size: 2.1 MB (2147209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fab17a3a8a64fc7d97edcaebeb741067ac9206e7c4435aac0d0cc120806d56d`  
		Last Modified: Sat, 17 Aug 2024 04:23:13 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e95f07bb621aa06cb60820bc0f6d1d60ad35d011fa8e05b30416a217df958639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94576571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f261bf2730cc37c7fa86f9d8bddd6978b6cf8092f0c4ed07b01bf46855ed2c4f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b0f730ed44dfb39896c5490f8e02366e4e83459efe4e227655825f0061f7d9`  
		Last Modified: Sat, 17 Aug 2024 02:58:18 GMT  
		Size: 60.1 MB (60112393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27d31383fea6ad264a8dd88dfba7de923586c66aadd82bd0cedf087d992adae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecffa6ea76317b60c0efdf702e189dab57c880eb3f6ddeca42bff590596d32b`

```dockerfile
```

-	Layers:
	-	`sha256:bb531ce2b78d1851bf4e60bd79b7b6221009a2cdb95577c3144e48c2cf28ee30`  
		Last Modified: Sat, 17 Aug 2024 02:58:16 GMT  
		Size: 2.2 MB (2151436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee259b9049b9afe2312499fa199367e761446482603681cd6ffd3047b4b6c56`  
		Last Modified: Sat, 17 Aug 2024 02:58:16 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json
