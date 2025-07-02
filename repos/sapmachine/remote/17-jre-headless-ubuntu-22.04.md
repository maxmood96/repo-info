## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:0e83fd2621cc330e3865bb323dced884bf5bcdb3da905e2c6914be7c63ac80a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:28b3f45d16d117a0f0118573019ab0d9136c9d980df4a3b2e57758b1f182a5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82138035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38acbdf791065d94f5631227e690fdec0292b7d0c3a0f21df2587b35a4c58b3c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7610291973729a5934180b411c358479c09bb21f3c2413de4bb009cd6babe875`  
		Last Modified: Wed, 02 Jul 2025 06:07:35 GMT  
		Size: 52.6 MB (52602349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e5de6996d2de25aabc58b94b96490d580b678ad7fc966552bf4c82c355c78804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d8acbf1f2b4cd2098f3656ac828642a6676369371c7d5342de61c3418b2849`

```dockerfile
```

-	Layers:
	-	`sha256:dec7c70afbdfbd4544b49368755e5018389175325a885a0d570de451654c5d5c`  
		Last Modified: Wed, 02 Jul 2025 06:06:03 GMT  
		Size: 2.3 MB (2292843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:509f6b3596a6bea88b7d0f859385be8547838576fdbe686eacdaea208f9b2831`  
		Last Modified: Wed, 02 Jul 2025 06:06:03 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:483e0b33995d66f6821b5237509c67adb4b39306ed42de478ac337becf656c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79366646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5b9f84c33891f3dc219721a62767962168764780b2c2771103d564c98d95ef`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6834481eb5cb86fccd4c316a42c5ccfd1e36bfa47555c92b06cd35ca3737b31b`  
		Last Modified: Wed, 02 Jul 2025 06:50:22 GMT  
		Size: 52.0 MB (52007374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0241fb1343975006bebee571c8d437507431b88d18ef70a2ebcee988a341eec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6f21b51378ba75534e458ad7f5d4fa7a89562315085a07cf278a853aefe767`

```dockerfile
```

-	Layers:
	-	`sha256:310e6d683df6ff0650d6d0cafe5286fdad9763d1db5b3ede6da1ed6de4914da8`  
		Last Modified: Wed, 02 Jul 2025 09:05:14 GMT  
		Size: 2.3 MB (2292515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c254076e586a8126088246dfb75b5a233646b36e1f11a3a43b73302310bb247b`  
		Last Modified: Wed, 02 Jul 2025 09:05:15 GMT  
		Size: 9.0 KB (9036 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1483891993cda374e403afd05c87f8905ba37d74151b86308028ad70132bda02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88374294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ebc1bad6cfdb673843fa577e26446f5508a1764549a2876b1e043139cf1c96`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2825b2dd72463568af0062a58a1d99ac9cfbd3b6d91f30aa325c18f5de49d462`  
		Last Modified: Wed, 02 Jul 2025 05:07:17 GMT  
		Size: 53.9 MB (53931673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d0b280ef0be413cfe8c4ea2336529cbe435373d2a15d0dd28a714896a35c41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a899950c1ad454b3e8dc220610dd8562000d9bcaeb175a0c5d20bf4b5b0abc`

```dockerfile
```

-	Layers:
	-	`sha256:7d674e498c77e6e55d36ea2e7db479e5c14b5f968dc51521b0985b3510c60f75`  
		Last Modified: Wed, 02 Jul 2025 06:06:12 GMT  
		Size: 2.3 MB (2296884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd1ac6729bd99f8a98c160b4522231c5a6d1e8efb7b31a98c523f944bc9295`  
		Last Modified: Wed, 02 Jul 2025 06:06:13 GMT  
		Size: 9.0 KB (8976 bytes)  
		MIME: application/vnd.in-toto+json
