## `sapmachine:24-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:0d379bcb6d2d26adcf3928b24b59a0a2a421009637265c1586cc6a2b72ea84b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c04feca7d88c43b0ada97162bb051791babef18e0385ba8446cbdde2e39a7ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96000678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74291cddb034ac29f1957224cc828a895819b5f4c895ec44c1e2800dd6cd7dfe`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cf0825f365ad7bca0f2e5054febdf5ff35af93bc58221548eeb09d4e75d526`  
		Last Modified: Mon, 05 May 2025 16:36:47 GMT  
		Size: 66.5 MB (66468064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:870200250355c074109ef4c480f043f91c84e3a76a18d0b708cf538a51356f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5e050789f6f06cfcf76ba21f2a3de9acdc24a660ede750c831e8497e26caed`

```dockerfile
```

-	Layers:
	-	`sha256:24acea9594ea57e8250cb660dd394eb30bcdeff6e4ab4a82ba14330b9131f822`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 2.2 MB (2173966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145df2639e47e560590e6cdaf44c71633af22a2b6b86b5f3b95c5519777a3fd3`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ce65439994cf9ef90a1d2b59bfc6230f56482368dd9947f8fc50e0557e7faea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92810132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbc2a2b1c45736303084b48385eaa453118c3661d965167195f6e4f3cd20ce8`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e734b6f308fa90bb08ec60788146681859959a49e5e3775f2d159c7dbdc1d331`  
		Last Modified: Mon, 05 May 2025 18:29:50 GMT  
		Size: 65.5 MB (65455921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5c3e11588b11e033b82bf783d96781b4c49113074a80bd669644ce8c28df4da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756d0e69a0209c3394e299b963b9c20beaffd63103010b2a31bb822c16d78a36`

```dockerfile
```

-	Layers:
	-	`sha256:a998e22c8308ea9d63c3833fcfe13d78dae71ceee55382c4d9143dd4a90607de`  
		Last Modified: Mon, 05 May 2025 18:29:48 GMT  
		Size: 2.2 MB (2173659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1e7d70cafb549137e863aa2b3520ba025a81ded8a1dd787cc398ab6bb276d5`  
		Last Modified: Mon, 05 May 2025 18:29:47 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ba6f8d8a768084378011eae8bca95f851435b8eaa840a12ee355ee7f2d1a1029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101998754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ff8c344525a5576365b80c0428d3069b547862e5bff03be67176795e5e6162`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5fd88eeec9d77d50d06cedd23da90a32650976d46e7a75132fece4ee715990`  
		Last Modified: Mon, 05 May 2025 18:21:13 GMT  
		Size: 67.6 MB (67555539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3ed6d0a21dbd5ca65484da168e5c36dd6f805951ce22db55316e3fd7b64de778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748739d1c01b5ab0457d264ab9bf3b5f18b314310164d68d009f49900332b8a4`

```dockerfile
```

-	Layers:
	-	`sha256:379589935e78219910318ba1219b1f9a1c3659ac96879178130272a669d2e6ad`  
		Last Modified: Mon, 05 May 2025 18:21:11 GMT  
		Size: 2.2 MB (2177259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bd54b51f08fa7e41a4ab1ecd461425c895e4a63ce547674d51188edd6bf319`  
		Last Modified: Mon, 05 May 2025 18:21:10 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
