## `sapmachine:21-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b1259e9e8bf71d81935100e3dc3386f087d571821f39581c0190c7be16429ca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e383121dabb07eb232b783c2bd90e49367e9a57b5ba4c76797b59ed8148fbd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243569536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe50f5db7f80dee6a198470a6196b12a9c2b63704944f4643b62354bce24b78`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748f0d75b658e205b5f67ae541bc7010bca43484787f7bb841ba35930c0b886d`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 213.9 MB (213851884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:73b66e5d215212c9108ee6566c9572a34c84af2b69046ea93d35b4d932c8c388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2faf67bca180418e20c711ff127d07905b128e004fef9dfb5c4b93012f726eab`

```dockerfile
```

-	Layers:
	-	`sha256:e64d495d6aa76153a220563f737df21c57de183a196e8e23f471098d9812df70`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 2.2 MB (2234505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12cfdfe8773ad8fc437778c9f6b5e2a3fdc6f29d01ebd28e552413174f829181`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3ded598c61760659202f57ab11fa1a83ba2f791c501a535d5aefcd48329cce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240977875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26f2a88d584f1c846678877bf7d5a81fb42534155d353cfd09054be1c65c248`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a88737c16f03783de88ca059f9f04b240545a0dd45b5b4fb646217d140a07`  
		Last Modified: Tue, 04 Feb 2025 15:26:54 GMT  
		Size: 212.1 MB (212084277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e789f8a78ce5e9ffe74b3f6dcb2d0a4038295e93982f3dd89cad6c20e9f86ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2248059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43abbcebe1c5d51fddda80c09b95daeb691867469630742be76910f300e8ff99`

```dockerfile
```

-	Layers:
	-	`sha256:3b6a0efb4593e3d61361f7ddf091a30902783be95db3e915ce9fab189eea9b0a`  
		Last Modified: Tue, 04 Feb 2025 15:26:49 GMT  
		Size: 2.2 MB (2237243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992c1a78b5581239dc6db96f04365153d816264092020e269513b63680b183e0`  
		Last Modified: Tue, 04 Feb 2025 15:26:49 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:914c5d8b1bd82426c9d9c86924e70ac4c48edfc4136486662416341556a423b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249409949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c85d0695b9e9a6c5af7c0e445ceafbc1959e87423c161c1bc9b12f44e27f77`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782dee025b5c816f7f16d39bb7583bd17fcff714afbbcc72f455477af3a8b365`  
		Last Modified: Wed, 09 Apr 2025 06:53:31 GMT  
		Size: 215.1 MB (215069082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:813aa783fa9f706340f0f173338b1e1eeaab6d2be7aa044a66127d8b785cdca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eac4193f450824badccc3c456ec1083b4b87f7c6f29801e80fb0047bbc02d3b`

```dockerfile
```

-	Layers:
	-	`sha256:1dca9390f81f2eef3318c118979bc7b7ba4d84dd9946b4c6588e2c864666786a`  
		Last Modified: Wed, 09 Apr 2025 06:53:25 GMT  
		Size: 2.2 MB (2236465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18951f2652e36b06dbe28693b65989fad63c524c64158dce5f09a49d5ab16a68`  
		Last Modified: Wed, 09 Apr 2025 06:53:24 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
