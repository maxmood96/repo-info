## `sapmachine:jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:c9c75394991fc66f70dc406d99ba2b1eef345f0ccb0d514970314feecbad571c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:db777e3fb3390f29a030e85735c4a654fb4da569486ca94b8c66228144efbce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97793467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e32353fa5e997c534e09e37102608af92b43ee118e22673db1a610fa20acdb`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a41e42143dfa2d3a66d892e2284d2cade47cd251803e96a9ba21d2f1851d`  
		Last Modified: Tue, 03 Jun 2025 04:17:32 GMT  
		Size: 68.1 MB (68078130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:11fdf815422c961917aa9cf5190c499902049f55c4b95f8a6358ca95579aed9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3403ef18ef49352621494e51dd4d21027304d19f89f79e125f401d13f66797ca`

```dockerfile
```

-	Layers:
	-	`sha256:ca570e9c4bf625cb6b49e3f53180cbb73e29c193af53d13771a7e3a7c39f7a03`  
		Last Modified: Tue, 03 Jun 2025 04:17:30 GMT  
		Size: 2.4 MB (2419058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6fc627c51227766ce5c770074d4c10faa385ed8e75cec6bb75d60fd90a1ef3b`  
		Last Modified: Tue, 03 Jun 2025 04:17:30 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; arm64 variant v8

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

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

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

### `sapmachine:jre-ubuntu-noble` - linux; ppc64le

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

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

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
