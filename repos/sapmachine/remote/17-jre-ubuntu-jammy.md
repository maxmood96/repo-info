## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:bf8957ee1492160cfec4054654222a218eb733de62dd4874fbcf2978bd494d30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:69577e45f83d08cf0a051718f6ef7e08060e23c93aea774f9f4245ae224e59c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83246300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d7c47b0395da12457bfc3b763d83bf82d59ca5b02e4d192b8d9ac81a76af22`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcac20d0e0949161583f8b3970738530271fa6896754e93ae1049c14ce039981`  
		Last Modified: Tue, 17 Sep 2024 01:00:44 GMT  
		Size: 53.7 MB (53710612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1db3729b5a54e7a5192726236420cdac6d6fd2f72e52b10a64247347093daf8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55901400703a80d4dd903d8c6a6daf24ca46e05d2cb5c30bd354bf24a41b87d0`

```dockerfile
```

-	Layers:
	-	`sha256:1b4acbb30199ae93131e6c13e97d7e977da0cbc94179f843a5d0d695e9fb2ab9`  
		Last Modified: Tue, 17 Sep 2024 01:00:43 GMT  
		Size: 2.4 MB (2386862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70013822a8513960aa451eb9f84d333f04de624955e8f22ca5f10502aab736c6`  
		Last Modified: Tue, 17 Sep 2024 01:00:43 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0fd2bb7f4d5b92f5f4f5f9b231f60c4ad6798701279c9e9f5b85b3935f4f9f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80404312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175222179804422f8eb252ee97d7a3d08bc0416fbc7707f4972de7797ea27a8d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d4cd1a3e8d3c80e436e69e0e16a1cc60182670c49a335afe3c790f7376b0b0`  
		Last Modified: Sat, 17 Aug 2024 04:36:05 GMT  
		Size: 53.0 MB (53045629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:89f4223ee5754826600c1c8c92c43c19d4a3e6cf065deb8e86ed1b27bfbe7c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bf26f316acc81333be1ead234048e26138e6761977ff6429fb26de0c194f98`

```dockerfile
```

-	Layers:
	-	`sha256:a51b5678875079ff377472cb4247159199b7fce26b65405850fd7f3be22caea4`  
		Last Modified: Sat, 17 Aug 2024 04:36:04 GMT  
		Size: 2.4 MB (2386542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73208645b96d68a28b71e027ce7f4760598b4ff74f09aa5aeffd632596c735ba`  
		Last Modified: Sat, 17 Aug 2024 04:36:04 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a899752995b76e6b53b8c7a97719cc2480e6abbca4288d6eab72fc43e37a2c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89643341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480248f78e54dd1fb4ac734f8ac173ad356cb3b0ba281e5c89ad371be8dce837`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46a9fb33d862e9b1db64cb7c7a0b6fa265738bbed3238683dba7b562f555df`  
		Last Modified: Tue, 17 Sep 2024 02:54:40 GMT  
		Size: 55.2 MB (55195099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dec425303a02701ed11c8fa1fb2c5efc321574acee3f160d7d52019fdbc57990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918ef1e64da6961a48192494848cd2bab0246d6e5a99b682b910088027417332`

```dockerfile
```

-	Layers:
	-	`sha256:e132c9d9a405252c82d66de3841307181963e8dd13fee9ec5f8b62904de61f07`  
		Last Modified: Tue, 17 Sep 2024 02:54:38 GMT  
		Size: 2.4 MB (2390841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bee4c2efb9be065f384f50f9160f31e91eaaa257abca926c655432cfd3d115e`  
		Last Modified: Tue, 17 Sep 2024 02:54:38 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
