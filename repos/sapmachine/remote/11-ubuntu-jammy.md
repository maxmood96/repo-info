## `sapmachine:11-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:8777e3ed82594fbd283253850d47400c9de169f26af996d83be16df30382298f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:55214d2ec67d51a936839fcc12a9eca198bcf8acb4dc41f2f48fd8f6b4ed6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230400066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be75423bc45f453b3884b5fec952fbc638da6b1e56302f936a8922408c143fb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46fa6d92dc4aa9d5abcd26191972c59f5c6144743e0db4595e2f831135cf523`  
		Last Modified: Wed, 02 Jul 2025 06:41:13 GMT  
		Size: 200.9 MB (200864380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5fadb1450100064d106c78040dcfbf04cb3262c6e1a52940a036203dac9b28e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2650725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e96c9820acd58592decbec5311080443100a75dc89243d1d247296e265cb13`

```dockerfile
```

-	Layers:
	-	`sha256:97cc507d7bc9a187b1ace9a15a347270dd413517bf6f358e51b1e16434c187b4`  
		Last Modified: Wed, 02 Jul 2025 06:04:30 GMT  
		Size: 2.6 MB (2640587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ceda3c1d8f2dedb95cb9bcc5b7a333c06ef1c06b7682787c0ada3a8379f6636`  
		Last Modified: Wed, 02 Jul 2025 06:04:30 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json
