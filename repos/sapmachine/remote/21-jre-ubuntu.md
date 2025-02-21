## `sapmachine:21-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:02830db659818e2edeaa711743d8b22fa6802f495ba5abca20c1efc2d3475802
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:e9e17e2021797e7bed6299c2bc23a194f810ec57a0da2cc482b6688f29e8b25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89865351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625e59036db53dd806da86a29f525e6a78a0bdc35fbc3a21f163f3c1f88f4bb4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0ccc56aee379584c08b0d4ab8666caa76aee7474e0b1aaff3ffced1c114bf8`  
		Last Modified: Tue, 04 Feb 2025 04:48:38 GMT  
		Size: 60.1 MB (60111061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:344c0adde1622045ef99b250429fc2e24114c40fd8e36c47cf09e77c4e112538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9792290ad6b8588e8b09dfd20c7995ea6a01a7e1d86e2335dfdaa26093114c16`

```dockerfile
```

-	Layers:
	-	`sha256:f0df94cb9ecc195957117689b189691d6f5045fbd969bf8de0ee77a81fe3ffc8`  
		Last Modified: Tue, 04 Feb 2025 04:48:36 GMT  
		Size: 2.4 MB (2390003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4484dfb9ee2cae2a241c0aabce15721f583dc57fffb7a4da0d0849cd4999383`  
		Last Modified: Tue, 04 Feb 2025 04:48:36 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c10617d3110d00780f5850c73902c3e08f5497c9a513b94017027106fdc191bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88194673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce51439651c9504b43b0bb4076d8ded76ad6a9e9d52a8585233951f8e0f008f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39103295c0d84626d0268d15d6116c5e6027bdbe07ddc57adb4c6ae859565912`  
		Last Modified: Tue, 04 Feb 2025 15:27:43 GMT  
		Size: 59.3 MB (59301075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:24d4a42535c8557aac13a52f296e3536e3041ded89d5f63bcbf683078e1bc1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edba1a824c22d206df0d24c4bc467d1d897472e001cc5ca74937be18bd3b383`

```dockerfile
```

-	Layers:
	-	`sha256:fb6091ce8079a15a85ff4e19dab98cdc17193cb3e386c21dd09db328b3872582`  
		Last Modified: Tue, 04 Feb 2025 15:27:41 GMT  
		Size: 2.4 MB (2390531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94921f5e58c7d685026e4daff82f02dedcc281976dedd0a261be2d67a445171b`  
		Last Modified: Tue, 04 Feb 2025 15:27:41 GMT  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d56b0d0cad18f5829686f266d416081ba5619bf580ef86a5a4dc1667907e06a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96199315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41b9432b939c3ef0875ef609c40b225083df8798e7567ebf0ffe1d5a06594a8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4453ee61c0d5c1bd22cf976ee39fb0b14b3ea327d36aa14663002f4a650f051`  
		Last Modified: Tue, 04 Feb 2025 14:37:47 GMT  
		Size: 61.8 MB (61809491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e5462a2719ae1be465cd78b3731759792a9ba33161c9e6eb4c1ea737d9ecb988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad675547915e7b88a2977fae911cda4d414817b1439be012c0bb6fd850d69067`

```dockerfile
```

-	Layers:
	-	`sha256:e82cdee0435ba898b384624ba20b82fda623d4a4df2dcdb772afa14e6024563e`  
		Last Modified: Tue, 04 Feb 2025 14:37:45 GMT  
		Size: 2.4 MB (2393972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68b89c57ae5bbe141ea735143e53104cea21e39368a363a45c40bd0b6056e0e`  
		Last Modified: Tue, 04 Feb 2025 14:37:45 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json
