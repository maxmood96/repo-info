## `sapmachine:11-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:9cae5b633b21e43d892172ea6ccb2e0b2a51eb34f9d3fc82183b6f3fad7ebd6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:c6456fc20d70883560cdd91ed2811ba3f5f3856f5639ff78cef838133f253554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230989449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7842cdf589007e8525809c272841117af0dd356096df8b4518573ea31172a6c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246ffb5602f5999516016983d2873d31f1acf093eb24ca49eeb10758c5280e2d`  
		Last Modified: Sat, 16 Nov 2024 02:57:49 GMT  
		Size: 201.2 MB (201237665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f94b192c0a85f29cf3b39187c80b6aae308a63e414b958e981d416c86db10ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5581b42db471e7cfa7e16e6c78a09d4b21ef3082ee5106bc32db1ae0656f1d70`

```dockerfile
```

-	Layers:
	-	`sha256:307b5d9175b9af8d31670c04529c731c0b90dc9a3eaa960133a05506a01f9347`  
		Last Modified: Sat, 16 Nov 2024 02:57:32 GMT  
		Size: 2.5 MB (2482622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97cf1d2b8cdc91d734b0512d831a197b7e73e6fccfe332741387dba89c4cfd39`  
		Last Modified: Sat, 16 Nov 2024 02:57:31 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6125785c2a64056c7418872cbd4fbe2c0af72ab34e5df35e3dd35480aec63b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228632262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e1f525e3900582b89f4a649cbc6a33165539e5726a3a8e405273c1ca2ec500`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038ca03857cb9230b91955cd3fa6db65d7d2f415b902b2113e5dbd120ddc7e18`  
		Last Modified: Sat, 16 Nov 2024 03:54:35 GMT  
		Size: 199.7 MB (199739837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:122b92f5c706d8f0f25456c454221f2503ca67ae9fe9fe73af66e16a3a869a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dae4ff087cdcc656feebe432c8c8742bc9f273b8e40131e94d335213fd640f`

```dockerfile
```

-	Layers:
	-	`sha256:42b9c3041836c428853e388c3ba5378c95924be53004247ce460da345bcf05b1`  
		Last Modified: Sat, 16 Nov 2024 03:54:30 GMT  
		Size: 2.5 MB (2483813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f20c54b5650b39b086cb3baf8660805c2ecb4d08e4d757f4d536b29f4041e5`  
		Last Modified: Sat, 16 Nov 2024 03:54:30 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b976d9eccb3e0e210f956ffb9bcc6b5d63d6f6666b0bc6b5be8b7031e91a8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222412636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacaa98f398ae362f57afcc3707500e205c23f89915b63dd873eac1508552fb7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eedc4640fc0efafa73de8502c27b3d881c41ea827b5961c6e20ec19596848a`  
		Last Modified: Sat, 16 Nov 2024 03:57:32 GMT  
		Size: 188.0 MB (188023814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:15017d934533c49b05feb074dcf51894af6d0418fbfa7424b98076db9e9eafaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b625725840d637c9d3558e6b075ae96f1e3f82e1226e4c18db931cb39225c4c7`

```dockerfile
```

-	Layers:
	-	`sha256:c20ba20c938823bf617499c1e7216684d4d9b29bc53a6a99fa9fc38e883a8f6d`  
		Last Modified: Sat, 16 Nov 2024 03:57:28 GMT  
		Size: 2.5 MB (2484033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f4bf62bb596b7a2b809a2e25c728aa2fc80735a9b137ae9035ee8a25cda2239`  
		Last Modified: Sat, 16 Nov 2024 03:57:27 GMT  
		Size: 11.5 KB (11485 bytes)  
		MIME: application/vnd.in-toto+json
