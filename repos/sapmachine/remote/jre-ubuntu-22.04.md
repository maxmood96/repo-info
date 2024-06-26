## `sapmachine:jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:60d34d1f52a7485ffd9a3c3bd0dc48d8f0b045a4cafebef3f14ec7266522f2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf7c465753c98d09545293f55bc100a62ccff71567ea4c69b6517a4e3eb4ca4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88871514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc71cc433b996857c80e2607b48dbe28509ef5285aca9ef7d3c755ed2a191fd7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683422a77e6a2e3b7e4d81a40ae838b3d4a86994ae61d3984bed6aa40461163`  
		Last Modified: Tue, 25 Jun 2024 22:58:42 GMT  
		Size: 59.3 MB (59337760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c9c52283190abe8a03f5d0e8c5eeeb97059ddf0552bfdf713ed6565d0389b23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdd909c802fbb648ee041ba0eb55163111095b310a8e783b50e8418390e6151`

```dockerfile
```

-	Layers:
	-	`sha256:df36de0ad0c9cce351a606f3d661bbf9d99349ee7be7c35462b067415e9ba77e`  
		Last Modified: Tue, 25 Jun 2024 22:58:41 GMT  
		Size: 2.4 MB (2360592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1bc81320ecde2511b3bb998544addb46285316c80c0d98fd382f7f3c07ecfd`  
		Last Modified: Tue, 25 Jun 2024 22:58:41 GMT  
		Size: 9.2 KB (9228 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:04da7e7922427c22bd622f6be96fe6a89dddf6b48f2be2a2254e54bb362a9c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85690773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8705d1e96901284fd95159a3a257f5841562bf3b61b5ef43593895ba5036a6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa4f8b843a640010b68f7351aef3491017dff003da99be01f10f309b1595932`  
		Last Modified: Tue, 25 Jun 2024 23:56:30 GMT  
		Size: 58.3 MB (58328991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6de12a0f7c65be5916740a641699b5d1631c71e5b9a86f2756a03f7ea1927fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78a96017b8d57bc6112a6f830ac879916202a4d15062f1a5000ad56d7eef34d`

```dockerfile
```

-	Layers:
	-	`sha256:e0ee300e8b228196f4a0b8ae4de284d02752740bb18197bbb96b8a79784e0ecc`  
		Last Modified: Tue, 25 Jun 2024 23:56:28 GMT  
		Size: 2.4 MB (2359665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f0e21cc0973b6f369d69ce578bdc12ea9dd26b1bbee9e72cddf47a20d50111`  
		Last Modified: Tue, 25 Jun 2024 23:56:28 GMT  
		Size: 9.6 KB (9553 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f28afa1a6ed0dd3b8f8fc4bf80a387fe7654dd751ae37209c7aeb7aea750e5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95230011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb1f3b7f5dcd91e32b0826fc03f5364de1c51ec1339c60d863469e6b592067f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467c21f11a5e506bbb02a2b0402e865637e58fd9671f176d8488b38f53306021`  
		Last Modified: Wed, 26 Jun 2024 00:16:28 GMT  
		Size: 60.8 MB (60769318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:49f8688dee51a3d7fa3e0e818b77051cef208171ed7f6932f60e647b3c0d5f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdf8b9aaa5f505aec20fcd6563c1b5dd74af9696d14a5a94e75384fe0d35fd0`

```dockerfile
```

-	Layers:
	-	`sha256:49edd96840c53138605fa5bb4b1d7778cc40f64024cd3b712bc55091d85ded9b`  
		Last Modified: Wed, 26 Jun 2024 00:16:26 GMT  
		Size: 2.4 MB (2363952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deda7108976cf3d0784a737e3235df5820f92d101a16cfc75d2858a964bb9fda`  
		Last Modified: Wed, 26 Jun 2024 00:16:26 GMT  
		Size: 9.3 KB (9278 bytes)  
		MIME: application/vnd.in-toto+json
