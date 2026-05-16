## `sapmachine:21-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:654f3e7226bbc9ebb6ee645e58d5d366bb22ab8a9a737fb9fcb9ed3724f1ccce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e17a0e75f0ac5998375beb11f5a0121af17dbc1539a72a15eaad5ca85ab628e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246056764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc27ccbbd33524447b1cc00e9201f7cf8bccf8ad9425c9205970fb228938a682`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 15 May 2026 21:21:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8887ed081dce3c7ca6e57e74afe11ed1276d0d27e18bc1f4b1c442f2397f2e60`  
		Last Modified: Fri, 15 May 2026 21:22:14 GMT  
		Size: 216.3 MB (216320080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:52cf79f9f95914c9de87976965f8197ddea3ca644692d112c9db9ce8e45f0634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0bdbdb6c10247d511f2cdf21193a9d5595c706b3414c89fc91760c4c5aef4`

```dockerfile
```

-	Layers:
	-	`sha256:549cab69937f5b06d5bdd21561ee84dc141346004abc57cec1c084c6e42f6443`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 2.6 MB (2632760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ac5a2a916a0eb3a861ef483fdfe9721bd187554c082e74708177a12c195ecc`  
		Last Modified: Fri, 15 May 2026 21:22:06 GMT  
		Size: 10.1 KB (10095 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2b8123209f3ef0f38da18428f169b7342a1478c1bf998dfd1e21ca6d58dc223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242147440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4673ed9227e1c80ce3fb8073905d641699cafc2b1ce414eb28d86980eed4a0d`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:22:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:22:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 15 May 2026 21:22:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528a7602452f579ddb683686f293e6707782368e6e566271043f6de56438a673`  
		Last Modified: Fri, 15 May 2026 21:22:33 GMT  
		Size: 214.5 MB (214540817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e664ce57df51a9cce988f71f614db701040f5cfabea7e734202a07a258d497ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1366b6afeecbf39ee63eed12349b925174de137bfc05e0e1ff614947b5d8e437`

```dockerfile
```

-	Layers:
	-	`sha256:bd226e937f395e96f9465d33172838e13ae47c72ebf6bf5adf5f34866b1cf7a8`  
		Last Modified: Fri, 15 May 2026 21:22:28 GMT  
		Size: 2.6 MB (2632490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b0d37b3a6a5701b0d362125994bc5206124f816ba16110be31453c603863011`  
		Last Modified: Fri, 15 May 2026 21:22:28 GMT  
		Size: 10.2 KB (10247 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3dd49c3be3229d8df7db4f8ab219faf270f9fa402ae112b483a42c39406c2894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251945326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf17f23c4c76fa594a179e6922679e709fa4afff19a030f30ae686d8131876`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:39:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:39:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 15 May 2026 21:39:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db909113bc8de7c8b859ddad1201bae99d0e5a4ef433b7f2ddea9ee1c741779`  
		Last Modified: Fri, 15 May 2026 21:40:39 GMT  
		Size: 217.3 MB (217298606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8026c675cb6934de058c6e03f9b21d2e9e9d71b7254b098cd1cb08c4ec934878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c6d41c33c2ba7a80b84db9aa4b6d0f08f75af5c0b4cce23921fa9ad4f6145b`

```dockerfile
```

-	Layers:
	-	`sha256:3d9753772de806dc09e331e48d59c35efd9a694c2decac1d2622c615adf1353e`  
		Last Modified: Fri, 15 May 2026 21:40:34 GMT  
		Size: 2.6 MB (2630370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990577698f2555bfac568dcf6e02df6f89297275408cd7f40659761116616f63`  
		Last Modified: Fri, 15 May 2026 21:40:34 GMT  
		Size: 10.2 KB (10163 bytes)  
		MIME: application/vnd.in-toto+json
