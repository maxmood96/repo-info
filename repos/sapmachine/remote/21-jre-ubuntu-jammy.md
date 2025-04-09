## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:1e2c6400868cf75996515d2e1bfadbffc2f29dd70315455a0913c356b82f64b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2b30aeb9da3ac320f531c26f780d23974e120abee0806fa4152f8dd00c5a3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89257106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4c685989864a7b94f2bb9f75ffb57b0ab29b6fd45157140d27af9c0ed8b4dc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee534d44c1594fd2887ee42502ead08fb9f58d7c5132c297ff0564a2a9b6dd1`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 59.7 MB (59724741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6ac01e8a5c24e16a34e90d3a837b12ca9c67f5966dba9d09bff675688729682a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55137f24627a20590f88d76850d53008212546ec4495f6f92591cd395ead770b`

```dockerfile
```

-	Layers:
	-	`sha256:c3e5489f0851e37fbe549177ef922b9c87e40d2f615c389da1ccfee906755ea8`  
		Last Modified: Wed, 09 Apr 2025 01:21:04 GMT  
		Size: 2.4 MB (2409372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a96e7be661538415daa3c4b8d5f1b38102209929a9217c021a6cb449f0fba9`  
		Last Modified: Wed, 09 Apr 2025 01:21:04 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:06d10b575fcf0a9c1ca9f34e0d6a5097ce008bf574eeeba964a4197fc6e0dbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86214474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f831d44b6f77dfeb87e293a3aa3177c174f5bbd139be647364fe3f0f99ea50`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23becfad8f3175f5149f8eb4f8caac0a04af11e69c1248224352bafc28630357`  
		Last Modified: Wed, 09 Apr 2025 09:34:34 GMT  
		Size: 58.9 MB (58860243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:425e7fdade4714dc7528dd5d11cbed7078f9dd2347a5b347127ab86db6967698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ccd476719d5861a88a2faf93d5a35ff1b13fc752e2e836cb3dc6f2dd7ccd6f`

```dockerfile
```

-	Layers:
	-	`sha256:71c89b2e8fa790d05b3237c377f45c9020c6aac666aed8041afc0f6b7379cdb4`  
		Last Modified: Wed, 09 Apr 2025 09:34:32 GMT  
		Size: 2.4 MB (2409078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ad9003ab5f56937069016d73100294ac6b3afe3441d9d6d03d1f923c6d5607`  
		Last Modified: Wed, 09 Apr 2025 09:34:32 GMT  
		Size: 9.6 KB (9607 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5654beb223f23aca91cb30a22c54d722bac729c467d1965b026f688b3066dda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95738464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d04c5b2a0284261b82027d9e4a67f7e83cb209d2348749d02c4d9db2483f2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f343a7efc884c1e057ede44d8c7285f78618778056bd912c181e24ea7be35a1e`  
		Last Modified: Wed, 09 Apr 2025 07:01:02 GMT  
		Size: 61.3 MB (61295768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d4c7add7bfa702b72638fdc7472b4b301b8225e081d8c511de0a13a0250093b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ed644ac61c661e847be76e4ce48e19114a45767a4bd574fc1d24da39fefd1`

```dockerfile
```

-	Layers:
	-	`sha256:55ecbda50499f0f2cc93bcd2dc43b4faeb8cd21e65281b4f1c4db4a0b5425f10`  
		Last Modified: Wed, 09 Apr 2025 07:01:00 GMT  
		Size: 2.4 MB (2413365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50bdee5f986b01a44a562d8820d8563faa0c2ac81a00242723abb6fb45dcd2f`  
		Last Modified: Wed, 09 Apr 2025 07:00:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
