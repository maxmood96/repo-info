## `sapmachine:17-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:d8ec8b5c1aa9b9830ecba97d32f56470c8ee3c01a5232672d7d7203cf2592928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:692c4ced677dff6ef406d33fef54356a158e93f8837b3ba2178472af90af8cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227072253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e5353597484d68b6f9571f103b9850d84eedd8aca6dc6ad7748b6b12a69826`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5fb54e52d78619d7bb98d5fb4ce83f6500e0dde9cead4bb54be43f404b1302`  
		Last Modified: Fri, 09 May 2025 16:58:09 GMT  
		Size: 199.6 MB (199561859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:91ad179ca13a68e0bed2d085f389f342c054beb780df4981b0528db576b69e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f38f21b89ebfc154256e4f24f5ef3d183dce5d5db90f856bb4e5f851e536480`

```dockerfile
```

-	Layers:
	-	`sha256:117b3a5212545f20211b9cdc2e82677ee67efd459692705e4bc2a7625be4dc2a`  
		Last Modified: Tue, 17 Jun 2025 09:50:50 GMT  
		Size: 2.4 MB (2383527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83662a089e9ba952e9759f32369c2737f1761f7ee65afa9f9ffc565ecab462a2`  
		Last Modified: Tue, 17 Jun 2025 09:50:51 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3c9da3038b7f8cc7dcdc5994ce2bd4ccc37bbbfc43a1cd728aca521fb916ad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224274074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1baf4e8a2701ea1cc56a9fffb405ef545f75f846d8c8f9ae32a37093849a20`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675d35119948013747b0c0858ba72108c3759da79e67a8b1daaaa17489207ddc`  
		Last Modified: Sat, 28 Jun 2025 16:38:36 GMT  
		Size: 198.3 MB (198296413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:265ce508c682239e82fef2f7e28c3848494bb838a4804bd65f6c80c2c3d43c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa849e56cf4a666838144b1e9510e2ea78f123448b843734fb16cad186cb906c`

```dockerfile
```

-	Layers:
	-	`sha256:dbe352d871922959784837671598778b5f1054d093120ce295fc112590f32a87`  
		Last Modified: Wed, 16 Apr 2025 16:43:56 GMT  
		Size: 2.4 MB (2383213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc2a806a7226cb9f1bc48caa9a44c7972e91d8d83707d4a996df0f34dab3167`  
		Last Modified: Wed, 16 Apr 2025 16:43:55 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1fe54222b33c15b1ea5694f3b0e5689debdfd335426720b7e8bc821e71a3c615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232337953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94eae15777f17821afef485f3568d21b00ef0801fb6781be8e85c42ef59f1c73`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f6f7975230a06b5fd5d2d450018a18f2c8d9b3d806217e87336c84f2440b5`  
		Last Modified: Wed, 16 Apr 2025 17:17:23 GMT  
		Size: 200.3 MB (200261007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:11ef84226be50466b4f6ef425a8778362ce946ec834e7146e49e15b7038a0b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e852b92b90f82d7c1b7a140741f0647dd47dcfd0999aa1e3a1eb57f4fb7c50f`

```dockerfile
```

-	Layers:
	-	`sha256:33bba81805b5418ca360e1a357056573739d3861a33deff755393e354b4adb03`  
		Last Modified: Wed, 16 Apr 2025 17:17:17 GMT  
		Size: 2.4 MB (2385372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:035745e1b11775774ed86bdef0fbbab9a4fc0e325eeca69e27306eeba7f0fe57`  
		Last Modified: Wed, 16 Apr 2025 17:17:16 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
