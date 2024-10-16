## `sapmachine:23-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:48f6397166386092f31017ec2aef5b444695701c05e3f67c407b8688829bd26a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:65ac80cfe8a5a4b87f00c7076b5c9462774a4d33fdd390b10a488e61a6ec48db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248857810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6001f2d3c3ec320285aa6b921083bcb1d77d2a51e0cd8da45bb7fbe9c20da587`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50246322460b061c017415db05408d43b5861488e205744cb27f12daa6afe420`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 221.3 MB (221346758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38e8ff5917db418ea96013ff1850d6c838995f494853f8f78963474f8e4b6bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c666f5a81eb8fbbc4496d0c74af01b5a8a01583776aaa066d34800225d469f6f`

```dockerfile
```

-	Layers:
	-	`sha256:b6b5557b9c4b5fa0379061708c82f242bec98dac27e7e4514bbbd90790db2452`  
		Last Modified: Wed, 02 Oct 2024 02:00:06 GMT  
		Size: 2.4 MB (2368383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a84241737141e4e095b75ff218e3ead7df490af94bbeae8a04823d80dfafad`  
		Last Modified: Wed, 02 Oct 2024 02:00:06 GMT  
		Size: 9.8 KB (9812 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4a53e40349ae5fc11292e498c7e2b083e4e8a6c070bef9ce00b95a85d4c0f7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245284159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaefc3fdf51a642f8d1883f9d76ad04e1908f548d8757c1ad077ab902b0b9f8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10714dfc841323c62fc31bd03dd7f00ad0edfb018768050629a8dca995abc4cf`  
		Last Modified: Wed, 16 Oct 2024 04:23:13 GMT  
		Size: 219.3 MB (219310331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:263049848bfb74a837489ca98f30365e77f4535c4cd13ce7ed3541c07fe9c5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1faa2b42ed380534402c5e888a57d659599389ee2827e44608f74836e16816`

```dockerfile
```

-	Layers:
	-	`sha256:b7cdefc2c60f0d13105f0add868c34f9a0f2fe92f736d2a95041a2ac840c6dad`  
		Last Modified: Wed, 16 Oct 2024 04:23:07 GMT  
		Size: 2.4 MB (2367436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66baffa92c5d1985a76a466da414b4de7b3e64d47344996317202214e4a78c6`  
		Last Modified: Wed, 16 Oct 2024 04:23:06 GMT  
		Size: 10.0 KB (9991 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:caa54218a2e895e58e8b323086e8d220f5ddb5c00505c85c226da780a91ac466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254014261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67c7b8f45c4d2defcaac4db0d8b4d47fb1e162d94d240ee314c343844175ec0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34124117bc27b34540954ea282a68261de0ceaa3aa5d857f2d16af947da64a8d`  
		Last Modified: Wed, 16 Oct 2024 02:39:27 GMT  
		Size: 221.9 MB (221937755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:56eb236b822020b6b9a52fa59a26f55a8394c907bf0441a90ba9ffb4743adc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d87f84bc566a120fb8051f6e28e80cd40cf010388957c4865f1d240805fb99`

```dockerfile
```

-	Layers:
	-	`sha256:2024c45ac94b47cae316f7fbe772b46dc440e79808b8e883a23ff68d2c1ebb40`  
		Last Modified: Wed, 16 Oct 2024 02:39:21 GMT  
		Size: 2.4 MB (2369604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c8698310c0dbb0a99b2bd653f0b937c7ef6aa1be5a7fc1aa678dd094fce798`  
		Last Modified: Wed, 16 Oct 2024 02:39:21 GMT  
		Size: 9.9 KB (9907 bytes)  
		MIME: application/vnd.in-toto+json
