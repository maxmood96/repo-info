## `sapmachine:24-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:4523a190a7b10bcc0d373cc7a5c1e63a69bd8ebb4f2056ac8c10f0d574dcb52b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8b514eb01663b748a463517cb31e8744eba5c26d6314ab4b8e2cedc03810975d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97795433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3585652fa0f8147372ca696ffedce342f3916d1f066d60865074fb83f9363a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fdf661188af0eecf56c0937ff3b304245d5d6d7822a595f1de7d0467b358aa`  
		Last Modified: Mon, 05 May 2025 16:36:33 GMT  
		Size: 68.1 MB (68077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9f08c0c3c03217148972241b2ff5c1e5288a18cc868846846e2cec6ccee13be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a20ed7813711bee1426462d73a1749396466dca10d9b75137532accf55fefd`

```dockerfile
```

-	Layers:
	-	`sha256:4088d1ea75652e2464e542fbec3670321adccfe3ffdfc87613312d00c8f368f3`  
		Last Modified: Mon, 05 May 2025 16:36:33 GMT  
		Size: 2.4 MB (2394850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1c83e176202f5c3ab1a47419807b562b7b0714485bd61b91cbd217cb12c81c`  
		Last Modified: Mon, 05 May 2025 16:36:32 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e540f21fb90629e693b42d76774a5720385a5d96c307f8b7ffc60c06f0d7ad5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95966461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f2f96a7a283b813f5200914803752be9924ba475ec2d545377c085bde9de2f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f67cc60b0db30ec924ad6230006b5d16ad5847fe5b657a462f896a361553d3`  
		Last Modified: Mon, 05 May 2025 18:25:13 GMT  
		Size: 67.1 MB (67119585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:441091ee5be044bc3f3eeb41c43166f3a816a55538fe8e2804f476a82f14e873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182462e40cef415fda5c5952d46cbbb1e3411a5e69aca38bdb848435fb96835b`

```dockerfile
```

-	Layers:
	-	`sha256:8e8918ccde27408fb115d719c3e874bd7a1748f1d8d6c3ec1f0783d054a89005`  
		Last Modified: Mon, 05 May 2025 18:25:11 GMT  
		Size: 2.4 MB (2395375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:775c159186ab0eaeb564086c3fb9e3334c1f122fa1999cc671210d0333e9f342`  
		Last Modified: Mon, 05 May 2025 18:25:10 GMT  
		Size: 10.6 KB (10590 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:30e22db5ee1ef02e4e07e5924bd50848a55e3ac7a1f5dba27ac536aac6e03f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103800179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2687f2fd04a1519f82e66a86d00c566efa762729d5655d40553e73c82628e5ac`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be321d17dd215900955a05e4667af2693a7b770b84a1a85278e0a31797b3e99`  
		Last Modified: Mon, 05 May 2025 18:13:59 GMT  
		Size: 69.5 MB (69459341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:193970c158c9b2095eebf57cbacd5f06c6baf9568202d907132d9846e680a74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b07326b9ccfb8cb4da9db7a25bcb030de1bb484c0fe571cb8ff7441d742d37`

```dockerfile
```

-	Layers:
	-	`sha256:1daf996a98cabbfe8eb70d1723066d92872bf9ef0ce81bb806b701ab33e1f29f`  
		Last Modified: Mon, 05 May 2025 18:13:57 GMT  
		Size: 2.4 MB (2398189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a908dc1cf82589fca2ce5a8879c33ee0533511d554042efbfb07545c9d88c3e2`  
		Last Modified: Mon, 05 May 2025 18:13:56 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json
