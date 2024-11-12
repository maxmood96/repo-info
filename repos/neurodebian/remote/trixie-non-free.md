## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:e69cbee7d65af11160c8da53d6f4fb639cab4a59f6d5e279d1c1590ec14200d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a30d0910eee54e78cff1ebacfbf94d0f5d1bcfb233729937a5383b3b8754aebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59860224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58b7b67a10ad31319482f49ce07ffaed1409f4bdc42bdb57591f94a9f55f870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463f8d68a16e9ac92c12f43868402c6f3f57d26fdad10a18f8469cbe505b5557`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 6.5 MB (6527838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb52b6a48245f5a8831658b3aabe3cf7c7ff05fac76e80b3f6301fae8148095c`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d374d800c72b49ed8fe36ec4a126f57a5db7d2354dd3a32c800f1143d1a7`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0266e43d73ad49f9d716b54f8d979e37b5114c365d04ef4a24186995d7ec2739`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 91.2 KB (91229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf7b9db2b69c3f521edd6792979833642d688b878bb51d6390bb1461a1fa26d`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bcdc6c21779357df565f1ad14a6f8c8508b2a8dc04d4b1dbbc25d4b2cd773cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575d2ce06e3134c6340d5878b4d0403f24d2d7ebc47116f54490e5c6a19ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:26e7003cef78c34f6c8b2ab579f8ffd7624e7c5566f72feec2ab5465909c0ad7`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 3.5 MB (3538040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51fb57aa93986c771ed7fb9e961105a680c9f6cd0999e682188320cdf94ee724`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9800c97a370a781ffb9871de33494c3a06907666e74ec5dfd30006c9acd5d149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49241192e3ffb655678dd748976796c720d47028f0001ebb417840254c4d9524`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507ba0d1af87c79eb5ed21e470daeb6651cd6fd35ac71c7f4316437bcf9838b`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 6.5 MB (6513412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea37e5d08e4432023f6c69cebd438dd20a209a3cd3b94eb789a8c4f80f5fb74`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7766e08b26d04d33fce1a14d04e2233cb4eb74cda5d72aaa29f51748001414e`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41352cbfcbfbb365bc31271939a7c8835966e68a87266f29c649ba4302e4f95`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 91.9 KB (91941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45f485faecfdb395798bd27324e61884a7fa42eb02cb31494f7362503104`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4bf8e13d9e5fde0aa2ec003ed93ba575b296b6a1fa393a343426333a5f3bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67a8e580c3f4979cbb59915aab3ad2437957ad387641a293eb5a716dab2d9b`

```dockerfile
```

-	Layers:
	-	`sha256:2a1b5b9e67e1dc1eb6abb7fe584c62fd8dc2ddf3e9842df732676c693cc1a80d`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 3.5 MB (3539082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b9375ffc08954ec2b358f015f7142cdbd3b31bc5835e0cbea70ffa77c06bad`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 15.6 KB (15649 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:534dce1a3347a1871c4179745706a330c6b415fa9fd8eda2f32b41251d970ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60825149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a57bbdf189d2c4ec8efaa71b304424be58a2d1e58cd22074929fe6c196ca00`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0ffbd19363ce5a9fc6e9f7187c63b2555049a39825812a94c390e6d270d52`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 6.6 MB (6635929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172f7e731b0de0a50742f1afcbacaebdf9c053a18fe4aa63b34f108143ce784f`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a4148e81020142fc4c880700a5d8912a5ba1357a3e86a38dbfdf1421011cfa`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cebeba3a77966586091e95bab2b4a598231d8c300e6551fd937ddbd75a7d9b`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 91.7 KB (91650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80068347cef0c5223d5f71e7dc0d64b732ec48e36d6055338c7f363bc46f3a23`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50deb3e18194c5d466b1b6686d20d650631d5abb9211cc67f1275a9f18c945dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fc10c3e19ac99eb4c385e5f1d514019783499f18773f359e61963a5cf47327`

```dockerfile
```

-	Layers:
	-	`sha256:5827057745618179658ddb32068a4bb10e525186aed20b21cd4ce612b5e0268e`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 3.6 MB (3565563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dd822b3c8e11b3af5d8111e0582dee4147705a9e8c8e9f967578b5d00b5d286`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json
