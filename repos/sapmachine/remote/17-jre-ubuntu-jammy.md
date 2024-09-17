## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:20af8d5e13f5f6390c1b009e3dbad9605c0b63e450cef39b747dc919870155d4
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
$ docker pull sapmachine@sha256:29e514ac5d0f08cac5d5241377ee3f3b19ec8a7bf06fc9bdbe7d11b7e4dc22c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80403884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f770428a2c8aac1d6dfd95739a183fb11ce875287f508b5f2c63a5e1a2b9e29a`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d1c9962e555f86d7cc230f84fc95a2792343bdd69d9ddbb97167f1d6a03713`  
		Last Modified: Tue, 17 Sep 2024 03:33:30 GMT  
		Size: 53.0 MB (53045555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:662adb0b9438452390d30a65ae0c885e2f96537b34b4d5358ade090e97af3a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a59b76f1fe429c2d7dfd8090d6cb5f0466c659b3eb3988c565d9a65d24e6c7`

```dockerfile
```

-	Layers:
	-	`sha256:0564704d7df196ba782e07a617213593d229f810329c0f90156cde0fdd321c08`  
		Last Modified: Tue, 17 Sep 2024 03:33:29 GMT  
		Size: 2.4 MB (2386542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f42893ff09e4a0ca22805e74ae0167ca1bd04a3a0d1b6da6b9ad7be3d7350e`  
		Last Modified: Tue, 17 Sep 2024 03:33:29 GMT  
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
